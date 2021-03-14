# notify-line-dev-news
[LINE Developer news] 

If there is a new post, it will be sent as a line message.

## Setup

(https://notify-bot.line.me/my/)

```bash
$ pip install -r requirements.txt
$ cp .env.sample .env
```

## Step1

(Log in to LINE at https://notify-bot.line.me/my/) and select the talk room you want to notify and issue a token.

Created with Setup.Write tokens in NOTIFY_TOKEN in env.  

Change 'DB_FILE_PATH' when you want to change the database name.

```bash
DB_FILE_PATH="news.sqlite"
NOTIFY_TOKEN="iEET2ScqVhKrt45ZTXXXXXXXXXXXX"
```

## Step2

Practice

```bash
$ python3 notice.py
```

## a predominant idea

Since the first run does not have data in the previous database, there are many consecutive notifications.

Because of this, 'NOTIFY_SPAN' is installed on './news_notify/news/config.py'.

Changing this value allows notifications to be made in seconds specified.

```python
NOTIFY_SPAN = 0
```
