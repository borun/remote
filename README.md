# Remote
Right now it is based on **Zsh**. I have made this tiny tool for my **MacBook** to ease my ssh session management.It is better if you manage your remote servers with public key authentication. You may have one password protected key to log into your servers.

Anyway, download this directly and unzip or untar in your preferred location.You can also clone this using git clone command.

Add the path of the completion directory in ~/.zshrc,
`fpath=(<remote_path>/comppletion/ $fpath)`

In case your zsh completion module is not installed, add this line and restart the terminal
`autoload -Uz compinit && compinit`

Then create a short cut of <remote_path>/bin/remote in /usr/local/bin/
`ln -s <remote_path>/bin/remote /usr/local/bin/remote`.
```
Usage:/usr/local/bin/remote: host_address[:port]|<host_filename> -s|-f
	-s: ssh connection
	-f: sshfs connection
```
This tool is built with ssh and sshfs.

## To-Do
* Removing unnecessary known ssh host of the system
* Creating host file
* Add documentaion for managing remote ssh session using public key
