# Aset brand Posmed Studio

File SVG adalah master. PNG dibuat dari SVG dengan `rsvg-convert`.

| File | Pakai untuk |
| --- | --- |
| `avatar.svg`, `avatar-512.png`, `avatar-1024.png` | foto profil organisasi dan akun, latar penuh tanpa sudut membulat karena platform memotongnya sendiri |
| `logo-ikon.svg`, `logo-ikon-512.png` | ikon aplikasi, favicon, dan tempat yang menampilkan logo apa adanya |
| `logo-polos.svg`, `logo-polos-512.png` | logo tanpa latar, untuk ditaruh di atas latar terang |
| `banner.svg`, `banner.png` | banner profil GitHub, 1500 x 420 |

Warna utama teal `#0b7a6b`, sudut bidik `#cdeee8`, titik rekam `#ff6b57`. Tulisan memakai Inter dengan fitur `cv11` (huruf a satu tingkat), sama seperti Posmed. Di `banner.svg` teksnya sudah diubah jadi path, jadi tampil sama di mana pun tanpa perlu font terpasang. Untuk mengubah teks banner, bentuk ulang teksnya dengan HarfBuzz memakai fitur `cv11`, karena `rsvg-convert` mengabaikan `font-feature-settings`.

Contoh membuat ulang PNG

```
rsvg-convert -w 512 avatar.svg -o avatar-512.png
rsvg-convert banner.svg -o banner.png
```
