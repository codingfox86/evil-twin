Steps:
1. install OS on raspberry pi using rasp. pi imager
(choose pi version - choose os -> own OS - voreinstellungen)
---> sudo apt update && sudo apt upgrade

2. establish ssh connection if you don't have an external display for the pi
-> change ssh keys
-> if necessary modify sshd_config on the pi:
	sudo nano /etc/ssh/sshd_config
	PasswordAuthentication yes
	PermitRootLogin no
	sudo systemctl restart ssh
	ssh-copy-id pi@192.168.x.x
	-> after establishing disable password login
		sudo nano /etc/ssh/sshd_config
		PasswordAuthentication no
		sudo systemctl restart ssh

3. install your wifi-adapter

4. connect to your preferred Wi-Fi (with wlan0):
	list all available wifis: nmcli device wifi list
    connect to preferred wifi: nmcli device wifi connect "<SSID>" password "<password>" ifname wlan0

5. setup your wlan1 as a router:
	check if interface is recognized 
	-> iw dev -> Look for wlan1 and confirm it shows a phy device and managed mode.
	-> iw list -> Supported interface modes:
    * managed
    * AP  <---- without AP it does not work!

   install required tools:
   sudo apt install aircrack-ng hostapd dnsmasq iptables net-tools (parrot and kali should already have these)



/evil-twin/ subdirectories
-configs — for your hostapd config files
-captures — for packet captures or logs you might save
-logs — general logs
-portal — for captive portal files (HTML, PHP, etc.)
-scripts — for bash/python scripts you may write

