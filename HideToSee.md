---
title: HideToSee

---

#HideToSee
Link Chall: https://play.picoctf.org/practice/challenge/351?category=2&difficulty=2&page=1
Download the image to laptop and we have
![atbash](https://hackmd.io/_uploads/rymnYcHZ-x.jpg)
Look at the picture, I guess it is the atbash cipher, you can search on google:)
Let's use steghide command to extract it
![image](https://hackmd.io/_uploads/ry3h5qHWWl.png)
Now the file asks for a password. But I tried not entering anything and just hit enter and we have encrypted.txt file:)
Use strings to filter text
![image](https://hackmd.io/_uploads/Bk6kocrZZe.png)
Well, now throw that text on CyberChef and use atbash cipher to decode it
![image](https://hackmd.io/_uploads/r1NMn9SWWg.png)
The flag: picoCTF{atbash_crack_8a0feddc}