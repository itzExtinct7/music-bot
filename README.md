# Basic discord bot using discord js

## [](#general)General

This is a basic Discord music bot that can play music from YouTube and other sources. It has the basic functionality
of a music bot.

## [](#features)Features

The bot can play music from YouTube, SoundCloud, Apple Music and Spotify and has a queue system. It also has
some commands to
control the music and the bot itself.

## [](#before-starting)Before starting

### [](#prerequisites)Prerequisites

To run the bot, you need to have Node.js installed on your machine. You can download it from the official
[Node.js](https://nodejs.org/en/) website. You also need to have ffmpeg installed on your machine. You can download it
from the official
[ffmpeg website](https://www.ffmpeg.org/download.html).

### [](#setup)Setup

To set up the bot, you need to create a new application on the
[Discord Developer Portal](https://discord.com/developers/applications),
create a `.env` file in the root directory of the project and copy the
token of the bot into this file like this:

```
TOKEN=xxx
```

### [](#developing-and-testing)Developing & testing

For testing, you can change the `testServer` and `devs` properties in `config.json` file to to your test server id and
your developers discord
id's.  
Now you can run the bot with the argument `--test` to start the bot in
development mode, where new commands only get registered on your testServer.  
Pay attention, that the already registered commands will still be available on all servers.

## [](#running)Running the bot

To run the bot, you need to open a terminal in the root directory of the project and run the command
`npm run src/index.js`.

If you want to run the bot in development mode, you can run the command `npm run src/index.js --test`.

If you don't want to develop the bot, you can also run the bot as
a [docker container from docker hub](https://hub.docker.com/r/paulmueser/musicbotdocker)
with the command `docker run -d --env TOKEN=xxx paulmueser/musicbotdocker`.

## [](#commands)Commands

### [](#misc)Misc

- ping - Pong!

### [](#musicControl)Music Control

- play {song} - plays a song
- pause - pauses the music
- resume - resumes the music
- skip - skips the current song
- stop - stops playing music and disconnects from the channel
