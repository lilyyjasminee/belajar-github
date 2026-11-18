# Belajar API - Contoh Pertama

API itu penghubung antar aplikasi. Contoh paling gampang: minta data profil GitHub sendiri lewat API GitHub, tanpa API key.

## 1. Coba di browser

Buka link ini di browser:

https://api.github.com/users/lilyyjasminee

Kamu akan lihat data dalam bentuk JSON, seperti nama, jumlah repo, dan tanggal akun dibuat.

## 2. Coba di Terminal Windows (PowerShell)

```powershell
curl https://api.github.com/users/lilyyjasminee
```

## 3. Coba di Python

```python
import requests

response = requests.get("https://api.github.com/users/lilyyjasminee")
data = response.json()

print(data["login"])
print(data["public_repos"])
```

## Istilah penting

- Request: permintaan yang kamu kirim ke API.
- Response: jawaban yang dikirim balik oleh API, biasanya bentuk JSON.
- Endpoint: alamat URL API-nya, contoh di atas.
- API Key: password khusus buat API yang butuh login. Contoh ini tidak butuh API key.
