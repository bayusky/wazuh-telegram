# wazuh-telegram
Send wazuh alert to telegram by telegram bot.

1. First requirement is you should have working Telegram bot with **API KEY** and **CHAT ID** and also fully working Wazuh server.

2. Check reqirements with this command :
```
#pip install requests
```

3. Insert your **CHAT ID** to **custom-telegram.py**. Copy **custom-telegram** and **custom-telegram.py** to **/var/ossec/integrations/**

4. Set correct permission to those files:
```
#chown root:wazuh /var/ossec/integrations/custom-telegram*
#chmod 750 /var/ossec/integrations/custom-telegram*
```

5. Insert your API KEY to these line and copy those lines to **/var/ossec/etc/ossec.conf**
```
    <integration>
        <name>custom-telegram</name>
        <level>3</level>
        <hook_url>https://api.telegram.org/bot<API_KEY>/sendMessage</hook_url>
        <alert_format>json</alert_format>
    </integration>
```
6. Restart wazuh server
```
#systemctl restart wazuh-manager
```
