---
title: Disko-2

---

#DISKO_2
 
Download the file by wget in linux or normal download is fine🐧
Ok! Now we can use fdisk to list available partitions.

<img width="734" height="331" alt="image" src="https://github.com/user-attachments/assets/66465082-1ea2-4d4d-859e-b854597ff7f2" />


As we can see, it has two partitions disko-2.dd1 and disko-2.dd2. Let’s check the first one.
Hint: How can you extract/isolate a partition?
Therefore, we focus on Linux partition, extract the partition into an .img format, by these commands

<img width="841" height="161" alt="image" src="https://github.com/user-attachments/assets/79f22674-764e-4af2-a587-4b3b326d4512" />


 
Now we can use strings to find the flag 

<img width="513" height="86" alt="image" src="https://github.com/user-attachments/assets/795648f2-bd92-4a79-b725-349d44e401c9" />


The Flag: picoCTF{4_P4Rt_1t_i5_a93c3ba0}
