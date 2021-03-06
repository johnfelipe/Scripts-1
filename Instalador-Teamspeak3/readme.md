<h1 align='center'>Teamspeak 3 Server Installer</h1>

<br>

Compatibility / Tested
----------------
+ CentOS 6.x 32bit or 64bit
+ Ubuntu 12.04 32bit or 64bit
+ Not Tested on CentOS < 6.5
+ Not Tested on Ubuntu > 12.04

<br/>

Default Ports
-----------------
These need to be open and can be changed during install
+ 9987 UDP - Voice
+ 30033 TCP - File Transfer
+ 10011 TCP - Server Query
+ 2008 TCP - License Check (only needed if using a license)

<br/>

Install
-----------

#### Run the following one liner as root
```
wget -q https://raw.githubusercontent.com/MartinRaiola/Scripts/master/Instalador-Teamspeak3/install.sh && bash install.sh && rm -f install.sh
```
<strong>Note:</strong> Teamspeak application files are located @ /home/ts3user/ts3-server<br/>
<strong>Note:</strong> Teamspeak service file is located @ /etc/rc.d/init.d/teamspeak (CentOS) or /etc/init.d/teamspeak (Ubuntu) <br/>
<strong>Pro Tip:</strong> Press CTRL+C @ token screens during install to continue

<br/>

Usage
---------

<strong>Note:</strong> Teamspeak Server automatically starts @ server boot in instances of restarts or system crashes.

Start Teamspeak Server: ```service teamspeak start```

Stop Teamspeak Server: ```service teamspeak stop```

Restart Teamspeak Server: ```service teamspeak restart```

Show Teamspeak Server Status: ```service teamspeak status```

<br/>

Uninstall
-------------

#### CentOS
```
service teamspeak stop && userdel -r ts3user && rm -f /etc/rc.d/init.d/teamspeak
```

#### Ubuntu
```
service teamspeak stop && userdel -r ts3user && update-rc.d -f teamspeak remove && rm -f /etc/init.d/teamspeak
```