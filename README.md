# Music Test Bot
  A standalone Discord.JS music bot based on [DarkoPendragon](https://github.com/DarkoPendragon]'s [discord.js-musicbot-addon](https://github.com/DarkoPendragon/discord.js-musicbot-addon) module.
  Some parts of this code is taken from his module (v1.5.1 and v1.10.3)
	Developers: Naz // BluSpring, Damo // CodaEnder
You are allowed to take any piece of code from here into your own music bot :)
You are also allowed to fork this code and edit the code into a module.
Another thing is you are allowed to not credit me (finally doing this for once)
This is open-source code, anyway.
I left some notes for help.

Please join my bot's Discord server here for assistance with the module: [FoozBallKing Bot Official](https://discord.gg/CYVBkej)

# How to use
First off, `cd` into the bot folder (after downloading it) and type `npm i`. This will install all the required modules.
Rename the `d_config.json` file to `config.json`.
Also, please install FFMPEG. Instructions [here](https://github.com/adaptlearning/adapt_authoring/wiki/Installing-FFmpeg)
And also, install either node-opus or opusscript.
`npm i -s node-opus` OR `npm i -s opusscript`



# Configurations

| Option | Type | Required? | Description | Default
| --- | --- | --- | --- | --- |
| token | String | yes | Required for the bot to log in. Get a token from [here](https://twentysix26.github.io/Red-Docs/red_guide_bot_accounts/#creating-a-new-bot-account) | None |
| ytapi3 | String | yes | Required to search for YT videos. How to get one is [here](https://developers.google.com/youtube/v3/getting-started) | None |
| prefix | String | no | Shows what you want your bot to respond to. | ! |
| helpCmd | String | no | What should the help command be. | help |
| playCmd | String | no | What should the play command be. | play |
| pauseCmd | String | no | What should the pause command be. (UNFINISHED) | pause |
| stopCmd | String | no | What should the stop command be. (UNFINISHED) | stop |
| queueCmd | String | no | What should the queue command be. | queue |
| npCmd | String | no | What should the Now Playing command be. | np |
| downloadVid | Boolean | no | If you want to download the video. Make a folder called `audio_temp` so it would put it there. | false |

Also, make sure the commands are done in lowercase, since the code already makes the commands go from uppercase to lowercase.
Basic configuration:
```json
{
	"token": "token",
	"ytapi3": "youtube-api-key"
}
```

Advanced configuration:
```json
{
	"token": "token",
	"ytapi3": "youtube-api-key",
	"prefix": "!",
  "helpCmd": "gitsomehelp",
  "playCmd": "add",
	"pauseCmd": "pass",
	"stopCmd": "stahp",
	"queueCmd": "gimmedaqueue",
	"npCmd": "whatsplaying",
	"downloadVid": true
}
```


__Common installation issues:__  
__Issue: (Trivial)__ FFMPEG was not found on your system.  
__Fix:__ Make sure ffmpeg is installed correctly and set in your PATH variable.  

__Issue: (Uncommon)__ Couldn't find an Opus engine.  
__Fix:__ `npm install node-opus` or `npm install opusscript`  

__Issue: (Rare)__ [NPM] ERR Cannot read property '0' of undefined  
__Fix:__ `npm i -g npm@4.6.1` or another lower version of npm.  

__Issue: (Rare)__ TypeError: Invalid non-string/buffer chunk  
__Fix:__ Stop using `ffmpeg-binaries`. Seriously. It's been said enough to use `ffmpeg` itself by now.

__Issue: (Trivial)__ Any node-gyp errors. (build fail, missing cl.exe, etc.)  
__Fix:__ This one is a little more complicated.  
1. Type `npm i -g --production windows-build-tools`

OR

1. Download and install [Visual Studio 2015](https://www.visualstudio.com/downloads/)  
2. New project -> Visual C++  
3. Install Visual C++  

If that doesn't fix your issue;  
1. Download and install the [Windows 8.1 SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-8-1-sdk)  

__Issue: (Uncommon)__ `ffluent-ffmpeg` errors.
1. Download and install ffmpeg correctly for your OS/env.