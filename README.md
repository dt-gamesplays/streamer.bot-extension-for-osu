# Streamer.bot extension for osu!
This extension integrates commands that you can use during your osu live streaming. Some commands are useful for the viewer to get extra real-time information about your osu instance, while others are useful for not having to leave Twitch to get information from the osu site.
To learn what the commands are for this extension go to the bottom of the [Commands Description and Usage](https://github.com/dt-gamesplays/streamer.bot-extension-for-osu/tree/main?tab=readme-ov-file#commands-description-and-usage) section.

## Configuration of Streamer.bot
1. Download [Streamer.bot](https://streamer.bot/)
2. In Streamer.bot navigates to `Platforms` > `Twitch` > `Accounts`

   ![sb_configuration](https://i.ibb.co/72FdFFw/Streamer-bot-twitch-login.png)

3. Click the `Login` button in the `Broadcaster Account` section and proceed to enter your Twitch account


## Import the extension into Streamer.bot
1. Download the [extension](https://github.com/dt-gamesplays/streamer.bot-extension-for-osu/releases) (.sb file)
2. In Streamer.bot click the `Import` button in the top menu. Drag the extension file into the `Import String` field.

   ![import_extension](https://i.ibb.co/b2fQqdr/import-extension.png)

3. Click `Import` to finalize the import.
4. Enable commands in the Commands section: right-click on the group `Osu! Info` > `Group` > `Enable all`

   ![enable_commands](https://i.ibb.co/Y49gPW3/Enable-commands.png)


## Get your personal osu key from osu site
> The !best, !recent, !stats, !top commands require the use of an osu key.
1. Go [here](https://osu.ppy.sh/p/api) to the API section of the osu website
2. Go to the bottom of the Legacy API section
3. Click on `new Legacy API key` button
4. In the `application name` field enter `Streamer.bot`
5. In the `application url` field enter `http://localhost`
6. Click on `Create Key` button

   ![osu_api_settings](https://i.ibb.co/WHgHh0x/osu-API-settings.png)

8. Click on `Show Key` button and copy the key


## Enter the osu key in Streamer.bot
1. Go to the !best, !recent, !stats, !top actions and enter in the `value` field of the argument `%osukey%` your osu key

   ![enter_osu_api](https://i.ibb.co/jVGpsrm/Enter-osu-key.png)

2. Click `OK` button to confirm the entry


## Configuration of the !skin command
1. Go to the folder where osu is installed: If you have not changed the installation path of the game press `WIN` + `R`, type `%localappdata%` and press `OK`

   ![WIN+R](https://i.ibb.co/WvQnTFT/win-r-localappdata.png)

2. Open the `osu!` folder and create a folder called `Links`
3. Right-click on the `Links` folder > `Open in a new window`
4. Open the `Skins` folder in the previously opened window
5. Within the `Links` folder you just created, create text files named exactly like the name of the folders found in `Skins` folder

   ![osu Folders](https://i.ibb.co/d5nxTL0/osu-Folders.png)

6. Enter for each text file the link to the corresponding skin. You can upload skins to cloud storage and get the link or use sites like [osuck](https://skins.osuck.net/skins/category/popular?t=1&d=0) and search for your skin. If you use osuck just search for your skin, click on the download link button and then click on the copy short link button


## Install Tosu
> The !acc, !np, !pp, !skin commands require the use Tosu.
1. Download [Tosu](https://github.com/tosuapp/tosu)


## Commands Description and Usage
> For the !acc, !np, !pp, !skin commands to work, you must run Tsou.
In case Tosu is not open when the command is started, no message will be sent. In case the commands should not be used correctly or with invalid data they will not send any chat message.

| **Command**      | **Description**     |      **Usage**              |      **Example** |
|---|---|---|---|
| **!acc** | current map info based on acc. | !acc "n∈[1,100]" | !acc 98
| **!best** | best statistics  | !best "playerName" | !best dt_gamesplays
| **!np** | current map | !np | !np
| **!pp** | acc to get the desired pp | !pp "n∈{pp with 90 ≤ acc ≤ 100} | !pp 600
| **!recent** | the last map played. | !recent "playerName" | !recent dt_gamesplays
| **!skin** | current skin link. | !skin | !skin
| **!stats** | general statistics. | !stats "playerName" | !stats dt_gamesplays
| **!top** | n-th best play. | !top "playerName" "n∈[1,100]"  | !top dt_gamesplays 1
