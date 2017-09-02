# pastehunter
Just some pastebin things

## PreReqs

You need a Pro account on pastebin that has access to the scraping API.
https://pastebin.com/api_scraping_faq

## Install.

# Elastic Search
https://www.elastic.co/guide/en/elasticsearch/reference/current/deb.html

# Kibana
https://www.elastic.co/guide/en/kibana/current/deb.html

# This little app
git clone https://github.com/kevthehermit/pastehunter

## Configure

copy settings.conf.sample to settings.conf
populate the details.
For the scraping API you need to whitelist your IP on pastebin. No API key is required. See the link above

I set a cronjob to run this script every two minutes with a pastelimit of 200

```
localadmin@pastebin:~/pastehunter$ cat /etc/cron.d/pastehunter
# Run every 5 minutes
*/2 * * * *   localadmin  cd /home/localadmin/pastehunter && python3 pastabean.py >> /home/localadmin/pastehunter/cronlog.txt
localadmin@pastebin:~/pastehunter$
```