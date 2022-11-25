# wazuh-telegram
Send wazuh alert to telegram by telegram bot.

First reqirement is you should have working Telegram bot with API KEY and CHAT ID and also fully working Wazuh server.

Check reqirements with this command :

# pip install requests

Insert your chat id to custom-telegram.py. Copy custom-telegram and custom-telegram.py to /var/ossec/integrations/

Set correct permission to those files:

# chown root:wazuh /var/ossec/integrations/custom-telegram*
# chmod 750 /var/ossec/integrations/custom-telegram*

Insert your API KEY to ossec.conf and copy those lines to /var/ossec/etc/ossec.conf
Restart wazuh server

# systemctl restart wazuh-manager
