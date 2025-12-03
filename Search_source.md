Link challenge: https://play.picoctf.org/practice/challenge/295?category=1&difficulty=2&page=2

Access the website and I don't see anything strange. Because the title is Search_source, so I checked the source page. But it is too long and too much.

Base on hint, I used linux to copy the entire web to my computer by wget command. 

<img width="574" height="56" alt="image" src="https://github.com/user-attachments/assets/7334f6e4-41bf-4ad3-95f2-5d1fa78f5b6b" />

Now, in your computer workspace will appear a foler has name like this 

<img width="214" height="60" alt="image" src="https://github.com/user-attachments/assets/67032bee-a255-4999-9925-3694d2d220cd" />

cd in it and use "grep -r "picoCTF" to filter the flag. "r" to recurse into subdirectories

<img width="618" height="109" alt="image" src="https://github.com/user-attachments/assets/376066bb-3216-43ba-9553-535ed8e63aca" />

The flag: picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49}
