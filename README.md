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

