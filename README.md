# Bolt-THM

----------------BOLT(TryHackMe)--------------------

Finding open ports:
1) 22:SSH
2) 80:Apache httpd 2.4.29
3) 8000:Apache httpd 2.4.29(This is a bolt cms website)

# There is a comment through admin where i got user and pass

bolt:boltadmin123

Directory Fuzzing:
/bolt directory which is login page of given website (manymore diretory is found:/pages,/search etc...)

when i login to this website using above credentials I found the vulnerable version bolt 3.7.1 which is rce vulnerability

Now open metasploit-framework and find bolt rce
---> use exploit/unix/webapp/bolt_authenticated_rce
(add lhost,rhost,username and password)
use exploit and you got root of this machine

i get flag.txt and finally go to bed:)

