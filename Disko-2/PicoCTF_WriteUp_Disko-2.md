#DISKO\_2

![](Aspose.Words.40131121-854c-4982-b8ba-ba9e11e5217e.001.png)

Download the file by wget in linux or normal download is fine🐧

Ok! Now we can use fdisk to list available partitions.

![](Aspose.Words.40131121-854c-4982-b8ba-ba9e11e5217e.002.png)

As we can see, it has two partitions disko-2.dd1 and disko-2.dd2. Let’s check the first one.

Hint: How can you extract/isolate a partition?

Therefore, we focus on Linux partition, extract the partition into an .img format, by these commands

![A black background with white text&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.40131121-854c-4982-b8ba-ba9e11e5217e.003.png)

Now we can use strings to find the flag![A black background with white text&#x0A;&#x0A;AI-generated content may be incorrect.](Aspose.Words.40131121-854c-4982-b8ba-ba9e11e5217e.004.png)

The Flag: picoCTF{4\_P4Rt\_1t\_i5\_a93c3ba0}
