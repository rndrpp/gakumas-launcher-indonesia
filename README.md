# Launcher Gakuen Idolmaster (Bahasa Indonesia)

Launcher Windows untuk menjalankan **Gakuen Idolmaster** (versi DMM) tanpa DMM GAME PLAYER dan tanpa VPN.

Versi bahasa Indonesia dari [i0rph/gakumas-launcher](https://github.com/i0rph/gakumas-launcher).

Ambil `GakumasLauncher.exe` dari [Releases](../../releases) lalu jalankan. Game tetap harus sudah terpasang sekali lewat DMM GAME PLAYER.

## Mode koneksi Jepang

| Mode | Keterangan |
|---|---|
| VPN Gate | Bawaan. Menyambung ke server publik VPN Gate (Universitas Tsukuba) hanya di dalam launcher. Tidak perlu pengaturan tambahan. |
| File VPN | Menyambung memakai file konfigurasi dari layanan VPN Anda, di dalam launcher. Mendukung OpenVPN (`.ovpn`) dan WireGuard (`.conf`). |
| Tanpa VPN | Memakai internet PC apa adanya, tanpa VPN. Jika Anda di luar Jepang, sambungkan dulu ke VPN Jepang lewat aplikasi VPN. |

VPN Gate dan File VPN tidak mengubah pengaturan jaringan Windows — hanya komunikasi launcher yang melewati VPN.

### Cara memakai File VPN

1. Di halaman akun layanan VPN Anda, unduh file konfigurasi manual untuk **server Jepang** (OpenVPN atau WireGuard).
2. Di launcher, pilih **File VPN** → **Pilih file**, lalu pilih file yang sudah diunduh.
3. Jika file OpenVPN meminta ID dan kata sandi, isi lewat **Akun**. Sering kali ini akun khusus OpenVPN, bukan kata sandi login layanan.

File konfigurasi dan akun disimpan dalam bentuk terenkripsi, hanya bisa dibuka oleh akun Windows di PC ini.

## Build

```
cargo build --release --bin GakumasLauncher
```

## Peringatan

DMM tidak mendukung penggunaan dari luar Jepang. Segala risiko penggunaan menjadi tanggung jawab pengguna.
