# R4venRecon

RavenRecon is a personalized fork of the R4VEN tool, designed as a Proof of Concept (PoC) for cybersecurity learning and showcasing the potential risks of granting permissions to malicious websites. This project retains the original features of R4VEN while introducing customized elements for research and educational purposes.

<h4 align="center"> This tool is for Educational and Research Purposes Only. </h4>

Using this tool, you can find out what information a malicious website can gather about you and your devices and why you shouldn't click on random links or grant permissions like Location to them.

### 🌟 Key Features :

- IP address and geographic location tracking
- Collection of device system information
- Capturing images from the device's camera
- Integration with Discord for data presentation
- User interaction for location permission
- Display of a website through an embedded iframe
- Regular interval-based data collection
- Access to and upload webcam images
- Formatting and presentation of data in Discord messages
- Links to Google Maps and Google Earth based on location
- Error handling for denied location permission
- User feedback and error messages

---
### 📍 Goals:
R4venRecon aims to:
-Enhance understanding of cyber reconnaissance techniques.
-Provide hands-on learning with ethical and legal cybersecurity tools.
-Serve as a personalized project for showcasing technical skills.

---
### 🔑 Key Changes from the Original:

-Improved user interface for a better experience.
-Custom data formatting for easier analysis.
-Enhanced error handling and feedback mechanisms.
-Expanded documentation for transparency and usability.

---

### On the link click

```diff
+ It will automatically fetch the IP address and device information
! If location permission is allowed, it will fetch the exact location of the target.
! If camera permission is allowed, it will capture non-stop from the front camera.
```
### 🚨 Limitations:
- Port Forwarding Required: Ensure external access for mobile browsers.
- Browser Restrictions: Not all browsers (e.g., Safari) support permissions required for GPS or camera access.
- Device Limitations: Requires devices with GPS and camera capabilities.

### IP location VS. GPS location

```diff
- Geographic location based on IP address is NOT accurate,
# Does not provide the location of the target. 
# Instead, it provides the approximate location of the ISP (Internet service provider)
```
```diff
+ GPS fetch almost exact location because it uses longitude and latitude coordinates.
@@ Once location permission is granted @@
# Accurate location information is received to within 20 to 30 meters of the user's location.
# (it's almost the exact location)
```
---

<h4 align="center">
  OS compatibility :
  <br><br>
  <img src="https://img.shields.io/badge/Windows-05122A?style=for-the-badge&logo=windows">
  <img src="https://img.shields.io/badge/Linux-05122A?style=for-the-badge&logo=linux">
  <img src="https://img.shields.io/badge/Android-05122A?style=for-the-badge&logo=android">
  <img src="https://img.shields.io/badge/macOS-05122A?style=for-the-badge&logo=macos">
</h4>

<h4 align="center"> 
Requirements:
<br><br>
<img src="https://img.shields.io/badge/Python-05122A?style=for-the-badge&logo=python">
<img src="https://img.shields.io/badge/Git-05122A?style=for-the-badge&logo=git">
<img src="https://img.shields.io/badge/Discord webhook-05122A?style=for-the-badge&logo=discord">
</h4>

###  🚦 Installation:
---

```
git clone https://github.com/spyboy-productions/r4ven.git
```
```
cd r4ven
```
```
pip3 install -r requirements.txt
```
```
python3 r4ven.py
```

`NOTE:` If you're not going to use `localhost` `(http://127.0.0.1:8000/image)`

Please `modify` [this](https://github.com/spyboy-productions/r4ven/blob/6e5230d309a4a3acf0d7a67a8e3913ccc35f7124/index.html#L203C29-L203C50) line with the `URL` you wish to use.

OR

Please use the `-t` flag to choose a different URL.

Use the following command to make r4ven executable:

```
chmod +x r4ven.py
```
```
python3 r4ven.py [-t target] [-p port]
```

**Example:** `python3 r4ven.py -t https://replit.com/myproject/images -p 8080`

---

```Enter your discord webhook URL (set up a channel in your discord server with webhook integration)```

https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks

`if not have discord account and sever make one, it's free.`

https://discord.com/

---

📍 _Track info data will be sent to your discord webhook channel._

- why discord webhook? Conveniently, you will receive a notification when someone clicks on the link.

---

#### ⭓ To change website template

- open file `index.html` on line 12 and replace the `src` in the iframe. (Note: not every website support iframe)

---

#### ⭓ To port forward install ngrok or use ssh or whatever tool you want to port forward with.

- For ngrok port forward type: ngrok http 8000
- For ssh port forwarding type: ssh -R 80:localhost:8000 ssh.localhost.run

```diff
- Warning: Make sure you port forward else it will not work on the smartphone's browser
```

---

#### Contribution:

Contributions and feature requests are welcome! If you encounter any issues or have ideas for improvement, feel free to open an issue or submit a pull request.

#### 😴🥱😪💤 ToDo:

- port forward directly

- Use trycloudflare to give web URL https://try.cloudflare.com/ https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with- 
  tunnels/trycloudflare/
- or use these https://tunnelmole.com/ https://github.com/robbie-cahill/tunnelmole-service

- Give the option to choose what you want 1. track location 2. camera access 3. just IP and device info 4. all of it
- PHP code to host a website without Python
- Iframe can be warned ..make a phishing template 

#### 💬 If having an issue [Chat here](https://discord.gg/ZChEmMwE8d)
[![Discord Server](https://discord.com/api/guilds/726495265330298973/embed.png)](https://discord.gg/ZChEmMwE8d)


📖 Acknowledgments:
This project is based on the original R4VEN tool by Spyboy. Full credit for the base code and inspiration goes to the original creator.
<p align="center"> <a href="https://twitter.com/spyboyproductions"> <img src="https://img.shields.io/badge/-TWITTER-black?logo=twitter&style=for-the-badge"> </a> &nbsp; <a href="https://spyboy.in/"> <img src="https://img.shields.io/badge/-spyboy.in-black?logo=google&style=for-the-badge"> </a> &nbsp; <a href="https://spyboy.blog/"> <img src="https://img.shields.io/badge/-spyboy.blog-black?logo=wordpress&style=for-the-badge"> </a> &nbsp; <a href="https://discord.com/"> <img src="https://img.shields.io/badge/-Discord-black?logo=discord&style=for-the-badge"> </a> </p> <img width="100%" align="center" src="https://spyboyblog.files.wordpress.com/2022/05/cream-brown-aesthetic-new-product-skincare-canvas-banner-2.png" />
