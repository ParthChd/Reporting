
# Task 3 - Linux

####  SSH into a server with IP 10.23.45.78, with the user free-now-user and :
<pre>
$ vim ~/.ssh/config  
  Host freenowssh  
    HostName 10.23.45.78  
    User free-now-user   
    IdentityFile  ~/.ssh/my_key 
    IdentitiesOnly yes

$ ssh freenowssh
</pre>



#### go to the directory /var/log 
<pre>
 $ cd /var/log/  
</pre>

### show on console the latest 20 lines of the file dpkg.log 
<pre>
tail -20 dpkg.log 
</pre>