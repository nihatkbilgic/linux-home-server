# SSH and Firewall Configuration

## Firewall

Rocky Linux üzerinde firewalld kullanıldı.

Firewall durumu kontrol edildi:

sudo firewall-cmd --state

Firewall aktif olarak çalışmaktadır.

İzin verilen servisler kontrol edildi:

sudo firewall-cmd --list-services

HTTP (http) ve SSH (ssh) servisleri firewall üzerinde izinlidir.

## SSH

Sunucuya uzaktan bağlantı için SSH kullanıldı.

SSH anahtarı ile bağlantı yapılandırıldı.

SSH güvenlik ayarları kontrol edildi:

sudo sshd -T | grep -E '^(passwordauthentication|permitrootlogin|pubkeyauthentication)'

Sonuç:

- PermitRootLogin no — root ile doğrudan SSH girişi kapalıdır.
- PubkeyAuthentication yes — SSH anahtarıyla giriş aktiftir.
- PasswordAuthentication no — SSH parolasıyla giriş kapalıdır.
