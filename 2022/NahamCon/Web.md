# Jurassic Park
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166406160-ed899798-245f-4b95-b1ea-8a407e150bb9.png)
## Solution
I went through the usual content discovery methods on the webpage and found the /ingen directory is disallowed in robots.txt file\
![image](https://user-images.githubusercontent.com/63440532/166406349-d3bec937-ff2e-42d8-ace0-8193d3479d54.png)\
In the /ingen directory, there's a flag.txt file and I successfully obtained the flag from there.\
![image](https://user-images.githubusercontent.com/63440532/166406410-d5fff887-6637-4b56-99bb-0cafe943d51b.png)
![image](https://user-images.githubusercontent.com/63440532/166406417-348a7055-abc8-4f1b-9b14-f2a4e5d739b1.png)
## Thoughts
Great challenge that tests the player's fundamentals in web application content discovery. 

# EXTravagant
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166409378-69c51d94-324c-4b12-b3ab-20f9ba4021d3.png)
## Solution
The web application allows users to submit and view XML files. From the name of the challenge and some googling, I suspect it might be vulnerable to XML external entity (XEE) injection. XXE allows an attacker to interfere with an application's processing of XML data which enables the attacker to interact with any back-end or external systems that the application itself can access. It could potentially lead to DoS, file disclosure, SSRF and other system impact results.\
Now back to the challenge. So after realising the potential vulnerability, I went to look for a suitable payload.\
I picked a payload from https://github.com/payloadbox/xxe-injection-payload-list and made some changes to it.\
This XML file payload specifies that the &ent entity should be replaced by flag.txt which is in the /var/www directory on the system.\
![image](https://user-images.githubusercontent.com/63440532/166409944-f66f5e82-923f-48e4-979e-a5638b0a9aeb.png)\
Afterwards, I simply uploaded the payload and then viewed it on the web application to obtain the flag. 
![image](https://user-images.githubusercontent.com/63440532/166410083-6a773b4d-6f8a-4b70-aae6-c45e7d72c309.png)
## Thoughts
I really enjoyed this challenge as I learnt about a new vulnerability - XXE Injection. One of my biggest takeaways in this CTF 😸

# Personnel
Didn't managed to solve this in time but still learnt a lot from it.
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166410969-0143827d-a119-48a9-a16b-00850cdfbe51.png)
## Solution
From app.py, I know that there's a list of names and the flag is appended to the end. 
![image](https://user-images.githubusercontent.com/63440532/166411097-08c97ff3-52cc-4510-b23c-e21e60dc8fb0.png)
Took me a long time to realise that I could inject a regex expression `.*` to retrieve the entire list of names. However, I did not manage to obtain the flag even after doing so. Then, I tried using burp suite to intercept the request and see what's in it. Turns out, there was a setting parameter set to 0 by default.\
![image](https://user-images.githubusercontent.com/63440532/166412351-d230e375-f98d-49a1-8cf7-b1d9ce26d521.png)\
I thought it's probably something to do with flag being in lower case but didn't know what to do so I tried changing the value to 1 and 2, and BOOM! I managed to obtain the flag when I set the value to 2.\
![image](https://user-images.githubusercontent.com/63440532/166412425-adb1185b-a05e-4dc1-b7fd-b79194044b45.png)
## Thoughts
I actually found this challenge hard even though it's categorized as easy, took a long time for me to figure out and didn't manage to get points for it but hey, at least I learnt something new which is what I'm here for :) 
