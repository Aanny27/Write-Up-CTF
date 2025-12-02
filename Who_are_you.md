Link challenge: https://play.picoctf.org/practice/challenge/142?category=1&page=4

When I lauch the, I arrive on this page

<img width="1065" height="681" alt="image" src="https://github.com/user-attachments/assets/edaa1729-28aa-410a-93fe-3508d67b40c8" />

It note that the only user from PicoBrowser can acess the real site. Therefor, I used BurpSuite to modify the User-Agent header to PicoBrowser.

<img width="1017" height="434" alt="image" src="https://github.com/user-attachments/assets/0e742ec5-2744-4f35-a68d-d73af3283b96" />

Next, The page tells me that It don't trust user visitting from another site. So I add Referer header and put this value: http://mercury.picoctf.net:52362/ ( is link of website )

<img width="1026" height="478" alt="image" src="https://github.com/user-attachments/assets/5f32ea49-8675-4c45-b970-b0415f23c565" />

It only workrd in 2018 ? Add the Date header and set in 2018

<img width="1029" height="572" alt="image" src="https://github.com/user-attachments/assets/63d9bc24-61e1-4a09-aaa9-9893c11565a8" />

Tracked ? This notice refers to the DNT header. This is the header users send to request websites not to track their browsing behavior. Let's add DNT (Do not tracked) header and set the value is 1 ( 1 is Do not stalk and 0 is can).

<img width="1023" height="469" alt="image" src="https://github.com/user-attachments/assets/ff592be9-a378-41c3-85a6-e179ebea205d" />

Okay, now it says it only accept people from Sweden. So I change IP to Sweden IP by add X-Forwarded-For header and choose the one on google. 

<img width="1035" height="497" alt="image" src="https://github.com/user-attachments/assets/ffb7311f-b11c-4b2b-a071-3b2621694d02" /> 

Now we just need to add the Swedish language code to accept-language and we're done.

<img width="1029" height="508" alt="image" src="https://github.com/user-attachments/assets/5db62a09-4d6d-4d8a-b84f-77cfda7984f3" />

The flag: picoCTF{http_h34d3rs_v3ry_c0Ol_much_w0w_0c0db339}





