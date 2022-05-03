## Flagcat
### Challenge
![image](https://user-images.githubusercontent.com/63440532/166398612-c51a96ff-e66a-46f4-b652-8514fd6d7b16.png)
### Solution
Download the flagcat file and run the cat command on it.\
![image](https://user-images.githubusercontent.com/63440532/166399601-6891c64b-f627-4602-97bf-2c24250a8988.png)\
### Thoughts
This challenge is usually way too easy to be a CTF challenge, however I think it's nice to have it so the entire CTF doesn't look too intimidating for beginner CTF players. Kudos to John Hammond :)

## Wizard
### Challenge
![image](https://user-images.githubusercontent.com/63440532/166399742-5adc2120-9cc3-4c16-9dd8-93e6786794c2.png)
### Solution
There are 6 fixed questions which requires us to convert strings between hex, binary, ascii as well as decimal.\
I won't be going through each of them as it's easy to do it using converters online.\
It's a little annoying though if u accidentally make a mistake xD\
![image](https://user-images.githubusercontent.com/63440532/166399795-f44b6f75-74ea-44e7-baf2-77997d5622f4.png)
### Thoughts
I failed 4 times lmao because I didn't read the last question properly, facepalmed really hard when I got it. 

## Technical Support
### Challenge
![image](https://user-images.githubusercontent.com/63440532/166400246-cae350db-585c-435c-9161-d687518dd01e.png)
### Solution
Because there were too many messages and people doing !flag, u can't simply search for "flag" and "flag{" doesn't work too :<\
How I got it was by applying channel filter in the search bar and then look for the oldest message of "flag".\
![image](https://user-images.githubusercontent.com/63440532/166400510-f9dee48d-bb25-4da5-8022-3d5ba01ed741.png)
### Thoughts
Proud to apply my PhD in Discord knowledge in this challenge KEKW

## Read The Rules
### Challenge
![image](https://user-images.githubusercontent.com/63440532/166400687-54a52119-f044-4924-8be6-b8163d21cfc0.png)
### Solution
On the rules page, use inspect element tool to view the flag written as a comment in page elements.\
![image](https://user-images.githubusercontent.com/63440532/166400719-73dd657a-e606-4729-b335-ea25f2a8aec9.png)
### Thoughts
Great warmup level challenge, helped to get my motor running.

## Quirky
### Challenge
![quirky1](https://user-images.githubusercontent.com/63440532/166400881-2cd18606-11d5-4115-bd2f-3e5dffd3f669.png)
### Solution
Didn't know what the quirky file was so I placed it in [CyberChef](https://gchq.github.io/CyberChef/), used the Magic operation and it turns out that it's a QR code containing the flag converted into hexadecimal byte string.\
![quirky](https://user-images.githubusercontent.com/63440532/166401049-503ffbd7-947c-4dda-bc55-b949c0120e1c.png)
### Thoughts 
Learnt once again how powerful CyberChef is lol

## Exit Vim
### Challenge
![exitvim1](https://user-images.githubusercontent.com/63440532/166401673-75e5658a-32ec-4f5d-8394-7c958df64894.png)
### Solution
Simple challenge to test knowledge on Vim. I used :q! command to exit.\
![exitvim](https://user-images.githubusercontent.com/63440532/166401867-2c49a8a8-9a31-4c2c-adc4-f6f551d51e89.png)
### Thoughts
Easy challenge.

## Prisoner 
### Challenge
![image](https://user-images.githubusercontent.com/63440532/166404730-fac1b887-5bd5-4fe8-b279-f2d155dd14ee.png)
### Solution
Firstly, the challenge requires you to "break" out of jail. I tried multiple ways to exit the session but it didn't work, till I googled and found out I could use Ctrl D to terminate the session.\
Then, it brought me to a python interpreter where I became clueless again what to do.\
![image](https://user-images.githubusercontent.com/63440532/166404944-0947b0f7-e3be-4f6a-b884-4fcfda3805f7.png)\
Thanks to a hint from RiffRaff#4469 on Discord, I realised I had to somehow open flag.txt which is in the same directory as jail.py.\
I googled and realised one way I could do it is using the exec function. I used the command `exec(open("flag.txt").read())` and boom, it worked!\
![prisoner](https://user-images.githubusercontent.com/63440532/166405908-e3bf8008-214f-45f6-a167-e3873779d1ff.png)\
Finally broke out of jail hehe.
### Thoughts
I was stuck in jail as an inmate for so long T^T\
Nevertheless, I learnt new things and this was a really meaningful challenge!
