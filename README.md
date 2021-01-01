# Pyrogram bot to automate streaming music in voice chats

## Help
If you face an error, want to discuss this project or get support for it, join [@su_Chats](https://t.me/su_Chats).

## Requirements
* A computer running a Linux distribution with a desktop environment (if you are on VPS and don't have one, refer to [this](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/use-remote-desktop)),
* the latest version of Telegram desktop,
* `pulseaudio` (installation on Ubuntu: `apt install pulseaudio`),
* `mplayer` (installation on Ubuntu: `apt install mplayer`),
* `python3` (installation on Ubuntu: `apt install python3`) and
* `python3-pip` (installation on Ubuntu: `apt install python3-pip`) installed on it.

## Running
1. Make sure you are not running any command as root, to avoid bulky errors.
2. Clone the repository and change the dir:
```
    git clone https://github.com/suprojects/VoiceChatPyroBot.git tgvcbot && cd tgvcbot
```
3. Copy `sample_config.py` to `config.py` and make it use your credentials:

    `API_ID` int: your api id from [my.telegram.org](https://my.telegram.org)

    `API_HASH` str: your api hash from [my.telegram.org](https://my.telegram.org)

    `TOKEN` str: your bot token from [@BotFather](https://t.me/BotFather)

    `SUDO_USERS` list(int): a list of user ids which can pause, skip and change volume

    `LOG_GROUP` int: (optional) a group chat id to send "now playing" messages to in a non-spammy way
    
    `LANG` str: your bot language, choose an available language code in [strings/](https://github.com/suprojects/VoiceChatPyroBot/tree/main/strings)
    
    `DUR_LIMIT` int: max video duration in minutes for downloads

4. Install the required Python packages:
```bash
    pip(3) install -U -r requirements.txt
```
5. Make sure pulseaudio is running and load a null sink named `MySink` by running:
```bash
    bash pa.sh
```
6. Run the bot:
```bash
    python(3) bot.py
```
7. Open Telegram desktop, join a voice chat and set `MySink.monitor` as your microphone, if you can't see `MySink.monitor`:
    1. Open pulseaudio volume control (pavucontrol).
    2. The configurations tab.
    3. Turn the configs/profiles you see off.
9. Once you've done the steps above, you can start using and sending commands to your bot to stream in the voice chat you are currently in with Telegram desktop!


## How to use

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
* [@SpEcHIDe](https://github.com/SpEcHIDe) ([Telegram](https://t.me/SpEcHIDe))

## License
