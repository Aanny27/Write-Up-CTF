---
title: Disko-2

---

#DISKO_2
 
Download the file by wget in linux or normal download is fine🐧
Ok! Now we can use fdisk to list available partitions.
![image](https://hackmd.io/_uploads/SJ3iRPwlWg.png)

 
As we can see, it has two partitions disko-2.dd1 and disko-2.dd2. Let’s check the first one.
Hint: How can you extract/isolate a partition?
Therefore, we focus on Linux partition, extract the partition into an .img format, by these commands
![image](https://hackmd.io/_uploads/BynnAPvgZe.png)

 
Now we can use strings to find the flag 
![image](https://hackmd.io/_uploads/BJ6a0PPgZl.png)

The Flag: picoCTF{4_P4Rt_1t_i5_a93c3ba0}
