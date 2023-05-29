<p align="center">
  <img src="images/logo.png"> <br>
  <b>:fire: Control your :penguin: Linux machine with Telegram bot.</b> <br>
</p>
  
## :herb: Functions:
- [x] Desktop Screenshot
- [x] Webcam Screenshot/Video
- [x] Microphone Recorder
- [x] Keylogger
- [x] Geolocation based on IP/BSSID
- [x] Filemanager
- [x] Taskmanager
- [x] Remote Shell
- [x] Remote keyboard
- [x] Power control (shutdown, restart, suspend, logoff)
- [x] Volume control
- [x] Wipe user data (browsers history, passwords, cookies...)
- [x] Rights management using authorization tokens 

## :hammer: Installation:

 * Arch based: `sudo pacman -S python3 python3-pip amixer portaudio xdotool --noconfirm`
 * Debian based: `sudo apt install python3 python3-pip amixer portaudio xdotool -y`
 
 ``` bash
 git clone https://github.com/kraloveckey/blaze-rat
 cd blaze-rat/
 pip3 install --user -r requirements.txt
 ```
 ## :gear: Initialization:
 1. You need to save your telegram bot token
   ``` bash
   python3 main.py --InitApiToken 1393978203:AAEIdXztREV2D1KEx3ggvuOn2gSS12bPDLc
   ```
 2. Now you need to create a token by which you will log in to the bot.  
    :bell: _Token with full access:_
    ``` bash
    python3 main.py --TokenCreate --name root --perms "*"
    ... Created new token '681fb124-9009-4a9b-964d-030c55c274b7', with permissions: *
    ```
    :no_bell: _Limited access token:_
    ``` bash
    python3 main.py --TokenCreate --name observer --perms SCREENSHOT WEBCAMERA KEYLOGGER LOCATION
    ... Created new token '52eff873-9c14-4c2b-8729-b2c6367925b7', with permissions: SCREENSHOT, WEBCAMERA, KEYLOGGER, LOCATION
    ```
 3. Add to startup
   ``` bash
   python3 main.py --InstallAgent
   ```