Lending bot SOP

1. regsister GCP "f1" "linux debian" free project(us west1b)(https://cloud.google.com/free?hl=zh-tw)
2. install pip
3. git clone this
4. edit default.config ,or ref default.config_diotemp
5. use "supervisor" to keep program alive (https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/362881/)
6. sudo mkdir /etc/supervisor.d
7. sudo vi test.conf ,or ref test.conf_diotemp
-----------------------------------------------
(option) auto push message by Telegram
8.new bot by "BotFather" (https://markteaching.com/create-telegram-bot/),get telegram_bot_id and telegram_chat_ids

'''Modify default.config'''
telegram = True
telegram_bot_id = 13xxxxxx36:AAxxxxa-rbDvxxxdkdv_TT_LYNxxxxxxfE
telegram_chat_ids = 11xxxxx79
''''''
