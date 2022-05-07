# Super Secure
## Challenge
![image](https://user-images.githubusercontent.com/63440532/167235670-aa45bf27-f19f-4645-9034-3b9da0b7c233.png)
## Solution
Upon arriving at the webpage, we can see there's a login portal. First thing that came to my mind was - SQL Injection. I tried submitting a single `'`.
![image](https://user-images.githubusercontent.com/63440532/167235803-d68ba88c-2d80-419f-8140-bcb204431c2c.png)
Aha, I was right. 
![image](https://user-images.githubusercontent.com/63440532/167236699-d0cc085d-e721-4be5-ac03-f4c228d025ee.png)
Looking at the error message, we can craft our payload. In this case, the basic `' OR 1 = 1;-- -` will work. Got the flag!
![image](https://user-images.githubusercontent.com/63440532/167236855-8971959a-d0c0-46ee-b78f-02b9d4c9b1ee.png)
## Thoughts
Pretty straight forward and easy challenge, great warmup though. 
# I made a blog!
## Challenge
![image](https://user-images.githubusercontent.com/63440532/167237072-5e12a49c-fa25-4918-a800-ed9a24cf9c65.png)
## Solution
I performed some usual web content discovery techniques, such as viewing the source code etc. Found something useful at /robots.txt. 
![image](https://user-images.githubusercontent.com/63440532/167237130-7a5569a7-0381-4364-ad3b-cc26c161b611.png)\
Tried visiting accessing the /flag.php but it didn't give me the flag, instead it showed me this question. 
![image](https://user-images.githubusercontent.com/63440532/167237383-a4d6fc56-bf2d-4ef8-bcc2-889a779a3ac0.png)\
I thought it must be some sort of clue, so I googled the three terms `php`, `filter` and `vulnerability`. Hmm, interesting. So it's a Local File Inclusion vulnerability.
![image](https://user-images.githubusercontent.com/63440532/167237520-a2cec76f-1b26-46e9-b615-bde0f36bdff7.png)\
LFI exists when a web application includes a file without correctly sanitising the input, allowing an attacker to manipulate the input and inject path traversal characters and include other files from the web server. Here, I found an entry point on the blog posts page.
![image](https://user-images.githubusercontent.com/63440532/167237608-bd5deee5-b079-43f2-944d-8b197b1325d2.png)
Now it's time to use the php filer wrapper to craft a payload and obtain the flag. The payload I'm using is `php://filter/convert.base64-encode/resource=flag.php`. Managed to obtain some base 64 encoded text. 
![image](https://user-images.githubusercontent.com/63440532/167237869-f750a650-7288-4260-8bf0-40d5795152b9.png)
Simply decoded it using https://www.base64decode.org/ and obtained the flag.
![image](https://user-images.githubusercontent.com/63440532/167237926-a27419fa-d14d-4a54-9920-c6905d0cec6f.png)
## Thoughts
Really enjoyed this amazing challenge and learnt something new :D
