# Keeber 1
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166417220-ea9a6b4d-7621-4d3b-939d-f0174e7b279e.png)
## Solution
Google Keeber Security Group to find their domain (keebersecuritygroup.com) and perform a whois lookup to obtain the flag.
![image](https://user-images.githubusercontent.com/63440532/166417355-a22de98b-0e0f-491c-a01f-6fc262400138.png)
## Thoughts
Pretty straight forward challenge, tests the player's fundamental knowledge on querying domain information.

# Keeber 2
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166417452-ba731756-fecf-473d-b73c-767779bff7d6.png)
## Solution
Use the wayback machine to view an archived version of the webpage keebersecuritygroup.com/team to obtain the flag.
![image](https://user-images.githubusercontent.com/63440532/166417557-5ddd7826-e502-4891-871a-2d5872fbe70d.png)
## Thoughts
The description gives a hint to find an older version of the webpage, and the first tool that came to my mind was the wayback machine.\
Great challenge for players who don't know about the tool, it's something new to learn :)

# Keeber 3
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166417588-4b9e5204-28be-4d2b-8324-ac74e4a8efff.png)
## Solution
I looked through the github repository and found this token in the history of .gitignore file.
![image](https://user-images.githubusercontent.com/63440532/166417744-8969dc19-8876-4e57-910e-db7909be6fa8.png)\
I spent like 30 minutes being clueless on what to do with it till I came across this webpage while googling for information.\
https://docs.gitguardian.com/secrets-detection/detectors/specifics/asana_access_token

It turns out to be an authorization bearer token and I can add it to the header using the curl tool, which allowed me to obtain the flag.
![image](https://user-images.githubusercontent.com/63440532/166417826-bf106605-2ec9-4d62-b852-791d1a6fe544.png)
## Thoughts
Struggled on this one as I didn't know what to do with the token, there was a little luck involved as I was just mindlessly searching and going through webpages lol.\
Overall it's an amazing challenge, learnt something new about authorization bearer tokens :D

# Keeber 5
## Challenge
![image](https://user-images.githubusercontent.com/63440532/166418341-0ce561cc-ab13-4837-b96f-1886bb1828c4.png)
## Solution
This challenge requires some GitHub knowledge and to look through commits performed by keeber-tiffany. Firstly, locate the code_reviews.txt file in security-evaluation-workflow repository. Click on the commit hash shown below. 
![image](https://user-images.githubusercontent.com/63440532/166418404-156fd7e7-81a7-4e1b-80bc-8f6f48ed2b2d.png)
Next, add a .patch to the end of the URL to convert into patch view, which will display the flag.
![image](https://user-images.githubusercontent.com/63440532/166418641-35015f00-6abd-4ca8-8a25-d104b3f8f90a.png)
## Thoughts
Knew how this challenge would work after reading it but still had to do some googling to refresh my memory a little as I don't use GitHub often. Classic but good challenge. 
