# brevo-sendmail
An alternative to sendmail / MSMTP to send all email via Brevo Mail HTTP API (to avoid SMTP)


# Log Rotation example:

```bash
sudo nano /etc/logrotate.d/brevo-sendmail
```

```bash
/var/log/brevo-sendmail.log {
    su root site-users
    daily
    rotate 7
    compress
    missingok
    notifempty
    create 660 root site-users
}
```

## Debug

```bash
sudo logrotate -d /etc/logrotate.d/brevo-sendmail
```

## Test

```bash
sudo logrotate -f /etc/logrotate.d/brevo-sendmail
```
