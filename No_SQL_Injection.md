Link challenge: https://play.picoctf.org/practice/challenge/443?category=1&difficulty=2&page=1

<img width="869" height="565" alt="image" src="https://github.com/user-attachments/assets/21083100-f501-4188-b9c0-72078a0f5ffe" />

Upon accessing the website, I noticed a login form. From the tilte, I see this is a No Sql injection category. I used Burp Suite to modify email and password ( u can get the email from source code )

<img width="1015" height="484" alt="image" src="https://github.com/user-attachments/assets/bb3ca5c6-8275-4a76-85f0-73a9ac6a4f6b" />

The respone returned "password.startsWith is not a function". This mean I sent an object but the server expected a string. We can see this in following code: 

<img width="455" height="157" alt="image" src="https://github.com/user-attachments/assets/db475497-a4f5-4046-ba7f-f3e5594e3430" />

When I sending the payload { "password": { "$ne": null } } via Burp Suite with Content-Type: application/json, the Express body-parser middleware parsed the password input as an Object. Consequently, when the code reached password.startsWith("{"), the server crashed with a 500 error because Objects do not possess the startsWith method

Solution: You have to send data such that password is a string, but the content of that string have to looks like Json starts with { and ends with }.

<img width="1334" height="497" alt="image" src="https://github.com/user-attachments/assets/5c030e7c-5e0d-469d-ae28-82bdbf8bcacc" />

Modify the password like this:
{"email":"picoplayer355@picoctf.org","password":"{ \"$ne\": \"abcd\" }"}

<img width="1332" height="489" alt="image" src="https://github.com/user-attachments/assets/7771a8d4-ef22-4c4b-9d10-dee6b524153d" />

The Flag: picoCTF{jBhD2y7XoNzPv_1YxS9Ew5qL0uI6pasql_injection_25ba4de1}

