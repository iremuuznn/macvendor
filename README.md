# MAC Vendor Analiz Sistemi 🚀🔍📡

## Proje Açıklaması 🛠️📊🔎
MAC Vendor Analiz Sistemi, ağ üzerindeki cihazların MAC adreslerini analiz ederek üretici bilgilerini çıkaran, cihazları kategorize eden ve potansiyel güvenlik risklerini belirleyen bir sistemdir. 🚦🖥️📈

Bu sistem, MAC adreslerinden üretici bilgilerini çekerek cihazların hangi kategoriye ait olduğunu (IoT, son kullanıcı cihazları, ağ ekipmanları vb.) belirler. Ayrıca, sahte MAC adreslerini tespit edebilir ve vendor bazlı güvenlik riski değerlendirmesi yapabilir. 🕵️‍♂️🔐📊

## Takım Üyeleri 🤝🎓📌
- **Ebru Gündoğdu**, Öğrenci No: **2320191087**
- **İrem Rabia Uzun**, Öğrenci No: **2320191032**

## Kullanılan Kütüphaneler ve Versiyonları 📦📜🔢
Proje Python diliyle geliştirilmiştir ve aşağıdaki kütüphaneler kullanılmaktadır: 🚀📊🔧

- `requests` (>=2.26.0) - API istekleri için
- `pandas` (>=1.3.3) - Veri işleme ve analizi için
- `numpy` (>=1.21.2) - Sayısal işlemler için
- `scapy` (>=2.4.5) - Ağ trafiği analizi için
- `json` (Python standart kütüphane) - Çıktıları JSON formatında düzenlemek için

## Gerekli Araçlar ve Kurulum Gereksinimleri 🖥️🔧⚙️

Sistemin çalıştırılması için aşağıdaki gereksinimler sağlanmalıdır: 📌📝✅

- Python 3.8 veya üstü
- İnternet bağlantısı (MAC vendor veritabanı güncellemeleri için)
- Linux veya Windows işletim sistemi
- `pip` ile bağımlılıkların yüklenmesi

Kurulum gereksinimlerini yüklemek için:
```bash
pip install -r requirements.txt
```

## Çalıştırma Parametreleri ⚙️🛠️🎯

### Zorunlu Parametreler 🔍🔑🔢
| Parametre  | Açıklama |
|------------|--------------------------------|
| `--network` | Tarama yapılacak ağ aralığını belirler (Ör: 192.168.1.0/24) |

Örnek kullanım:
```bash
python mac_vendor_analysis.py --network 192.168.1.0/24
```

### Opsiyonel Parametreler 🛠️🔧⚡
| Parametre  | Açıklama |
|------------|--------------------------------|
| `--update-db` | MAC vendor veritabanını günceller |
| `--output` | Çıktıyı belirlenen dosya formatında kaydeder (varsayılan JSON) |

Örnek kullanım:
```bash
python mac_vendor_analysis.py --network 192.168.1.0/24 --update-db --output output.json
```

## Çıktı Formatı 📄📊🔎
Sistem tarafından üretilen tüm çıktı JSON formatında olacaktır. JSON verisi düzenli ve okunabilir bir şekilde yapılandırılmıştır. 📌📜📊

Örnek JSON çıktısı:
```json
{
    "network": "192.168.1.0/24",
    "devices": [
        {
            "mac_address": "00:1A:2B:3C:4D:5E",
            "vendor": "Apple Inc.",
            "category": "Son Kullanıcı Cihazı",
            "risk_level": "Düşük"
        },
        {
            "mac_address": "00:AA:BB:CC:DD:EE",
            "vendor": "Bilinmiyor",
            "category": "Sahte MAC",
            "risk_level": "Yüksek"
        }
    ]
}
```

## Kurulum ve Çalıştırma Talimatları 🛠️🚀📌
1. **Depoyu klonlayın:**
   ```bash
   git clone https://github.com/kullanıcı_adı/mac-vendor-analysis.git
   cd mac-vendor-analysis
   ```
2. **Gereksinimleri yükleyin:**
   ```bash
   pip install -r requirements.txt
   ```
3. **MAC vendor veritabanını güncelleyin:**
   ```bash
   python mac_vendor_analysis.py --update-db
   ```
4. **Ağ taraması yapın:**
   ```bash
   python mac_vendor_analysis.py --network 192.168.1.0/24
   ```
5. **Çıktıyı belirli bir dosyaya kaydetmek için:**
   ```bash
   python mac_vendor_analysis.py --network 192.168.1.0/24 --output results.json
   ```
