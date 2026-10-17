# 🛰️ Bettercap Quick Notes

Catatan singkat & cheat sheet pribadi untuk penggunaan [Bettercap](https://www.bettercap.org/) — Swiss army knife untuk network attack, monitoring, dan MITM (Man-in-the-Middle) testing.

> ⚠️ **Disclaimer**
> Catatan ini dibuat untuk tujuan **pembelajaran & pengujian keamanan jaringan pada perangkat/jaringan milik sendiri atau yang sudah mendapat izin resmi (authorized penetration testing)**.
> Penggunaan tools ini pada jaringan orang lain tanpa izin adalah **ilegal** dan menjadi tanggung jawab pengguna sepenuhnya.

---

## 📦 Instalasi Singkat

```bash
sudo apt install bettercap
```

---

## 🚀 Menjalankan Bettercap

```bash
sudo bettercap -iface wlan0
```

Ganti `wlan0` sesuai interface jaringan yang kamu gunakan (`eth0`, `wlan0`, dll). Cek dengan:

```bash
ip a
```

---

## 🔍 Recon & Sniffing

```bash
net.probe on      # Scan device aktif di jaringan
net.recon on       # Ambil info tambahan device
http.proxy on       # Aktifkan HTTP proxy
net.sniff on        # Sniff traffic jaringan
```

---

## 🎯 Set Target Subnet

```bash
set arp.spoof.targets 192.168.1.0/24
```

## 🧪 ARP Spoofing (MITM)

```bash
arp.spoof on
arp.spoof off
```

---

## 📡 Cara Mengetahui Subnet Jaringan

```bash
ip route
```

Contoh output:

```
192.168.1.0/24 dev wlan0
```

Berarti subnet jaringan yang digunakan adalah `192.168.1.0/24`.

---

## 🧠 Ringkasan Perintah

| Perintah | Fungsi |
|---|---|
| `net.probe on` | Scan device aktif di jaringan |
| `net.recon on` | Ambil info tambahan device |
| `http.proxy on` | Aktifkan HTTP proxy |
| `net.sniff on` | Sniff traffic jaringan |
| `arp.spoof on` | Jalankan ARP spoofing / MITM |

---

## 📚 Referensi

- [Dokumentasi resmi Bettercap](https://www.bettercap.org/)
- [Repo GitHub Bettercap](https://github.com/bettercap/bettercap)

---

✍️ *Personal notes — dikumpulkan sambil belajar network security.*
