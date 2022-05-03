# Steam Locomotive
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166413192-68dd9911-455b-468b-82a7-22689f5da727.png)
## Solution
After having the train run across my screen like 3 times, I realised that I had to run the `ls` command which was mentioned in the description right behind the ssh command used to connect to the server.
![image](https://user-images.githubusercontent.com/63440532/166413993-eb75c666-e4aa-420f-8c01-1f1891dca318.png)\
Ah, there we go. Now simply run the ssh command again but with cat flag.txt to obtain the flag.
![image](https://user-images.githubusercontent.com/63440532/166414071-9f2dec9e-ddaa-45e0-bdc2-addc3114cd5d.png)
## Thoughts
Pretty easy but cool challenge 🚅

# WhenAmI
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166414390-db29906a-01c5-46f5-a356-425c6f1fd33c.png)
When am I??

So, I look down at my watch. It's December 28, 2011 at 11:59AM, and I'm just minding my own business at -13.582075733990298, -172.5084838587106.
I hung out there until the local time was 1:00AM on December 31st, and then I hopped on a plane and took a 1 hour flight over to -14.327595989244111, -170.71287979386747.\
Some time has passed since I landed, and on December 30th, 12PM local time, I took a 1 hour flight back to my original location.
It's been 10 hours since I landed on my most recent flight - how many seconds have passed since I first looked at my watch?

(Submission format is flag{<number of seconds goes here>}, such as flag{600}.)
## Solution 
Oh god it's painful to do the calculations, but for the sake of this writeup 🤧
Firstly, it took me some googling to find out that he was "minding his own business" at Samoa, and he took a flight to and back from American Samoa throughout this challenge.
Now here's the big brain trick hidden in this challenge. At the end of 29 December 2011, Samoa lost a day. Yes, you saw that right. Samoa lost 30 December 2011 and skipped directly into 31 December 2011. Hence,

December 28 11.59am (Samoa) -> December 31 1:00am (Samoa): 133260 seconds\
1 hour plane to American Samoa -> 133260 + 3600 = 136860 seconds\
December 31 2:00am (Samoa) = December 30 1:00am (American Samoa)\
December 30 1:00am (American Samoa) -> December 30 12:00pm (American Samoa): 136860 + 39600 = 176460 seconds\
1 hour place back to Samoa -> 176460 + 3600 = 180060 seconds\
Another 10 hours since reaching Samoa -> 180060 + 36000 = 216060 seconds.

flag{216060}
## Thoughts
This was probably the most mindblowing challenge for me, so much respect for the big brain challenge creator @Kkevsterrr#7469 for thinking of it. Really enjoyed it a lot 😆
