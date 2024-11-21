# CLAYTON MINING BOT

![clayton](assets/img1.png)

Clayton Bot is an automated tool designed to interact with the Clayton Coin platform. It performs various tasks such as daily check-ins, farming, partner tasks, and playing games to earn Clayton Coins (CL) and experience points (XP).

## PREREQUISITE

- Git
- Node JS
- TELEGRAM_APP_ID & TELEGRAM_APP_HASH Get it from [Here](https://my.telegram.org/auth?to=apps) (REQUIRED IF YOU WANT USE SESSIONS)
- Clayton Account , Create [Here](https://t.me/claytoncoinbot/game?startapp=6896240442) join and claim join reward

## BOT FEATURE

- Multi Account With Proxy Support
- Support Telegram Sessions and Telegram Query (Query May Expired)
- Auto Start Farming
- Auto Claim Farming Reward
- Auto Claim Daily Reward
- Auto Play Game
- Auto Complete Missions

## SETUP & CONFIGURE BOT

### LINUX
1. Clone project repository
   ```
   git clone https://github.com/Rambeboy/clayton-bot.git
   ``` 
   and cd to project dir 
   ```
   cd clayton-bot
   ```
2. Install dependencies 
   ```
   npm install 
   sudo apt-get install chromium-browser libx11-xcb1 libxcomposite1 libasound2 libatk1.0-0 libatk-bridge2.0-0 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgbm1 libgcc1 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6
   sudo mkdir -p /opt/google/chrome && sudo ln -s "$(which chromium-browser)" /opt/google/chrome/chrome &&
   ```
   
3. Run
   ```
   npm i telegram@2.22.2
   ```

4. Make new folder 
   ```
   mkdir -p accounts && mkdir -p app/config
   ```
5.  Configure all folder
   ```
   cp config/config_tmp.js config/config.js && cp config/proxy_list_tmp.js config/proxy_list.js
   ```

6. (If You Use Telegram Sessions) To configure the app, run 
   ```
   nano config/config.js
   ```
   and add your telegram app id and hash there.
7. (If You Use Proxy) To configure the Proxy, run 
   ```
   nano config/proxy_list.js
   ``` 
   and add your proxy list there, it currently only support https proxy.

8. To start the app run 
   ```
   npm run start
   ```
   
### WINDOWS

1. Open your `Command Prompt` or `Power Shell`.

2. Clone project repository
   ```
   git clone https://github.com/Rambeboy/clayton-bot.git
   ``` 
   and cd to project dir 
   ```
   cd clayton-bot
   ```
3. Install dependencies
   ```
   npm install && npm i telegram@2.22.2
   ```

5. Navigate to `clayton-bot` directory. 

6. Make new folder named `accounts`.

7. Navigate to `config` folder and rename `config_tmp.js` to `config.js` , `proxy_list_tmp.js` to `proxy_list.js`

8. Now Open and configure `config.js` and `pxoxy_list.js`.

9.  Now back to the `clayton-bot` folder

10. To start the app open your `Command Prompt` or `Power Shell` again and run 
    ```
    npm run start
    ```

## UPDATE BOT

To update bot follow this step :
1. Run 
   ```
   git pull
   ```` 
   or 
   ```
   git pull --rebase
   ``` 
   if error run 
   ```
   git stash && git pull
   ```
2. Run 
   ```
   npm update
   ```
3. Start the bot.

## SETUP ACCOUNTS

1. Run bot `npm run start`

2. Choose option `1` to create account

3. Choose account type `Query` or `Sessions`

4. `Session` Type
- Enter Account Name
- Enter your phone number starting with countrycode ex : `+628xxxxxxxx`
- You will be asked for verification code and password (if any)
- Start The bot Again after account creation complete

5. `Query` Type
- Enter Account Name
- Enter Telegram Query (you can get query by opening bot app on browser > inspect element > storage / application > session storage > telegram init params > copy tg web app data value)
- Start The bot Again after account creation complete

6. After bot started choose option `3` start bot
   

## SESSION TROUBLESHOOT
If you asked to enter phone number again after sessions creation, it mean session not initialized correctly, try to delete the created sessions. 

Example Case
- example you already have 1 session (sessionA) and all good when you run bot. After that you create another session, but when you run bot, the bot asked to enter phone number again, so the problem is on (sessionB), to fix it just remove the `accounts/sessionB` folder and re create it or just delete all folder inside `accounts` directory with prefix `sessions-`.

## QUERY TROUBLESHOOT
if your bot get eror, with some error code `401` it mean your query expired, go get new query and run bot again and choose option `4` for query modification. 

## NOTE

Don't use bot with `session` type if you using telegram account that bought from someone because it can make your telegram account deleted. instead of using `session` type, use `query` type.

This bot can use Telegram Query and Telegram Sessions. if you want to use sessions, and ever use one of my bot that use telegram sessions, you can just copy the `accounts` folder to this bot. Also for the telegram APP ID and Hash you can use it from another bot. If you want to use Telegram Query, get your query manually.

if you got error `Invalid ConstructorId` try to run this ```npm i telegram@2.22.2```

## LICENSE

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
