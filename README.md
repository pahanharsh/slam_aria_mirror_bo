[![Slam](https://telegra.ph/file/019996f816db9ed576cff.jpg)](https://t.me/request_ayush)

owner of this repo :- [AYUSH](https://github.com/ayushteke)

contact me :- [AYUSH](https://t.me/request_ayush)

# Slam Mirror Bot
This is a telegram bot writen in python for mirroring files on the internet to our beloved Google Drive.

## Deploying on Heroku
Give Star & Fork this repo, then upload **token.pickle** & **credentials.json** to your forks

to know how to get them click on the  #[ link ](https://github.com/spe4641/test-new#getting-google-oauth-api-credential-file)

after this click on the below button 👇👇👇👇
<p><a href="https://heroku.com/deploy"> <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy to Heroku" /></a></p>

## This the structure of Bot

# 1) 👇👇👇👇👇

[<img src="https://telegra.ph/file/a55cd673bee2b8e23782c.jpg" alt="screenshot"/>](https://t.me/AT_BOTS)

# 2) 👇👇👇👇👇

[<img src="https://telegra.ph/file/1f1f93c4d55d7f6c33fd9.jpg" alt="screenshot"/>](https://t.me/AT_BOTS)


# 3) 👇👇👇👇👇

[<img src="https://telegra.ph/file/e886a4c116ff6c47bcdfa.jpg" alt="screenshot"/>](https://t.me/AT_BOTS)


## Features supported:

- Mirroring direct download links to Google Drive
- Mirroring Mega.nz links to Google Drive (In development stage)
- Mirroring Uptobox.com links to Google Drive (Uptobox account must be premium)
- Copy files from someone's drive to your drive (Using Autorclone)
- Download/upload progress, speeds and ETAs
- Docker support
- Uploading To Team Drives.
- Index Link support
- Service account support
- Mirror all youtube-dl supported links
- Mirror telegram files
- Delete files from drive
- Add stickers to your pack
- Check Heroku dynos stats
- Nyaa.si and Sukebei Torrent search
- Shell and Executor
- Shortener support
- Custom Buttons
- Custom Filename (Only for url, telegram files and ytdl. Not for mega links and magnet/torrents)
- Speedtest with picture results
- Extracting password protected files and using custom filename see these examples:
- [custom file name examples ](https://telegra.ph/Magneto-Python-Aria---Custom-Filename-Examples-01-20)
- Bot can extract the following types of files
```
ZIP, RAR, TAR, 7z, ISO, WIM, CAB, GZIP, BZIP2, 
APM, ARJ, CHM, CPIO, CramFS, DEB, DMG, FAT, 
HFS, LZH, LZMA, LZMA2, MBR, MSI, MSLZ, NSIS, 
NTFS, RPM, SquashFS, UDF, VHD, XAR, Z.
```

</details>

## How to deploy on vps ?
Deploying is pretty much straight forward and is divided into several steps as follows:

## Installing requirements

- Clone this repo:
```
git clone https://github.com/ayushteke/slam_aria_mirror_bot_HEROKU/
cd slam_aria_mirror_bot_HEROKU
```

- Install requirements
For Debian based distros
```
sudo apt install python3
sudo snap install docker 
```
- For Arch and it's derivatives:
```
sudo pacman -S docker python
```

## Setting up config file
<details>
    <summary><b>Click here for more details</b></summary>

```
cp config_sample.env config.env
```
- Remove the first line saying:
```
_____REMOVE_THIS_LINE_____=True
```
Fill up rest of the fields. Meaning of each fields are discussed below:
- **BOT_TOKEN**: The telegram bot token that you get from [@BotFather](https://t.me/BotFather)
- **GDRIVE_FOLDER_ID**: This is the folder ID of the Google Drive Folder to which you want to upload all the mirrors.
- **DOWNLOAD_DIR**: The path to the local folder where the downloads should be downloaded to
- **DOWNLOAD_STATUS_UPDATE_INTERVAL**: A short interval of time in seconds after which the Mirror progress message is updated. (I recommend to keep it 5 seconds at least)  
- **OWNER_ID**: The Telegram user ID (not username) of the owner of the bot
- **AUTHORIZED_CHATS**: Fill user_id and chat_id of you want to authorize.
- **AUTO_DELETE_MESSAGE_DURATION**: Interval of time (in seconds), after which the bot deletes it's message (and command message) which is expected to be viewed instantly. Note: Set to -1 to never automatically delete messages
- **IS_TEAM_DRIVE**: (Optional field) Set to `True` if GDRIVE_FOLDER_ID is from a Team Drive else False or Leave it empty.
- **USE_SERVICE_ACCOUNTS**: (Optional field) (Leave empty if unsure) Whether to use service accounts or not. For this to work see "Using service accounts" section below.
- **INDEX_URL**: (Optional field) Refer to https://github.com/maple3142/GDIndex/ The URL should not have any trailing '/'
- **API_KEY**: This is to authenticate to your telegram account for downloading Telegram files. You can get this from https://my.telegram.org DO NOT put this in quotes.
- **API_HASH**: This is to authenticate to your telegram account for downloading Telegram files. You can get this from https://my.telegram.org
- **USE_TELEGRAPH**: Set to `true` to use Telegra.ph for search results from /list bot command, or else set to `false`.
- **MEGA_API_KEY**: Mega.nz api key to mirror mega.nz links. Get it from [Mega SDK Page](https://mega.nz/sdk)
- **MEGA_EMAIL_ID**: Your email id you used to sign up on mega.nz for using premium accounts (Leave th)
- **MEGA_PASSWORD**: Your password for your mega.nz account 
- **STOP_DUPLICATE_MIRROR**: (Optional field) (Leave empty if unsure) if this field is set to `True` , bot will check file in drive, if it is present in drive, downloading will ne stopped. (Note - File will be checked using filename, not using filehash, so this feature is not perfect yet)
- **BLOCK_MEGA_FOLDER**: (Optional field) If you want to remove mega.nz folder support, set it to `True`.
- **BLOCK_MEGA_LINKS**: (Optional field) If you want to remove mega.nz mirror support (bcoz it's too much buggy and unstable), set it to `True`.
- **UPTOBOX_TOKEN**: Uptobox token to mirror uptobox links. Get it from [Uptobox Premium Account](https://uptobox.com/my_account).
- **SHORTENER_API**: Fill your shortener api key if you are using shortener.
- **SHORTENER**: (Optional field) if you want to use shortener in Gdrive and index link, fill shotener url here. Examples:
```
exe.io
gplinks.in
shrinkme.io
urlshortx.com
shortzon.com
```

**Note**: Above are the supported url shorteners. Except these only some url shorteners are supported. If you want to use any other url shortener then first ask me that shortener is supported or not.

</details>

## Getting Google OAuth API credential file

- Visit the [Google Cloud Console](https://console.developers.google.com/apis/credentials)
- Go to the OAuth Consent tab, fill it, and save.
- Go to the Credentials tab and click Create Credentials -> OAuth Client ID
- Choose Desktop and Create.
- Use the download button to download your credentials.
- Move that file to the root of mirrorbot, and rename it to credentials.json
- Visit [Google API page](https://console.developers.google.com/apis/library)
- Search for Drive and enable it if it is disabled
- Finally, run the script to generate **token.pickle** file for Google Drive:
```
pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib
python3 generate_drive_token.py
```

## Deploying on vps

- Start docker daemon (skip if already running):
```
sudo dockerd
```
- Build Docker image:
```
sudo docker build . -t mirrorbot
```
- Run the image:
```
sudo docker run mirrorbot
```


## Bot commands to be set in [@BotFather](https://t.me/BotFather)

```
mirror - Start Mirroring
tar - Upload tar (zipped) file
unzip - Extract files
clone - copy file/folder to drive
watch - mirror YT-DL support link
tarwatch - mirror youtube playlist link as tar
cancel - Cancel a task
cnlall - Cancel all tasks
del - Delete file from Drive
list - [query] searches files in G-Drive
status - Get Mirror Status message
stat - Bot Usage Stats
hlp - Get Detailed Help
speedtest - Check Speed of the host
log - Bot Log [owner only]
repo - Get the bot repo
```
## some of the commands are changed because the group members use them without any reason 


## Using service accounts for uploading to avoid user rate limit
For Service Account to work, you must set **USE_SERVICE_ACCOUNTS="True"** in config file or environment variables
Many thanks to [AutoRClone](https://github.com/xyou365/AutoRclone) for the scripts
**NOTE**: Using service accounts is only recommended while uploading to a team drive.

## Generate service accounts. [What is service account](https://cloud.google.com/iam/docs/service-accounts)

Let us create only the service accounts that we need. 
**Warning**: abuse of this feature is not the aim of this project and we do **NOT** recommend that you make a lot of projects, just one project and 100 sa allow you plenty of use, its also possible that over abuse might get your projects banned by google. 

```
Note: 1 service account can copy around 750gb a day, 1 project can make 100 service accounts so that's 75tb a day, for most users this should easily suffice. 
```

`python3 gen_sa_accounts.py --quick-setup 1 --new-only`

A folder named accounts will be created which will contain keys for the service accounts

**NOTE**: If you have created SAs in past from this script, you can also just re download the keys by running:
```
python3 gen_sa_accounts.py --download-keys project_id
```

## Add all the service accounts to the Team Drive
- Run:
```
python3 add_to_team_drive.py -d SharedTeamDriveSrcID
```

## Youtube-dl authentication using .netrc file
For using your premium accounts in youtube-dl, edit the [.netrc](https://github.com/breakdowns/slam-mirrorbot/blob/master/.netrc) file according to following format:
```
machine host login username password my_youtube_password
```
where host is the name of extractor (eg. youtube, twitch). Multiple accounts of different hosts can be added each separated by a new line

## Credits

Thanks to:
- [out386](https://github.com/out386) heavily inspired from telegram bot which is written in JS
- [Izzy12](https://github.com/lzzy12/) for original repo
- [Dank-del](https://github.com/Dank-del/) for base repo
- [magneto261290](https://github.com/magneto261290/) for some features
- [SVR666](https://github.com/SVR666/) for some fixes
- [4amparaboy](https://github.com/4amparaboy/) for some help
- [WinTenDev](https://github.com/WinTenDev/) for Uptobox support
- [iamLiquidX](https://github.com/iamLiquidX/) for Speedtest module
- [ydner](https://github.com/ydner/) for Usage module
- [breakdowns](https://github.com/breakdowns) idk


and many more people who aren't mentioned here, but may be found in [Contributors](https://github.com/breakdowns/slam-mirrorbot/graphs/contributors).
