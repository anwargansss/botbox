# Android Telegram Bot

Bot Telegram untuk kontrol `/system/bin/sbfr`, dashboard YACD, dan manajemen core (Clash, Xray, Sing-box, V2Fly, Hysteria) di Android.

---

## 📦 Fitur

- `/help`       - Menampilkan bantuan
- `/menu`       - Menampilkan menu utama
- `/import`     - <path> (default: /data/adb/box/)
- `/export`     - <path/file> (default: /data/adb/box/)
- `/log`        - Membaca isi runs.log
- `/sbfr`       - Menu kontrountuk /system/bin/sbfr
- `/yacd`       - Menu kontrodashboard YACD
- `/core`       - Pilih core untuk settings.ini
- `/speedtest`  - Pilih aksi SpeedTest

---

## ⚙️ Instalasi

1. Clone repository:

```bash
git clone <REPO_URL>
cd <REPO_FOLDER>
```

2. Install dependensi Go:

```bash
go mod tidy
```


3. Buat konfigurasi bot di bot.ini:

```ini
[bot]
token = <YOUR_BOT_TOKEN>
owner = <YOUR_TELEGRAM_ID>
mihomo_api = http://192.168.1.1:9090
api_secret = 123456
```

4. Build bot:

```bash
go build -o bot .
```

5. Jalankan bot:

```bash
su -c sh bot -c docs/bot.ini
```
> -c opsional, default bot mencari bot.ini di folder binary.

## Struktur Folder 
```bash
bot/
├── README.md
├── main.go
├── commands.go
├── yacd.go
├── go.mod
├── go.sum
├── docs/
│   ├── bot.ini
│   └── bot.sh
```

