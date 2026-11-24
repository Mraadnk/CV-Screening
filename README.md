# n8n CV Analyzer Workflow

Workflow n8n buat ambil file CV (PDF), ekstrak isinya, kirim ke LLM buat dianalisis, lalu hasilnya dirapihin jadi JSON.

## Alur Workflow

<img width="1183" height="312" alt="Screenshot 2026-11-24 091308" src="https://github.com/user-attachments/assets/eaa1c7f3-12aa-4044-aa92-b1c27f2c58a3" />


- **When clicking 'Test workflow'**: Trigger manual buat ngetes jalan atau enggaknya alur.
- **Set Variables**: Ngatur variabel atau input awal yang dipakai di proses berikutnya.
- **Download File**: Download file CV PDF dari sumbernya.
- **Extract Document PDF**: Ambil teks dari dalam file PDF biar bisa dibaca model AI.
- **OpenAI - Analyze CV**: Kirim teks CV ke API LLM buat dianalisis sesuai prompt.
- **Parsed JSON**: Rapihin hasil analisis ke format JSON biar gampang dipakai lagi.

## Tools yang Dipakai

- n8n
- Gemini API / LLM endpoint
- JSON

## Cara Pakai

1. Import file `.json` workflow ke n8n.
2. Pasang API key / credential di node yang butuh akses (jangan di-hardcode di file yang mau di-upload).
3. Sesuaikan isi **Set Variables** sama sumber file di **Download File**.
4. Klik test workflow dan cek hasil JSON-nya.

## Catatan

Cek dulu isi JSON sebelum di-push ke Git—pastikan enggak ada API key, link privat, atau data CV asli yang ikut ke-commit.
