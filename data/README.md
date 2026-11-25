# Dataset

## Sumber
- Dataset: CWRU Bearing Datasets (diunggah oleh brjapon)
- Platform: Kaggle
- Link: https://www.kaggle.com/datasets/brjapon/cwru-bearing-datasets
- Data asli: Case Western Reserve University (CWRU) Bearing Data Center

## File yang Dipakai
- Nama file: [feature_time_48k_2048_load_1.csv]
- Jumlah data: 2300 sampel (230 sampel per kelas)
- Jumlah kolom: 10 (9 fitur + 1 label)

## Kondisi Pengukuran
- Sensor: akselerometer di drive end motor
- Bearing: SKF 6205-2RS JEM (deep groove ball bearing)
- Frekuensi sampling: 48 kHz
- Beban motor: 1 HP
- Jenis cacat: dibuat dengan electro-discharge machining (EDM)

## Fitur (Domain Waktu)
| Kolom | Keterangan |
|---|---|
| max | Nilai maksimum sinyal |
| min | Nilai minimum sinyal |
| mean | Rata-rata sinyal |
| sd | Standar deviasi |
| rms | Root mean square |
| skewness | Kemiringan distribusi sinyal |
| kurtosis | Keruncingan distribusi, naik saat ada impuls akibat cacat |
| crest | Crest factor (puncak dibagi RMS) |
| form | Form factor (RMS dibagi rata-rata nilai absolut) |

## Label (kolom `fault`)
10 kelas kondisi bearing:
- Normal
- Ball fault: 0.007, 0.014, 0.021 inci
- Inner Race fault: 0.007, 0.014, 0.021 inci
- Outer Race fault: 0.007, 0.014, 0.021 inci

Pada notebook, 10 kelas digabung menjadi 4 kelas: Normal, Ball, Inner Race, Outer Race.

## Catatan
File CSV tidak diunggah ke repo ini. Unduh langsung dari Kaggle lalu simpan di Google Drive.

## Referensi
- W. A. Smith and R. B. Randall, "Rolling element bearing diagnostics using the Case Western Reserve University data: A benchmark study," Mechanical Systems and Signal Processing, vol. 64-65, pp. 100-131, 2015.
- D. Rinaldi and I. P. Sary, "Machine Learning untuk Predictive Maintenance Motor: Studi Komparasi Isolation Forest, Autoencoder, dan Z-score," Jurnal Elkolind, vol. 13, no. 2, 2026.
