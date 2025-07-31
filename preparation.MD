<h3>What you need to do before you can start with your rogue AP </h3>

--> Note: Since there were not many available Wi-Fi adapters and none of these compatible with Kali Linux, I've gone with this setup: <br>
    Raspberry Pi 4B with 4GB RAM (including 32GB SD-Card, HDMI adapter and power supply) <br>
    Parrot OS 64bit security version (https://deb.parrot.sh/parrot/iso/6.4/Parrot-security-6.4_rpi.img.xz) <br>
    WiFi-Adapter BrosTrend AC650 <br>
If you're more up for working with Kali Linux, feel free to do so!
<br>
1. Download Raspberry Pi Imager for your OS -> https://www.raspberrypi.com/software/
<br>
2. Install Parrot or Kali on the SD (on your local workstation) for the Raspberry Pi: <br>
    Choose your model, OS and SD-card. Some OS are ready to choose from the imager. If you like your own downloaded OS, you can always choose "own image" in the drop down menu. I recommend modifying the configuration to your home WiFi and if possible, enable SSH.  <br> 
    <br>
3. Put your Raspberry together and start it for the first time! Use a monitor for better view (I connected only via SSH in the beginning and encountered some difficulties that only occured there). <br>
<br>
4. The credentials for the first login are often: <br>
    -user: pi <br>
    -password: raspberrypi<br>
    Or your chosen credentials. You logged in succesfully? Great!<br>
<br>
First thing to do: <i>sudo apt update && sudo apt upgrade</i><br>
If you're not connected to your WiFi:<br>
    - <i>ip addr show</i> -> look for your Pi-internal WiFi (for mine it's wlan0)<br>
    - connect to it -> <i>nmcli device wifi connect "<SSID>" password "<password>" ifname wlan0</i><br>
You'd rather work within the GUI and not only CLI? <br>
Check your default -> <i>sudo systemctl get-default</i><br>
Is it <i>multi-user.target</i>? <br>
Change it! <i>sudo systemctl set-default graphical.target</i> and after <i>sudo reboot</i> it should boot into the GUI.<br>
<br>
Plug your external WiFi Adapter in. Check if youre system recognizes it with: <i>lsusb</i><br>
Install the software!


<b>YOU ARE READY TO GO!</b>