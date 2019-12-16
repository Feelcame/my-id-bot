# Bot to get users/chats IDs in Telegram

Demo: [@my_id_bot in Telegram](https://t.me/my_id_bot).  

This is a simple bot written with [aiogram](https://github.com/aiogram/aiogram) framework to show some IDs, like:

* Your user ID (when asked in inline mode or in private chat with any message);  
* Group/supergroup ID (when added to that group or with /id command);  
* Channel ID (when message forwarded from channel to one-to-one chat with bot);  
* Group to supergroup migrate information (both old and new ID).

#### Requirements:
* Python 3.7 and above;  
* Linux (should work on Windows, but not tested);   
* Systemd init system (not necessary).

#### Installation:  
1. Create a directory for bot: `mkdir my-id-bot`;  
2. `cd my-id-bot && python3 -m venv venv`;  
3. Put `bot.py` file to `my-id-bot` directory;  
4. `source venv/bin/python && pip install aiogram`;  
5. `chmod +x bot.py`;  
6. `BOT_TOKEN=yourtoken ./bot.py`

If you want systemd support for autostart and other tasks: open `my-id-bot.service` file, change relevant options to match yours, enter correct token.  
Now copy that file to `/etc/systemd/system` enable it with `systemctl enable my-id-bot.service` and run it: `systemctl restart my-id-bot.service`. Easy!

 

