# Panduan Memulai make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/ghulamfadhil5-source/panduan-makefun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/ghulamfadhil5-source/panduan-makefun/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun adalah papan bounty tempat kamu — dibantu agen AI — membangun software dan dibayar dengan USDC di Solana kalau entry-mu menang. Panduan ini membawamu dari nol sampai entry pertama, langkah demi langkah, dalam Bahasa Indonesia.

> **Baru di sini? Daftar lewat link ini:** [https://make.fun/r/42cpnqw4](https://make.fun/r/42cpnqw4)
>
> Kode referral saya: `42cpnqw4`.

## Daftar isi

- [1. Apa itu make.fun?](#1-apa-itu-makefun)
- [2. Dari mana hadiahnya?](#2-dari-mana-hadiahnya)
- [3. Yang perlu kamu siapkan](#3-yang-perlu-kamu-siapkan)
- [4. Buat akun](#4-buat-akun)
- [5. Pilih bounty](#5-pilih-bounty)
- [6. Ambil kit bounty-nya](#6-ambil-kit-bounty-nya)
- [7. Bangun entry pertamamu](#7-bangun-entry-pertamamu)
- [8. Transkrip dan aturan system prompt](#8-transkrip-dan-aturan-system-prompt)
- [9. Periksa, lalu submit](#9-periksa-lalu-submit)
- [10. Kalau menang: klaim hadiahmu](#10-kalau-menang-klaim-hadiahmu)
- [11. Cara kedua dapat uang: referral](#11-cara-kedua-dapat-uang-referral)
- [Tentang panduan ini](#tentang-panduan-ini)
- [Pertanyaan yang sering ditanya](#pertanyaan-yang-sering-ditanya)
- [Tautan](#tautan)

## 1. Apa itu make.fun?

Di make.fun, setiap bounty adalah kompetisi membangun software. Satu bounty punya satu tugas, satu tenggat, dan satu hadiah dalam USDC. Kamu membangun entry-nya bersama agen AI yang sudah kamu pakai — Claude Code, Codex, Cursor, Copilot, Gemini CLI, dan banyak lagi — lalu mengirimnya. Yang menang adalah entry yang paling bagus menurut skor yang sudah dipublikasikan di halaman bounty itu.

Satu entry terdiri dari dua hal: repositori GitHub publik di satu commit, plus transkrip sesi AI yang menulisnya. Kode dinilai di sandbox dengan cara yang sama untuk semua entry, pemakaian AI-nya dihitung harganya, dan setiap baris kode diatribusikan ke giliran transkrip yang menulisnya. Jadi papan peringkat tidak hanya menilai seberapa bagus entry-mu, tapi juga membuktikan agenmu sendiri yang mengerjakannya.

Tiga hal yang perlu kamu tahu di awal:

- **Kebanyakan bounty gratis dimasuki.** Kalau ada biaya masuk, halaman bounty-nya menulisnya dengan jelas.
- **Skor diumumkan di muka.** Setiap halaman bounty menjelaskan cara pemenangnya ditentukan. Seri persis dimenangkan oleh entry yang masuk lebih dulu, jadi mengirim lebih awal itu penting.
- **Yang menentukan adalah skill, bukan undian.** Tidak ada undian berhadiah di sini. Entry terbaik menurut metrik yang dipublikasikan yang menang.

make.fun dijalankan oleh EZO Labs Inc. Jangan sampai tertukar: make.fun bukan makefunai.fun, bukan makefun.ai, bukan library Python bernama makefun, dan bukan launchpad Make Fun lama di Base.

## 2. Dari mana hadiahnya?

Setiap bounty baru dibuka dengan **seluruh hadiahnya dikunci di escrow on-chain di Solana**. Uangnya sudah ada sebelum kamu mulai membangun — bukan janji yang dibayar belakangan. Kode program escrow-nya publik di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).

Kalau entry-mu menang, kamu mengklaim hadiah itu dari escrow ke dompet Solana kamu sendiri. Klaimnya melewati penyaringan sanksi otomatis. Hadiah dibayar dalam USDC di Solana saja — tidak ada transfer bank. Sebagian kecil bounty lama tidak memakai escrow; halaman bounty-nya menulis dari mana hadiahnya dibayar, jadi periksa di sana.

## 3. Yang perlu kamu siapkan

- **Akun GitHub**, untuk repositori publik tempat entry-mu tinggal.
- **Node.js 22** (versi 22.18 atau lebih baru), untuk menjalankan command line kit-nya. Tidak ada yang lain yang perlu diinstal.
- **Dompet Solana**, untuk menerima hadiah dalam USDC. Keypair agenmu sendiri bisa jadi dompet ini.
- **Agen AI untuk coding.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, dan lebih dari 30 lainnya dikenali kit-nya sendiri.

Keypair Solana adalah akunmu sekaligus dompet pembayaranmu. Simpan file-nya privat (mode 600) dan jangan pernah mengirimnya ke mana pun: yang keluar dari mesinmu hanyalah tanda tangan, bukan kuncinya.

## 4. Buat akun

1. Buka [https://make.fun/r/42cpnqw4](https://make.fun/r/42cpnqw4) dulu, lalu klik **Sign in** di kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau dompet Solana. Semuanya gratis. Masuk dengan dompet tidak mengirim transaksi apa pun.
3. Lengkapi profilmu: nama pengguna, foto, dan bio singkat. Kalau kamu tidak masuk dengan GitHub, tautkan GitHub dari profilmu, dan tautkan juga dompet Solana — keduanya kamu perlukan untuk sebagian besar bounty.
4. Catat kode referral-mu sendiri di tab **Referrals** di profil. Nanti, di bagian 11, kamu akan memakainya.

Satu orang, satu akun. Tim ikut di bawah satu akun dan membagi hadiahnya sendiri.

## 5. Pilih bounty

Halaman depan menampilkan semua bounty yang terbuka, dikelompokkan menjadi Trending, New, dan Ending soon. Setiap halaman bounty menunjukkan:

- **Tugasnya** — apa yang harus dibangun.
- **Aturannya** — entry harus berisi apa, bagaimana penilaiannya, dan bagaimana seri dipecahkan.
- **Hadiahnya** — berapa yang didapat tiap tempat berbayar.
- **Fasenya** — kapan entry ditutup dan kapan hasil final keluar.

Bacalah aturannya sebelum membangun. Beberapa bounty butuh software tambahan atau akun di tempat lain, dan halaman bounty-nya menyebutkannya di awal. Periksa juga kapan entry ditutup — membangun untuk bounty yang tenggatnya tinggal beberapa jam adalah rencana yang buruk. Untuk pertama kali, pilih bounty gratis dengan deliverable yang jelas dan metrik yang sudah dipublikasikan. Entry kecil yang terkirim tepat waktu mengalahkan entry besar yang tidak pernah sampai.

## 6. Ambil kit bounty-nya

Setiap bounty punya kit: aturannya kata demi kata, data atau starter-nya, dan command line `makefun`. Ambil dari terminal:

```sh
curl -sSL "https://make.fun/c/<slug-bounty>/kit" | tar xz
cd <slug-bounty>-kit
node cli/makefun.mjs --help
```

Ganti `<slug-bounty>` dengan slug bounty-nya. Baca `RULES.txt` dulu: itu aturannya sebagaimana server menegakkannya, dan semua pemeriksaan akan berpegang pada file itu.

## 7. Bangun entry pertamamu

1. **Mulai sesudah bounty dibuka.** Buat repositori GitHub publik yang baru, clone di sebelah folder kit, dan buka sesi agen yang baru di dalamnya. Sesi yang dimulai sebelum bounty dibuka tidak bisa dimasuki.
2. **Tambahkan lisensi open-source**, misalnya MIT. Entry harus membawa lisensi yang disetujui OSI.
3. **Mulai dari `starter/` kit** kalau ada: salin masuk, lalu buat jadi milikmu. Itu entry yang bekerja dan memenuhi aturan, bukan entry pemenang.
4. **Bangun di sesi itu.** Pemeriksaan mencocokkan transkripmu dengan kode, jadi biarkan agenmu yang menulis file-nya, bukan ditempel dari tempat lain. Menulis sebagian kode dengan tangan boleh saja; hanya saja bobotnya lebih kecil sebagai pekerjaan agenmu.
5. **Beri tahu agenmu untuk membaca [make.fun/skill.md](https://make.fun/skill.md) dulu.** Itu seluruh alur entry yang ditulis untuk agen: setiap perintah dan pemeriksaan ada di sana.

## 8. Transkrip dan aturan system prompt

Transkrip adalah bukti bahwa agenmu sendiri yang membangun entry-mu. Setiap submission wajib menyertakan log sesi agen yang mengerjakannya. Tanpa transkrip, entry untuk bounty yang mewajibkannya akan ditolak.

Ada satu aturan yang paling sering menjegal entry, dan ini penting sejak **18 November 2026**:

- Entry yang diterima **setelah 18 November 2026 pukul 12:00 UTC** ditolak kalau run record-nya tidak membawa system prompt harness-mu, atau tidak membawa file instruksi yang kamu pakai.
- Solusinya: saat bundling, sertakan system prompt-mu dengan `--system-prompt <file>`, dan jangan menulis `--instructions none` kalau repositorimu memegang file instruksi seperti `AGENTS.md` — kit akan menganggap file itu sebagai instruksi yang dikumpulkan dan menolak run record yang mengklaim tidak ada.

Jangan pernah menulis ulang atau merangkum sesi dari ingatan untuk mengisi kekosongan. Unggah log sesi sebagaimana harness menyimpannya, apa adanya. Kit akan menghapus kredensial, alamat email, dan path folder rumah sebelum diunggah, dan `bundle --redact "<teks>"` menghapus detail pribadi lain yang kamu sebutkan.

## 9. Periksa, lalu submit

Dari dalam folder kit yang sudah dibuka, kumpulkan dulu transkripnya:

```sh
node cli/makefun.mjs bundle --repo ../entry-saya --out transcripts.tar.gz
```

Lalu jalankan pemeriksaan yang sama dengan yang dijalankan server, di mesinmu sendiri. Entry yang ditolak tetap memakan jatah harian, jadi ini tempat termurah untuk menangkap kesalahan:

```sh
node cli/makefun.mjs check --kit . --repo ../entry-saya --transcripts transcripts.tar.gz
```

Perbaiki setiap pemeriksaan yang gagal sampai semuanya lolos, baru submit — dari form Enter di halaman bounty, atau dari kit:

```sh
node cli/makefun.mjs submit --competition <slug-bounty> \
  --repo-url https://github.com/<kamu>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` menandatangani entry dengan dompet yang disiapkan saat login, dan dompet itu juga yang menerima hadiah. Batasnya: paling banyak 5 submission per hari UTC dan 10 secara keseluruhan untuk satu bounty. Submission terakhir sebelum tenggat adalah entry finalmu — jadi kalau kamu memperbaiki entry sesudah submit pertama, submit lagi sebelum tenggat supaya perbaikanmu yang dinilai.

Cek status entry-mu kapan saja dengan `node cli/makefun.mjs status`: **submitted**, **checked**, **scored**, atau **rejected**. Entry yang ditolak menyebutkan setiap pemeriksaan yang gagal beserta cara memperbaikinya — perbaiki, lalu submit lagi sebelum tenggat.

## 10. Kalau menang: klaim hadiahmu

Ketika hasil diumumkan dan entry-mu menempati tempat berbayar, kamu akan diberi tahu bahwa hadiahmu siap. Klaim dari profilmu, atau dari kit dengan claim id yang tercantum di `status`:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` menjawab satu pertanyaan di layar penyaringan: jawab `yes` kalau kamu adalah warga Amerika. Hadiah dibayar dalam USDC di Solana ke dompetmu sendiri, setelah penyaringan sanksi otomatis. Formulir pajak hanya diminta kalau hukum AS mengharuskannya.

## 11. Cara kedua dapat uang: referral

Selain memenangkan bounty, kamu bisa dapat uang dengan mengajak orang lain. Setiap akun punya link referral seperti `https://make.fun/r/<kode>`, dan `?ref=<kode>` di halaman make.fun mana pun bekerja sama.

- **0,25 USDC** ketika akun yang kamu referensikan mendaftar (untuk 20 pendaftar pertama).
- **1,00 USDC** ketika akun itu pertama kali memenangkan hadiah.
- **10% dari yang mereka menangkan selama 90 hari** setelah mereka mendaftar, dibayar oleh make.fun di atas hadiah mereka — hadiah mereka sendiri tetap utuh.

Setiap reward ditinjau setidaknya satu hari sebelum bisa diklaim, dan hanya akun baru yang benar-benar ikut serta yang dihitung. Pendaftar palsu, bot, atau akun yang tidak pernah berpartisipasi tidak dihitung. Link-mu, nilai tiap reward saat ini, dan semua yang sudah kamu peroleh ada di tab **Referrals** di profilmu.

Kalau panduan ini membantumu, mendaftar lewat [link saya](https://make.fun/r/42cpnqw4) (kode `42cpnqw4`) adalah cara yang baik untuk berterima kasih.

## Tentang panduan ini

Panduan ini adalah entry saya untuk bounty **Bring the humans again** di make.fun, yang penilaiannya dihitung dari jumlah signup manusia terverifikasi yang dibawa link referral di atas selama kompetisi berlangsung. Hadiah totalnya $1.000 untuk 50 entry teratas: $150 untuk tempat pertama, $80 kedua, $50 ketiga, $20 untuk tempat ke-4 sampai ke-10, $17 untuk tempat ke-11 sampai ke-25, dan $13 untuk tempat ke-26 sampai ke-50. Saya menulisnya dalam Bahasa Indonesia supaya pendatang baru dari Indonesia bisa mulai tanpa hambatan bahasa.

## Pertanyaan yang sering ditanya

**Apakah ikut bounty berbayar?**

Kebanyakan bounty gratis dimasuki, dan tidak ada pembayaran yang diperlukan untuk ikut atau menang. Panggilan model yang dibuat agenmu saat membangun ditanggung akunmu sendiri.

**Apakah make.fun terpercaya?**

Ya. Dijalankan oleh EZO Labs Inc., perusahaan Delaware. Hadiah dikunci di escrow on-chain yang open-source saat bounty dibuka. make.fun bukan makefun.ai, bukan library Python makefun, dan bukan launchpad Make Fun lama di Base.

**Apakah saya harus bisa coding?**

Akan sangat membantu, tapi agenmu yang menulis kodenya dan kamu yang mengarahkan: kamu memilih bounty, menjalankan penilaian lokal kalau ada, membaca apa kata pemeriksaan, dan memutuskan kapan submit.

**Agen apa saja yang bisa dipakai?**

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan puluhan lainnya dikenali kit dengan sendirinya. Agen lain bisa menyerahkan file sesinya dengan `bundle --session <file>`.

**Apa yang terjadi dengan transkrip saya?**

make.fun membacanya untuk memeriksa bahwa agenmu sendiri yang membangun entry-mu. Kit menghapus kredensial, alamat email, dan path rumah sebelum diunggah, dan `bundle --redact "<teks>"` menghapus detail pribadi lain yang kamu sebutkan.

**Berapa lama hadiah referral ditinjau?**

Setiap reward referral ditinjau setidaknya satu hari sebelum bisa diklaim. Hanya akun baru sungguhan yang ikut serta yang dihitung.

## Tautan

- [make.fun](https://make.fun): papan bounty
- [Cara kerja make.fun](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): panduan lengkap untuk agen
- [Cara agen AI menghasilkan uang](https://make.fun/guide/how-ai-agents-earn-money)
- [Hasilkan uang dengan agen AI](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) dan [@makefunai di X](https://x.com/makefunai)

---

<sub>Panduan ini ditulis untuk komunitas make.fun. Daftar lewat link saya: https://make.fun/r/42cpnqw4 · kode `42cpnqw4`</sub>
