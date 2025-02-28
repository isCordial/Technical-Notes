---
tags:
  - cybersecurity
  - blueteam
  - competitions
  - NCAE
  - linux
date: 2025-02-27
---
# Preparing for a Blue Team Competition as a Beginner

> [!warning]+ Notice
> This article focuses on blue team preparations in the context of **Linux-centric Environments**. It does not provide much blue team advice specific to Windows environments.

> [!note]+ My preparation notes
> See [NCAE 2025](../../My%20Notes/NCAE%202025%20Preparation%20🛡️/NCAE%202025.md) for comprehensive links to my prepatory documents.

This past February, I began volunteering in WGU's Cyber Club. This afforded the opportunity to participate in the [2025 NCAE Cybergames](https://www.ncaecybergames.org/). It's a single-day blue team-oriented competition aimed at first-time competitors. This is my first experience taking part in a team-based defensive engagement like this.

As someone with a previous background in software development, I like to think of myself as fairly capable at the terminal—and with tech in general—but nothing can really prepare you for the open-endedness of a competition like this. There are a lot of approaches you can take, each requiring specific knowledge one might connect the dots on. Because of this, It was difficult for me to come up with any kind of "comprehensive" study plan.

So, I sought the help of others. Here's what they told me. Keep in mind, this competition mostly uses Linux hosts. This article doesn't offer much Windows-specific advice.

## General Tips
- When you have *lots of options*, don't consider *too many* of them all at once. You will experience [Choice Paralysis](../../My%20Notes/Unsorted/Choice%20Paralysis.md). At times it's best to pick a certain tool just to get experience with it. If it's not working out, go to the next thing on the list.

## Core Skills
First and foremost

Keep in mind that this entire list may be more or less than what you're after. [The NCAE has its own YouTube playlist](https://www.ncaecybergames.org/tutorials/) that covers fundamental linux skills. It is comprehensive, but can take awile to 

### Research Skills
Not necessarily formal research. Knowing how to quickly and tactically prompt search engines and various other tools can get you needed information fast. Knowing when to question results is just as important.

### Linux Fundamentials
- **Linux**
	- Navigating the Linux Command-line and File structure
	- Bash syntax
	- Common commands
	- Service configuration
		- systemctl / systemd
	- Networking in Linux
		- DNS
		- Opening/closing ports
		- Routing
	- Windows 


## Gaining a Competitive Edge
There are **key skills** one should be familiarized with before expecting *competitive* results in an engagement. I am not saying one *shouldn't compete if the skills aren't yet in their toolbelt*—these engagements are great ways to acquire them—but, if you plan to *win* preparation, study, and regular practice are an absolute must.

## Temp notes
Echotango + w33t notes:

- You are root 
- There is no GUI.  
- There is no locking yourself out bcuz proxmox 
- Ssh 
    - Ssh config 
    - Ssh proxying 
- Common service configs 
    - Nginx 
    - Databases (SQL, postgres, flask) 
    - Bind DNS 
    - Certificate services – certbot 
        - --dry-run DO THIS BEFORE RATE LIMITS IMPOSED 
- Monitoring 
    - Syslog? 
    - Wazuh? Maybe not 
- Ansible 
    - Add hosts to ansible inventory 
- `lsof -i –n` 
- `Lsof –p <process id> #open file with process id of <>`
- Ls /proc to see the process id folder 
- Run srtrings on exe file on memory  
- Pay attention to where the file was invoked at to look in the `/proc/<processid>/cmdline` ##cat this file 
- Come up with a triage of IoCs.  
- Search all hosts for IoCs. For the SAME IoCs you've found on individual hosts. 
- Runbook?? For IoCs 
- Netstat and ss comand are looking for ioc 
- IPtables deep dive wouldn’t be a bad idea. Nmap scan deturrent  
    - Localhost firewall per host??? 
    - We need a way to share passwords  
    - Ssh keys?? Add pub key to auth_keys 
    - Practice enviroment???? 
    - Digital ocean for one box for the enviorment AZure terraform few bucks... 

Discord 

Black team – they are there to help remember this is a beginner level comp and you are here to learn they are here to teach  

Red team – they are there to make fun with you   

Potential Roles 
- Someone watching the attacks 
- Could a less experienced team member "get the 3 checks" as fast as possible? 
    

Questions 
- How do you profile the scoring engine? 
    - Looking at http logs 
    - Looking for keywords for certain exploits ---> drop those packets 

Links: 
- https://redsiege.com/tools-techniques/2019/05/logging-passwords-on-linux/

Misc. Tips 

- Lsof command 
- Absolute Musts: 
    - Take backups immediately 
    - User / group setup script 
        - Memorize your own unique passwords 
    - Least privileges 
        - File/folder roles 
    - Vulnerability Scan 
    - Backups   
    - Monitoring 
        - Wazuh – (anihacc had set up something) 
    - SSH config

## Credits
Thank you to these fine folks for taking the time to offer their expertise!

- w33t
- echotango