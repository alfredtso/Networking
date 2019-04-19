# Learn about SSH on local network

## Use Key-Based SSH Logins
- Using password login apparently is a bad idea, instead you should use key-based
```
// Create a public on the client (the machine you use to connect to the remotehost)
ssh-keygen -t rsa

// You could use passphrase for extra-security

Generating public/private rsa key pair.
Enter file in which to save the key (/home/username/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/username/.ssh/id_rsa.
Your public key has been saved in /home/username/.ssh/id_rsa.pub.

// Could increase the encryption level with -b flag
ssh-key-gen -t rsa -b 4096
```

- Then, you need to transfer this ``id_rsa.pub`` to host
	-  You could use physical devices or use ``ssh-copy-id``
		- this would need ssh using a password
- I use usb drive to then manually add to authorized_keys
```
// If the file is absent, create it
touch authorized_keys 

// If already had, its good to backup
cp authorized_keys authorized_keys_backup

// concat
cat id_rsa.pub >> authorized_keys
```

## Modify SSH config file
- Not to confuse ssh config file in ``.ssh/config`` and ``/etc/ssh/sshd_config``
	- ``.ssh/config`` is where you put config so that instead of ``ssh -v -p 453 username@123.13.4.23``, you could `` ssh mypc ``
	- ``sshd_config`` is where you can disable password login etc

- Modifications	
```
// this allows you to specify certain users and address access
AllowUsers username@1.1.1.1

// this can diasable password login
PasswordAuthenfication no

// On my Mac i need to disable this too for the above to work
// Not sure why, i found it on SE
UsePAM no
```


## To Do 
[x] ssh into tmux server on remote server to work on the same session
	- tmux attach -t $YOURSESSION
[ ] use ssh config file on client 
[ ] learn about different type of keygen 

