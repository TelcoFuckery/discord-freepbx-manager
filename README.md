# FreePBX Manager

[![License](https://img.shields.io/badge/license-GPL--3.0-blue)](https://github.com/ChrisChrome/discord-freepbx-manager/blob/main/LICENSE)

## Description
FreePBX Manager is a Discord bot designed to manage FreePBX configurations. Please note that this project is currently a hot mess and may not be suitable for production use.

## Pre-requisites
- [Node.js](https://nodejs.org/en/download/)
- [FreePBX](https://www.freepbx.org/)
- [A Discord Bot](https://discord.com/developers/applications)

## Features
- [x] User-created extensions
- [x] Automatic extension creation
- [x] Extension deletion
- [x] Extension status
- [x] Extension list

- Probably some more stuff that I forgot to write down lol

## Setup
To set up the config file, follow the steps below:

1. Clone the repository:
   ```shell
   git clone https://github.com/ChrisChrome/discord-freepbx-manager.git

   cd discord-freepbx-manager
   ```
2. Install the required dependencies:
   ```shell
   npm install --save
   ```

3. Create a new file named `config.json` in the root directory of the project and fill it with the following content:
   ```json
   {
	    "ntfyUrl": "ntfy-url",
		"freepbx": {
			"server": "sip-server-ip",
			"url": "pbx-api-url",
			"clientid": "gql-client-id",
			"allowedscopes": "gql",
			"secret": "gql-secret",
			"startExt": 1000
		},
		"discord": {
			"token": "bot-token",
			"guildId": "guild-id",
			"roleId": "user-role",
			"logId": "log-channel",
			"extList": "extension-list-channel",
	        "developers": ["your-user-id"]
		},
		"mariadb": {
			"host": "db-hostname0here",
			"user": "bot",
			"password": "bot",
			"database": "asterisk",
			"connectionLimit": 5
		},
	    "cdrdb": {
			"host": "db-hostname-here",
			"user": "bot",
			"password": "bot",
			"database": "asteriskcdrdb",
			"connectionLimit": 5
		},
		"status": {
			"interval": 60,
			"url": "uptime-kuma-link"
		}
	}
	```
4. Replace the placeholders with your own values:
   - `ntfyUrl`: The URL of the NTFY server.
   - `sip-server-ip`: The IP address of the SIP server.
   - `pbx-api-url`: The URL of the FreePBX API.
   - `gql-client-id`: The client ID for the GraphQL API.
   - `gql-secret`: The secret for the GraphQL API.
   - `bot-token`: The token of the Discord bot.
   - `guild-id`: The ID of the Discord guild.
   - `user-role`: The ID of the role that users must have to use the bot.
   - `log-channel`: The ID of the channel where logs will be sent.
   - `extension-list-channel`: The ID of the channel where the extension list will be sent.
   - `your-user-id`: Your Discord user ID.
   - `db-hostname-here`: The hostname of the MariaDB server.
   - `uptime-kuma-link`: The URL of the Uptime Kuma instance.
5. Run the bot:
   ```shell
   node .
   ```
6. Invite the bot to your Discord server using the following link:
   ```
   https://discord.com/oauth2/authorize?client_id=YOUR_BOT_ID&scope=bot&permissions=8
   ```
7. You're all set! The bot should now be up and running.