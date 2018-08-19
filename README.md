# homeautomation
raspberry pi, openHab,  Black Bean RM Mini 3 

### install raspberry pi

HowTo: https://www.datenreise.de/raspberry-pi-inbetriebnahme-howto/

- Copy the Image to the SD Card on MAC with Etcher [Link](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
- Enable SSH  [Link](https://www.raspberrypi.org/documentation/remote-access/ssh/README.md)
- Enable VNC [Link](https://www.raspberrypi.org/documentation/remote-access/vnc/README.md)
- Copy key to the remote machine [Link](https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md)

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
### install openHab on the raspberry

HowTo: https://openhabdoc.readthedocs.io/de/latest/Raspberry/

```bash
wget -qO - 'https://bintray.com/user/downloadSubjectPublicKey?username=openhab' | sudo apt-key add -

echo 'deb https://dl.bintray.com/openhab/apt-repo2 stable main' | sudo tee /etc/apt/sources.list.d/openhab2.list

sudo apt-get update

sudo apt-get install openhab2

```

Service managment

```
sudo /bin/systemctl start openhab2.service

sudo systemctl stop openhab2.service

sudo systemctl status openhab2.service

sudo systemctl daemon-reload

sudo systemctl enable openhab2.service


```

Than open:  [http://openhab-device:8080](https://docs.openhab.org/installation/linux.html) and choose Standart installation and Paper UI