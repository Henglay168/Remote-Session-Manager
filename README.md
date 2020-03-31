# Remote Session Manager

**This tool will provide easy access to the Linux or Windows Servers.**

![Imgur](https://i.imgur.com/rZaLXBI.png)

#### 1. Pre-Requirements
Here Ubuntu considerded as host machine for the installation setup, but this tool can be use with any Linux version *(Package management commands can be vary).* 

* Install sshpass for ssh with password authentication,

``` bash
sudo apt-get install sshpass
```

* Install rdesktop for Windows RDP,

``` bash
sudo add-apt-repository ppa:pmjdebruijn/rdesktop-release

sudo apt-get update

sudo apt-get install rdesktop

```

#### 2. Installation

* Download and save the script somewhere like ```/usr/local/bin ```

* Make sessionManager executable,

``` bash
chmod +x sessionManager
```

* Edit bashrc and create a custom aliases,

``` bash
vim ~/.bashrc
```

```
#Custom Aliases
alias sessionManager='/usr/local/bin/Remote-Session-Manager/sessionManager'
```

#### 3. Configuration
* Edit **projects.txt**, add a project ID and project name separating by a space.

*Example:*

[Project-ID] | [Project]
-------------|----------
1            | Project_1
2            | Project_2
3            | Project_3


# 

* Edit **serverlist.txt**, add a project details as following format separating by a space. 

Copy ssh keyfiles to the `{script_location}/bin/keys/` directory. 

*Example:*

[IP Addr] | [Description]| [Project]| [OS:LINUX/WIN]| [Username] | [Password or Key File Path] | [Root Password for Linux]
-------------|--------------|---------|-------------|------------|----------------------------|--------------------------
192.168.1.2  | Server_1A    |Project_1| LINUX	    | admin      | ./bin/keys/key1            | null
192.168.1.3  | Server_1B     |Project_2| LINUX	    | admin      | ./bin/keys/key2            | Password
192.168.1.4  | Server_2A     |Project_2| LINUX	    | user       | Password	              | Password
192.168.1.5  | Server_3B     |Project_3| WIN	    |administrator| Password                   | 

#### 4. Usage

``` bash
$ sessionManager
```

* Select project ID,

![Imgur](https://i.imgur.com/RoR8URF.png)



* Enter Server IP and hit enter to connect,

![Imgur](https://i.imgur.com/VBnQj8B.png)

#### 4. Bugs and Feedbacks

Please send you're feedbacks to : dilshanonline@gmail.com


	..::SessionManager::..                               

	Author : Dilshan Wijesooriya                                           	        	
	E-mail : dilshanonline@gmail.com                        
	GitHub : https://github.com/dilshanonline 
****









