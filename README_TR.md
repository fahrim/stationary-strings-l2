# Stationary Strings Letter 2 — Kaynak Yoksa Uyum da Yoktur

> **English:** [README.md](./README.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**L2: Kaynak Yoksa Uyum da Yoktur — Model Destekli Fizikte Literatür Değerleri İçin Adli Protokol**

Yazar: Fahri Meral · Tarih: 20 Ekim 2026 · Sürüm: v1 (L2)

> **Durum:** Yayımlanmamış ön-baskı (v1). Hakem denetiminden geçmemiştir. *[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.23517495-blue.svg)](https://doi.org/10.5281/zenodo.23517495)*

## Tek paragrafta iddia
Kendi ön-baskı serimizdeki, kendi kaynaklığımızdan gelen bir hatayı ve onu
aktarılabilir bir yönteme dönüştürüyoruz. Bir ölçümsel oranlar tablosu
*bağımsız literatür, model dışı* olarak etiketlenmiş ve iki model çıktısıyla
karşılaştırılmıştı; iki model çıktısı da iki alıntılanan aralığın içine
düşüyordu. Aralıklar hiçbir kaynakta yoktu — dört birincil makale tam olarak
indirildi ve tarandı (PDF metni *ve* LaTeX kaynağı) ve alıntılanan sayılar
onların hiçbirinde geçmiyor. İddia geri çekildi. İki bağımsız adli test kod
olarak yayımlanıyor: **depo arkeolojisi** (değer, onu kullanan uyum iddiası
*öncesinde* kaynak kaydı taşıyor muydu?) ve **kaynak varlık taraması**
(alıntılanan aralık korpusta hiç var mı?). İki görünür teyit ayrıca **cebire
bağımlıydı** — ikinci oran, birincinin karesinin kilitli bir sabite bölümü —
yani görünür iki noktalı uyum, kaynağı olmayan tek bir serbestlik derecesine
dayanıyordu. Etkilenen iki testte kullanılan altı literatür büyüklüğünden
**üçü hiçbir kaynağa izlenemiyordu**, ikisi daha sayısal olarak yanlıştı.

## Ne iddia ediliyor, ne edilmiyor
- **İddia:** hiçbir kaynakta var olmayan alıntılanan bir literatür aralığı
  teyit gibi görünebilir; tespit edilebilir; altı adımlık protokol ve en ucuz
  iki adımı uygulayan bir araç verilmiştir.
- **İddia:** kendi çalışmamızdaki somut aralık hayaletti ve iddia geri
  çekildi.
- **İddia edilmiyor:** aracın bir değerin *doğru* olup olmadığını
  belirleyebileceği. Araç depo provenance'ını ve korpus varlığını bildirir;
  kaynağın anlamsal okunuşu insani bir iş olarak kalır ve mektup bunu açıkça
  söyler.
- **İddia edilmiyor:** aralığın nereden geldiğini bildiğimiz. Depo yalnızca
  orada provenance kaydı *olmadığını* belirler.
- **Seriden bağımsızdır:** Teoremler I–X / Stationary Strings XI–XIV'ün hiçbir
  modeli, kilidi ya da ansatz'ı bu mektuba girmez.

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/stationary_strings_L2_ghost_parameter_forensics_EN.tex` | Mektup, İngilizce (7 sayfa, Tablo 1, Şekil 1) |
| `paper/stationary_strings_L2_ghost_parameter_forensics_TR.tex` | Türkçe sürüm |
| `figs/fig16_ghost_parameter_forensics{,_en}.{pdf,png}` | Adli özet figürü (2×2) |

Sayısal makine
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)
deposunda) bulunur:

```bash
python -W ignore duran_sicimler_sim/mini_check_l2.py    # 7/7 PASS
python -W ignore duran_sicimler_sim/ghost_audit.py \
    --repo . --values 1.55 1.70 --groups "1.55+1.70" \
    --paths duran_sicimler_sim \
    --sources <kaynak korpusu kok dizini>
```

Araç çözücüyü import etmez ve fiziksel modele bağlı değildir: bir depo ve bir
kaynak korpusu üzerinde çalışır.

## Atıf

```bibtex
@misc{meral2026ghost,
  author = {Fahri Meral},
  title  = {Kaynak Yoksa Uyum da Yoktur: Model Destekli Fizikte Literatür Değerleri İçin Adli Protokol},
  year   = {2026},
  url    = {https://github.com/fahrim/stationary-strings-l2},
  doi    = {10.5281/zenodo.23517495},
}
```

Ayrıca bkz. `CITATION.cff`.

## Lisans

CC BY 4.0 — bkz. `LICENSE`. İçerik hakem denetiminden geçmemiştir.
