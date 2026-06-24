
**PICKLE RICK CTF WALKTHROUGH**  
Difficulty: Easy

**Objectives:**  
– mainly focuses on basic linux commands  
– basic web enumeration 

**TASK 1:**  
What is the first ingredient that Rick needs?   
**ANSWER: mr. meeseek hair**

**TASK 2:**  
What is the second ingredient in Rick’s potion?  
**ANSWER: 1 jerry tear**

**TASK 3:**  
What is the last and final ingredient?  
**ANSWER: fleeb juice**

###  **Tools & Techniques Used**

1. `nmap –script vuln <ip>` : found out the login page from here.  
2. Can also use `gobuster/nikto` but not necessary since I used nmap vuln scan.  
3. Firstly, found out the username of the login from the page source of the website.  
4. The password was found from `robots.txt`  
5. Bunch of commands were required for trial and testing after logging in with the credentials.  
   Firstly, I tried ls and saw the list of directories present. Some were sus.  
   cat was not working so had to try other options like:   
   **Alternatives of cat:**   
   less file  
   more file  
   head file  
   tail file  
     
   Since cd is blacklisted too, an alternative can be ‘/’. So, first thing we need to do is `ls /`  
   This shows the contents of the root directory.   
   `sudo -l` means **"list the commands that the current user is allowed to run with sudo."**  
   
