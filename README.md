Instalacija

rm -rf install.py && wget https://github.com/iptvbosna/XTREAM-UI-20.04-22.04-24.04/raw/main/install.py && sudo python3 install.py 

Za pokretanje Xtream Codes panela koristite:

sudo systemctl start xtreamcodes

sudo systemctl start xtreamcodes
sudo systemctl restart xtreamcodes
sudo systemctl status xtreamcodes
sudo systemctl stop xtreamcodes
sudo systemctl reload xtreamcodes

Opis naredbe

status	Status the panel
start	Start the panel
stop	Stop the panel
restart	Restart the panel
reload	Reload Nginx konfiguracija


# 2.Ažuriranje XtreamUI Ubuntu20
apt-get install unzip e2fsprogs python3-paramiko -y && chattr -i /home/xtreamcodes/iptv_xtream_codes/GeoLite2.mmdb && rm -rf /home/xtreamcodes/iptv_xtream_codes/admin && rm -rf /home/xtreamcodes/iptv_xtream_codes/pytools && wget "http://sehara.eu:5656/XTREAMUI-20.04-22.04-24.04/update.zip" -O /tmp/update.zip -o /dev/null && unzip /tmp/update.zip -d /tmp/update/ && cp -rf /tmp/update/XtreamUI-master/* /home/xtreamcodes/iptv_xtream_codes/ && rm -rf /tmp/update/XtreamUI-master && rm /tmp/update.zip && rm -rf /tmp/update  && chown -R xtreamcodes:xtreamcodes /home/xtreamcodes/ && chmod +x /home/xtreamcodes/iptv_xtream_codes/permissions.sh && /home/xtreamcodes/iptv_xtream_codes/permissions.sh && find /home/xtreamcodes/ -type d -not \( -name .update -prune \) -exec chmod -R 777 {} + && /home/xtreamcodes/iptv_xtream_codes/start_services.sh && chattr +i /home/xtreamcodes/iptv_xtream_codes/GeoLite2.mmdb
