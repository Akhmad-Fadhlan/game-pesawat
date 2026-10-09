# Sky Fighters 3D

Game statis (HTML + Three.js via CDN). Tidak perlu build.

## Struktur
```
public/index.html   # game
vercel.json         # konfigurasi Vercel
package.json
```

## Deploy ke Vercel

**Opsi 1 - CLI**
```
npm i -g vercel
cd sky-fighters-vercel
vercel --prod
```
(Framework Preset: "Other", tanpa build command.)

**Opsi 2 - GitHub**
1. Push folder ini ke repository GitHub.
2. Di vercel.com klik *Add New > Project*, pilih repo.
3. Framework Preset: **Other**. Build Command: kosongkan. Output Directory: `public`.
4. Deploy.

## Catatan ESP32 (Bluetooth / USB)
Web Bluetooth dan Web Serial butuh **HTTPS** dan browser Chrome/Edge.
Vercel otomatis memakai HTTPS, jadi kontrol ESP32 langsung bisa dipakai
di domain `*.vercel.app` (tidak lagi perlu mengunduh file .html).
