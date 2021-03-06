[![Maintainability](https://api.codeclimate.com/v1/badges/2f38b21c193d33baed6d/maintainability)](https://codeclimate.com/github/sapumar/dailybot/maintainability)

# Daily Bot

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)


This is a simple bot to remind Telegram groups about it's daily standup. It runs
from monday to friday, but can run on different days too if you'd like.

## Setting up

I'm assuming you already have Python 3.6 and a bot token 
(if you don't, here's a good [link](https://www.siteguarding.com/en/how-to-get-telegram-bot-api-token))

Firstly, you have to set the following variables to your environment: 
- `NAME` - the bot's name;
- `TOKEN` - the bot's token;
- `CHAT_ID` - the chat with which the bot will send the daily messages
- `HOUR` - the hour that the bot will send the daily message
- `MINUTE` - the minute of the hour mentioned above that the bot will send the daily message
- `PORT` - only used if you're using `ngrok` or `Heroku` (and Heroku fills this variable automatically) 

Now, you might be asking, how do I set variables? Well, it's a simple command (for linux, of course),
see below for `CHAT_ID`.

```commandline
export CHAT_ID=-98364829374
```

After you set all variables, create a virtual environment (or not) and install all dependencies with

```commandline
pip install -r requirements.txt
```

And run the bot script

```commandline
python dailybot.py
```
