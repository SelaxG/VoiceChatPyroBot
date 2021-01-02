# Pyrogram bot to automate streaming music in voice chats

## Help
If you face an error, want to discuss this project or get support for it, join [@su_Chats](https://t.me/su_Chats) on Telegram.

## Requirements
* A computer (Linux VPS recommmended).
* A Telegram account
* Bot token from [@BotFather](https://t.me/BotFather).
* API ID & hash from [my.telegram.org](https://my.telegram.org).
* Python3 & pip3.

## Deploying

### The code

#### Cloning
```
    git clone https://github.com/suprojects/VoiceChatPyroBot.git tgvcbot && cd tgvcbot
```

#### Configuring

Copy `sample_config.py` to `config.py` and make it use your credentials:

`API_ID` int: your api id from [my.telegram.org](https://my.telegram.org)

`API_HASH` str: your api hash from [my.telegram.org](https://my.telegram.org)

`TOKEN` str: your bot token from [@BotFather](https://t.me/BotFather)

`SUDO_USERS` list(int): a list of user ids which can pause, skip and change volume

`LOG_GROUP` int: (optional) a group chat id to send "now playing" messages to in a non-spammy way
    
`LANG` str: your bot language, choose an available language code in [strings/](https://github.com/suprojects/VoiceChatPyroBot/tree/main/strings)
    
`DUR_LIMIT` int: max video duration in minutes for downloads

#### PIP requirements
```
    pip(3) install -U -r requirements.txt
```

### Running

⚠️ Warning for Linux users: don't run any command as root (except those which require it), else you'll face bulky pulseaudio problems. You can create a user with `adduser`.

#### On Linux VPS

These are apt package manager instructions but you can install the required packages with other package managers too.

1. Update and upgrade apt:
```
    sudo apt update && sudo apt upgrade
```

2. Install requirements:
```
    sudo apt install xrdp pulseaudio mplayer screen
```

3. Download tdesktop:
```
    cd ~ && wget https://telegram.org/dl/desktop/linux -O tdesktop.tar.xz && tar -xf *xz && rm -r *xz
```

4. Configure XRDP session to only start Telegram:
```
    echo "./Telegram/Telegram" >~/.xsession
```

5. Go back to directory of the clone and load a pulseaudio null sink, by running:
```
    bash pa.sh
```

6. Make a screen for the bot and attach to it:
```
    screen -S vcbot
```

7. Run the bot:
```
   python(3) bot.py
```

8. Detattach from the screen by pressing CTRL+A then CTRL+D.

9. Open a remote desktop client and login to your user.

10. You should see the Telegram GUI, just login, join a voice chat and set `MySink.monitor` as your microphone.

11. Done, you can now start sending commands to your bot and it'll stream in the voice chat.

## Usage

#### Method 1

1. Open [YouTube]( "https://youtube.com") in your browser, and search for a song.
2. Copy the complete video URL to clipboard and send it to your bot in private.


#### Method 2

1. Enable inline for you bot in  [@BotFather](https://t.me/BotFather).
2. In your bot's private, type @usernameOfYourBot followed by your YouTube search query, and click a result.


## Bot Commands
#### Inorder to command the bot send the below mentioned command with  **/**  prefix


* `start`  - start the bot

* `song`   - check the playing song

* `volume` - check the current volume

* `queue`  - check songs in the queue

* `pause`  - pause the playing song (Sudo Users)

* `resume` - resume the paused song (Sudo Users)

* `play` - same as resume (Sudo Users)

* `ban` - ban a user (Sudo Users)

* `unban` - unban a user (Sudo Users)

* `bans` - see banned users (Sudo Users)

* `skip` - skip the playing song (Sudo Users) 

* `stream` - stream a radio (Sudo Users)

* `cleardownloads` - delete all downloads (Sudo Users)


## Features

1. Download, queue and play videos from YouTube.
2. Stream any internet radio.
3. Ban and unban users from using the bot.

## TODOS

1. Migrate to proper Database like SQLite for storing media queue and user requests.
2. Fix issue related to displaying duration.
3. Keep track of previous and completed media requests.

## Authors & Acknowledgment

### Inspiration
* [@AndrewLaneX](https://github.com/AndrewLaneX) ([Telegram](https://t.me/TwitFace))

### Development & contribution
* [@rojserbest](https://github.com/rojserbest) ([Telegram](https://t.me/su_Theta))
* [@iiiiii1wepfj](https://github.com/iiiiii1wepfj) ([Telegram](https://t.me/itayki))
* [@ByteOPCode](https://github.com/ByteOPCode) ([Telegram](https://t.me/BAZINGA))
* [@pokurt](https://github.com/pokurt) ([Telegram](https://t.me/DeprecatedUser))
* [@SpEcHiDe](https://github.com/SpEcHiDe) ([Telegram](https://t.me/SpEcHIDe))
* [@sudoAlphaX](https://github.com/sudoAlphaX) ([Telegram](https://t.me/su_Alpha))
* [@zomenaro](https://github.com/zomenaro)
* [@subinps](https://github.com/subinps)
* [@NicolaSmaniotto](https://github.com/NicolaSmaniotto)
* [@sppidy](https://github.com/sppidy)

## License
