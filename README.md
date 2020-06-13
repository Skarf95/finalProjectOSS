# Raspberry Pi Print Server using CUPS
Final Project OSSLAB03

## What does this project do?

Print Server can connect one or more computers to a printer wirelessly. 
With the help of the Print Server, you can put your commands on your device to print your documents.

## Requirements:

* Raspberry Pi
* SD Card
* USB Printer
* Ethernet Cable
* Power Supply for the Pi

## Why is this Project useful?

Wired printing has too much work. With Print server, you can print you documents even though 
you are far away from the printer

## How do I get started?


**1) Upgrade the Pi**
```
sudo apt-get update
sudo apt-get upgrade
```

**2) Install Print Server Software CUPS**
```
sudo apt-get install cups
```

**3) Giving Pi user admin privileges and restart**
```
sudo usermod -a -G lpadmin pi
sudo cupctl --remote-any
sudo /etc.init.d.cups restart
```

**4) Configuring CUPS**

* Go to CUPS page (http://172.30.1.26:631)
And install Samba(sharing Network service) 
```
sudo apt-get install samba
```
* Configure CUPS
```
sudo vim /etc/samba/smb.conf
```
Change guest ok = no to **yes**
```
guest ok = yes
```
Change read only = yes to **no**
```
read only = no
```


**5) Add a Printer to Cups**

* CUPS homepage -> Administration -> Add Printer -> Choose a printer



## Where can I get more help, if I need it?
https://circuitdigest.com/microcontroller-projects/raspberry-pi-print-server

## Presentation video

## License
 
This project is licensed under the MIT License 


