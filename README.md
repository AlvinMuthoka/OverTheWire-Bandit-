# OverTheWire-Bandit🏴‍☠️💰

<h2>Description</h2>
<b>Over The Wire (https://overthewire.org/wargames/bandit/) has a number of wargames you can play through to sharpen your skills and learn new skills using bash. I played through the "Bandit" wargame to test my skills and learn new ones in my journey to master bash & become a Cloud Engineer ☁️👨🏿‍💻☁️. Each of the levels and the bash commands I used to beat each level will be shown below. </b>
<br />  
<b>There are 34 levels, so taking screenshots of everything & documenting would take a while, but I'll start with level 1 so you can get a feel for what things look like then I'll upload levels I found more challenging or learned something new in.
</b>
<br />
<br />
<h2>Getting Started</h2>
<b>To get started I downloaded Ubuntu ver 24.04 and set up the VM using Oracle Virtual Box.
</b>
<p align="left">
<img src="https://i.imgur.com/YTs30Ha.png" height="85%" width="85%" alt="Ubuntu Virtual Machine"/>
</p>
<br />
<br />
<h2>Level 1</h2>
<b> To log into the Bandit Linux server you need to use SSH. LogOn.sh shows the command & how I used it to get logged into the server. The prompt for Level 1 is below. </b>
<br />
<br />
<b>
"The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game."
</b>  
<br />
<br />
<b>
This is the initial log on menu
</b>
<p aligh ="left">
<img src="https://i.imgur.com/dWA7Z3R.png" height="85%" width="85%" alt="Ubuntu Virtual Machine"/>
<br />
<br />

<b>
I used "ls -a" to show all of the files/directories in the current folder and then used the "cat" command to display the contents of the "readme" file to get the password to logon to Level 1
</b>  
<p align="left">
<img src="https://i.imgur.com/b8mSzA6.png" height="85%" width="85%" alt="Ubuntu Virtual Machine"/>

