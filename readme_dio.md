# Lending bot SOP author(DioLin)

1. regsister GCP "f1" "linux debian" free project(us west1b)(ref https://cloud.google.com/free?hl=zh-tw)
2. install pip (python2)
 - 2.1 sudo apt update
 - 2.2 sudo apt install python-pip
3. git clone https://github.com/DioLin/MikaLendingBot.git
 - 3.1 pip install -r requirements.txt
4. edit default.config ,or ref default.config_diotemp (detail in https://poloniexlendingbot.readthedocs.io/en/latest/configuration.html#)
 - 4.1 rename default.config_diotemp to default.config.
 - 4.2 vim default.config,instead of your "apikey" and "secret" copied form bitfinex APIKEY.
5. In order to keep program alive , we suggest use "supervisor"(ref https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/362881/)
 - 5.1 echo_supervisord_conf | sudo tee /etc/supervisord.conf
 - 5.2 sudo vim /etc/supervisord.conf 
              un-mark [include]
              <pre>
              files = /etc/supervisor.d/*.conf</pre>
 - 5.3 sudo mkdir /etc/supervisor.d
 - 5.4 sudo vi test.conf ,or ref test.conf_diotemp
 - 5.5 sudo supervisord

## auto push message by Telegram(option)

6.new bot by "BotFather" (https://markteaching.com/create-telegram-bot/),get telegram_bot_id and telegram_chat_ids

Modify default.config
<pre>
telegram = True
telegram_bot_id = 13xxxxxx36:AAxxxxa-rbDvxxxdkdv_TT_LYNxxxxxxfE
telegram_chat_ids = 11xxxxx79
</pre>
 - 6.1 id "telegram_chat_ids" can be gained from botchat history (enter https://api.telegram.org/bot{$token}/getUpdates in your browser).



## The end,have fun :). BTW you can find your lending log in /www/botlog.json.
<img src="https://sls.weco.net/files/u2045/999.jpg">

