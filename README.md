Telegram flexible notifications script for check_mk
===

Get a telegram boot
===

* Talk with @botfather

```
@You:
  /newbot
@BotFather
  Alright, a new bot. How are we going to call it? Please choose a name for your bot.
@You
  My notification bot
@BotFather
    Good. Now let's choose a username for your bot. It must end in `bot`. Like this, for example: TetrisBot or tetris_bot.
@You
  mynotificationbot
@BotFather
    Done! Congratulations on your new bot. You will find it at t.me/csaludnotificacionesbot. You can now add a description, about section and profile picture for your bot, see /help for a list of commands. By the way, when you've finished creating your cool bot, ping our Bot Support if you want a better username for it. Just make sure the bot is fully operational before you do this.

Use this token to access the HTTP API:
000000000:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

For a description of the Bot API, see this page: https://core.telegram.org/bots/api
```

* Now you can talk with @mynotificationbot or add to any group

* Get your convestation id.

* Execute this command:

```bash
curl -s -X POST https://api.telegram.org/bot000000000:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/getUpdates | jq .
```

* Response

```json
{
  "ok": true,
  "result": [
    {
      "update_id": 000000000,
      "message": {
        "message_id": 0,
        "from": {
          "id": 0,
          "first_name": "Your",
          "last_name": "Name"
        },
        "chat": {
          "id": -999999999,
          "title": "Your group name",
          "type": "group",
          "all_members_are_administrators": true
        },
        "date": 1488626440,
        "group_chat_created": true
      }
    }
  ]
}
```

* Configure your check_mk flexible notifications

Use this guide [Mathias Kettner - Flexible notifications doc] (https://mathias-kettner.de/checkmk_flexible_notifications.html), and add your bot token (000000000:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx) like the first plugin argument and chat_id (-999999999) like the second.

* Enjoy!

Thanks
===

¡Ese torres!

About
===

Bau Mesa [https://github.com/hidupcloud](https://github.com/hidupcloud)
