# ClockworkPi-Skins
Skins for the ClockWorkPi Launcher, ClockWorkPi can be found here: https://www.clockworkpi.com/
The Launcher is the UI on the console. All skins currently require ssh access to the Pi, which is beyond the scope of this page. Please see [this](https://forum.clockworkpi.com/t/how-to-transfer-files-with-tinycloud-through-ssh/833) forum post for instructions on how to ssh into your console.

Installation of any skin found on this page, should be pretty easy, if git is installed. 

_please note, I changed the way skins are installed below. Instead oc moving the skin directory to the skins directory, I decided to link it; this should help if/when a skin gets updated._

### Install Git
```
sudo apt-get install git
```

### Switching Skins
At the time of this writing, this is still a manual process, hopefully the devs fix this soon!
As an example, I'll show the steps the switch the skin from default, to blue (assuming blue is already installed).
Ssh into your console, and make the following changes (one of the other, not both)

#### Manually (with vi)
```
vi /home/cpi/apps/launcher/sys.py/config.py
```
replace SKIN="detault" with SKIN="blue"
(save and quit the file)

#### Automagically (with sed)
The quick way, if your impatient, or not a vi fan:
```
sed -i 's/SKIN="default"/SKIN="blue"/' /home/cpi/apps/launcher/sys.py/config.py
```
### Reboot
reboot the console
```
sudo reboot
```

# Blue
This is my first skin, and was more of a proof-of-concept, to see if the launcher could be skinned. 
<img src="images/blue1.jpg" width="240px"/>
<img src="images/blue2.jpg" width="240px"/>


To install this skin, ssh into your console, and type the following:
```
cd ~/
git clone https://github.com/xstrex/CWP-Skin-Blue.git
ln -s /home/cpi/CWP-Skin-Blue/blue/ /home/cpi/apps/launcher/skin/
```

# Redrum
Second Skin - Took the time to colorize every single image, should look more complete. 
_images coming soon_


To install this skin, ssh into your console, and type the following:
```
cd ~/
git clone https://github.com/xstrex/CWP-Skin-Redrum.git
ln -s /home/cpi/CWP-Skin-Redrum/redrum/ /home/cpi/apps/launcher/skin/
```

_profit!_
