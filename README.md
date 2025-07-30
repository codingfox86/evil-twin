<img width="35" height="35" alt="" src="https://github.com/user-attachments/assets/cac505b8-347f-4980-b9fd-e8b46e978f4a" />

This is my documentation on how to set up and simulate an Evil Twin attack with a Raspberry Pi for educational purposes.<br>


An Evil Twin attack is a type of Wi-Fi phishing attack where a hacker sets up a rogue access point (AP) that mimics a legitimate wireless network. The goal is to trick users into connecting to the fake AP, allowing the attacker to intercept sensitive information such as login credentials or session cookies.

This project demonstrates how to simulate an Evil Twin attack in a controlled, ethical environment for educational purposes only. By following this guide you will:

-> Understand how Evil Twin attacks work in practice.

-> Learn how to configure a rogue AP using tools like hostapd, dnsmasq, and apache2.

-> Simulate a credential capture scenario using a fake captive portal.

-> Explore ways to detect and mitigate such attacks.

<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0d361d92-3112-4495-b6a3-37212ded082e" /> 
Disclaimer: This project must only be conducted in isolated environments with explicit permission from all participants. Unauthorized deployment of rogue access points is illegal and unethical. 
<img width="20" height="20" alt="image" src="https://github.com/user-attachments/assets/0d361d92-3112-4495-b6a3-37212ded082e" /><br>
______________________________________________________________________<br>
<br><img width="25" height="25" alt="" src="https://github.com/user-attachments/assets/3bdcf782-a450-4031-aee0-b91c42814b19"/>
Objectives <br><br>

Set up a Raspberry Pi or Linux-based system as an Evil Twin.

Create a cloned wireless network to simulate phishing.

Capture credentials using a fake login page.

Log and monitor client connections.

Reflect on defense techniques against such attacks.<br>
______________________________________________________________________<br>
<br><img width="25" height="25" alt="" src="https://github.com/user-attachments/assets/1add1cac-b4d2-403a-acec-073fa03f134b" />
Tools & Environment 

Raspberry Pi or any Linux system (Parrot OS or Kali Linux recommended)

External USB Wi-Fi adapter that supports monitor mode and packet injection

-> Note that you have to get a Wi-Fi adapter that is compatible with your OS. I couldn't get one that works with Kali Linux, otherwise I would recommend using Kali.

Tools: airmon-ng, airodump-ng, hostapd, dnsmasq, iptables, apache2

SSH connection (optional but I always use SSH for easier handling)

HTML/PHP files for a basic captive portal
