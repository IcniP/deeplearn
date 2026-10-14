# Studio 2 — Klasifikasi Sampah · Kelompok 8 MENDALAM BELAJAR

Deep Learning (IF25-40401) · Teknik Informatika ITERA · Semester Ganjil 2026/2027

## Anggota Kelompok

| No | Nama Lengkap | NIM | Kontribusi utama |
|----|--------------|-----|------------------|
| 1  | Dzaky pramadhani | 123140208 |             |
| 2  | M Farisi Suyitno | 123140152 |             |
| 3  | Awi Septian Prasetyo | 123140201 |         |

## Ringkasan Pendekatan

- **Arsitektur / backbone**: ResNet-18 pretrained ImageNet, layer fc diganti jadi 5 kelas
- **Strategi pelatihan**: fine-tuning semua layer, AdamW lr 3e-4, cosine scheduler, 10 epoch, batch 32, label smoothing 0.1, augmentasi random crop + flip + color jitter
- **Data tambahan**: tidak ada
- **Ukuran input & preprocessing**: 224x224, normalisasi ImageNet

## Hasil

| Putaran | Commit | Macro-F1 (split validasi lokal) | Macro-F1 (diumumkan asisten) |
|---------|--------|----------------------------------|------------------------------|
| Preview 1 (14 Okt) | | | |
| Preview 2 (21 Okt) | | | |
| Final (25 Okt)     | | | |

Catatan eksperimen singkat (apa yang dicoba, apa yang berhasil/gagal):

## Cara Reproduksi

```bash
pip install -r requirements.txt
# atau buka training.ipynb (Colab / Jupyter) dan Run All
python evaluate.py --submission ./submission --data ./my_val
```

Dataset (`train/`) diunduh dari Google Drive kelas dan tidak ikut diunggah ke repo ini.

## Struktur Repositori

```
submission/
  model.py          # get_model() dan get_transform()
  model.pth         # state_dict model terbaik
  requirements.txt
evaluate.py         # skrip evaluasi resmi
training.ipynb      # notebook pelatihan
requirements.txt
docs/progress_mingguan.md
```
