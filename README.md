# FalconPunchBot

FalconPunchBot is a personal Discord sound bot using [Discord.js](https://discord.js.org/) that is primarily for playing short sound clips to voice channels.
I have only tested the bot on Windows, but should work on any OS. 

## Features
Currently supports:
* Multiple Servers: Able to support multiple servers at the same time.
* Clip queuing: After the first clip finishes, the next clip queued will play in the appropriate channel.
* Alias support: Add aliases to your sound clips to give them more memorable commands.
* Search: Search for clips based on description or filename.
* Tracking: Tracks the most played clips from the bot. 

## Prerequisites
* Node v10 or later
* Python 2.7 and C++ compiler for `node-gyp` (for Windows: install Microsoft Build Tools 2015 includes necessary dependencies)

## Installation and Configuration
This is a personal bot for my own uses, but if you want to try it out:
* From command line, run `npm install`
* Open `config.json.example` in a text editor and edit the `admin` and `token` field with your user ID ex.(123456789012345678) and your bot's secret token.
* Rename `config.json.example` to `config.json`
* Take note of `soundDirectory`: Change it if you wish, then create the folder. For example if you have `"soundDirectory": "../clips/",` then create a clips folder in the root directory.
* 'deleteAfterSound' set to true if you want the bot to delete the message after it plays the sound from the soundpack!
* Add your sounds to the directory!
* Run the bot once, it should state the files added and "Bot Started!" if it works!
* You can update aliases or descriptions using the commands -alias add "*alias*" "*filename*", -alias remove "*alias*", -description "*description*" "*filename*"
* If you wish to change the descriptions or add aliases through the soundDB file, use a SQLite DB viewer such as [DB Browser for SQLite](https://sqlitebrowser.org/). Go to "sounds" table and edit the description columns or go to the "alias" table and add a new row with the new alias with filename.
* If you wish to change the descriptions through an update text file, see `update.txt.example`, an example line would be `joe,mp3,this is joe saying hi`

## Running the bot
* From the root directory run `npm start`

## License
This project is licensed under the MIT License - see the LICENSE.md file for details


