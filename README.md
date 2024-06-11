# OverTheWire-Bandit 🏴‍☠️💰

<h2>Description</h2>
<b>Over The Wire (https://overthewire.org/wargames/bandit/) has a number of wargames you can play through to sharpen your skills and learn new skills using bash. I played through the "Bandit" wargame to test my skills and learn new ones in my journey to master bash & become a Cloud Engineer ☁️👨🏿‍💻☁️. Each of the levels and the bash commands I used to beat each level will be shown below. </b>
  <br /> 
    <br />  
<i>Note: There are 34 levels, so taking screenshots of everything & documenting would take a while, but I'll start with level 1 so you can get a feel for what things look like then I'll upload levels I found more challenging or learned something new in.
  </i>
    <br />
      <br />
<h2>Getting Started</h2>
  <i>To get started I downloaded Ubuntu ver 24.04 and set up the VM using Oracle Virtual Box.
    </i>
      <p align="left">
        <img src="https://i.imgur.com/YTs30Ha.png" height="85%" width="85%" alt="Ubuntu Virtual Machine"/>
          </p>
<br />
  <br />
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
    
<i>
  This is the initial log on menu
    </i>
      <p aligh ="left">
        <img src="https://i.imgur.com/dWA7Z3R.png" height="85%" width="85%" alt="Ubuntu Virtual Machine"/>
          <br />
            <br />

<i>
I used "ls -a" to show all of the files/directories in the current folder and then used the "cat" command to display the contents of the "readme" file to get the password to logon to Level 1
</i>  
  <p align="left">
    <img src="https://i.imgur.com/b8mSzA6.png" height="85%" width="85%" alt="Ubuntu Virtual Machine"/>
        <br/>
          <br/>
            <br />
              <br />

<h2>Level 11</h2>
  <b> The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions</b>
    <br/>
      <i>Possible commands to use to beat this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd</i>
        <br />
          <br />

<i>
After getting logged into Level 11, I ran the "ls" command to show what files/directories were present. "data.txt" is the only file present so I run the "cat" command to take a look. The output string makes zero sense. This is where I have to look up the ROT13 cipher. ROT13 basically takes any given character and moves it 13 characters down. So in other words if I were to write "A" per ROT13 I'm really writing "N". I need a way to translate the contents of this file to make sense
  </i>  
    <br/>
      <p align="left">
        <img src="https://i.imgur.com/K40sbmI.png" height="85%" width="85%" alt="Level 11"/>
          <br />
            <br />
<i>The "tr" command is perfect for this. I run cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]' & get the output "The password is xxxxxxxxxxx" so I can move into level 12.</i>
  <br/>
    <br/>
      <em>To explain my bash script, I read the contents of the file using the "cat" command then used the pipe "|" to take the output of the file and translate it using the "tr" command. The first set '[A-Za-z]' covers the entire alphabet from A-Z in both uppercase & lowercase. The second set '[N-ZA-Mn-za-m]' specifies what the input stream will be translated to as each character is moved 13 times down the alphabet. Level 11 COMPLETE</em>
        <br />
          <p align="left">
            <img src="https://i.imgur.com/noIwOX3.png" height="85%" width="85%" alt="Level 11 COMPLETE"/>
