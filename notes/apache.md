# Apache Web Server

Apache HTTP Server, Rocky Linux üzerinde kuruldu ve çalıştırıldı.

Servis durumu systemd ile kontrol edildi:

sudo systemctl status httpd

Apache'nin yapılandırması kontrol edildi:

sudo apachectl configtest

Sonuç:

Syntax OK

Apache, HTTP trafiğini 80 numaralı port üzerinden kabul etmektedir.

Yerel HTTP bağlantısı curl ile test edildi:

curl http://localhost

İstek başarıyla işlendi ve HTTP 200 OK yanıtı alındı.

Apache access logunda test isteği görüldü:

GET / HTTP/1.1
HTTP status: 200

Apache erişim logları şu dosyada tutulmaktadır:

/var/log/httpd/access_log
