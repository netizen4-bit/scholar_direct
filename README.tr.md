# ScholarDirect-MCP v1.0 🎓

<p align="center">
  <b> Araştırmacılar İçin Yerel ve Güvenli Akademik Araştırma Asistanı</b><br>
  <i>FastMCP, OpenAlex, Crossref, DergiPark, TR Dizin, Dünya Bankası ve Academic Research Guardian Becerisi ile Desteklenmektedir</i>
</p>

<p align="center">
  <a href="README.md"><b>English 🇬🇧</b></a> • <b>Türkçe 🇹🇷</b>
</p>

<p align="center">
  <a href="https://github.com/netizen4-bit/scholar_direct/stargazers"><img src="https://img.shields.io/github/stars/netizen4-bit/scholar_direct?style=for-the-badge&logo=github&color=1F4E79" alt="Stars"></a>
  <a href="https://github.com/netizen4-bit/scholar_direct/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License"></a>
  <a href="https://www.patreon.com/netizen4_bit"><img src="https://img.shields.io/badge/Patreon-Destek-F96854?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"></a>
  <a href="https://www.linkedin.com/in/nihatkasim"><img src="https://img.shields.io/badge/LinkedIn-Bağlantı-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

---

ScholarDirect-MCP v1.0, akademik çalışmalarını kolaylaştırmak için geliştirilmiş ücretsiz ve açık kaynaklı bir araştırma aracıdır. 

Yapay zekâ modelleri (ChatGPT, Claude vb.) genellikle var olmayan makaleler ve çalışmayan linkler uydurur. Ayrıca veri analizleri yaparken sohbete sürekli tablo kopyalayıp yapıştırmak çok fazla token harcar ve maliyeti artırır. ScholarDirect-MCP, bu sorunları çözmek için geliştirilmiştir:

1. **Gerçek ve Doğrulanmış Kaynaklar:** Uluslararası (OpenAlex, Crossref) ve Türkiye'deki (DergiPark, TR Dizin) gerçek hakemli makaleleri bulur. DOI numarası çalışmayan veya yayından kaldırılmış hiçbir makaleyi listeye almaz.
2. **Gerçek Verilerle Otomatik Analiz:** Dünya Bankası veya finans piyasalarından gerçek verileri indirir, temel istatistikleri ve modelleri (regresyon, karar verme modelleri vb.) doğrudan kendi bilgisayarınızda hesaplar.
3. **Masaüstü Arşiv:** Tüm analiz dosyalarını, tabloları, grafikleri ve Word taslaklarını doğrudan Masaüstünüzde açtığı bir klasörde arşivler.
4. **%95'e Varan Token Tasarrufu:** Hesaplamaları yapay zekânın sohbet penceresinde değil, bilgisayarınızdaki Python'la yaparak yapay zekâ kullanım kotanızı korur.

---

## 🔒 Verileriniz Neden Güvende? (Doğrudan Masaüstünü Arşiv)

Birçok internet sitesi ve bulut tabanlı yapay zekâ uygulaması, yüklediğiniz tez taslaklarını, anket sonuçlarını veya veri setlerini kendi sunucularına kaydeder. Bu durum, henüz yayımlanmamış tez çalışmalarınızın veya araştırma fikirlerinizin başkalarının eline geçmesi riskini doğurur ve ayrıca anketleri bulut tabanlı uygulamaya yükleyip analiz etmek bilimsel etik kurallarını ihlal eder.

**ScholarDirect-MCP ile verileriniz tamamen sizin kontrolünüzdedir:**
- **Buluta Veri Göndermez:** İndirilen veriler, yapılan hesaplamalar ve oluşturulan yazılar bulut sunuculara yüklenmez. Tüm araştırma süreci doğrudan sizin bilgisayarınızda çalışır.
- **Dosyalarınız Masaüstünde Saklanır:** Her çalışma için otomatik olarak Masaüstünüzde düzenli bir klasör oluşturulur:  
  `Masaüstü/Academic_Research_Workspace/<Proje_Adı>_<Tarih>/`
- **Tam Gizlilik:** Ham verileriniz, analiz kodlarınız, anketleriniz, grafikleriniz ve Word formatındaki makale taslağınız sadece sizin bilgisayarınızda kalır.

---

## ⚡ Token Verimliliği ve Karşılaştırmalı Kıyaslama

Yapay Zekâya *"bana şu konuda makale yaz ve analiz yap"* dediğinizde; ham tabloları eklemek, hatalı kodları düzeltmek ve doğrulanmamış kaynakları ayıklamak için yüz binlerce token harcarsınız. 

ScholarDirect-MCP, FastMCP arka plan araçlarını **Academic Research Guardian** (`academic-research-guardian`) ile birleştirerek bu sorunu çözer:

### 6 Aşamalı Akademik Araştırma Döngüsü Kıyaslaması

| Araştırma Aşaması | Standart / Serbest Yapay Zekâ Sohbeti | ScholarDirect-MCP + Guardian Becerisi | Token Tasarrufu |
|---|---|---|---|
| **1. Kaynak Arama & Tarama** | **~120.000 token**<br>*(Ham HTML sayfaları, doğrulanamayan PDF'ler, ölü linkler)* | **~3.500 token**<br>*(Sadece onaylı OpenAlex + DergiPark özet tablosu)* | **-%97,1** |
| **2. Makale Uygunluk Puanlama** | **~85.000 token**<br>*(Sohbette konu ve metot hakkında tahmin yürütme)* | **~2.200 token**<br>*(Bilgisayarda hızlı Python matematiği; kesin karar)* | **-%97,4** |
| **3. Literatür Boşluğu Analizi** | **~90.000 token**<br>*(Grafiksiz, genel ve yüzeysel sohbet önerileri)* | **~2.500 token**<br>*(Masaüstüne kaydedilen 300-DPI grafik ve Word raporu)* | **-%97,2** |
| **4. Ampirik Veri & Betimsel İstatistik** | **~180.000 token**<br>*(Sohbete ham tablo yapıştırma; hatalı hesaplar)* | **~3.000 token**<br>*(Dünya Bankası API çekimi; yerel Scipy APA matrisi)* | **-%98,3** |
| **5. Ekonometrik Modelleme** | **~250.000 token**<br>*(Sohbette 15+ tur Python hata ayıklama ve kod düzeltme)* | **~3.500 token**<br>*(Yerel `statsmodels`/`lifelines` çalıştırması; tanı testleri)* | **-%98,6** |
| **6. Makale Taslağı Yazımı** | **~220.000 token**<br>*(Turnitin %60+ benzerliğini kırmak için defalarca yeniden yazma)* | **~18.000 token**<br>*(İlk seferde doğal akademik dilde Word çıktısı)* | **-%91,8** |
| **Toplam Harcanan Bağlam Tokenı** | **~945.000 token** | **~32.700 token** | **-%96,5 Toplam Tasarruf** |

---

## 📊 Karşılaştırma: ScholarDirect-MCP vs. Diğer Yöntemler

| Özellik | Normal ChatGPT / Claude | Ücretli Akademik Siteler (30-100$/ay) | ScholarDirect-MCP |
|---|---|---|---|
| **Kaynak Doğruluğu** | ❌ Olmayan makaleler uydurabilir. | ⚠️ Yalnızca anlaşmalı dergileri gösterir. | ✅ **%100 Gerçek:** Crossref ile kontrol edilmiş gerçek makaleler. |
| **Türkiye Literatürü (DergiPark)** | ❌ DergiPark ve TR Dizin'i tarayamaz. | ❌ Genellikle sadece yabancı kaynaklara bakar. | ✅ **Var:** DergiPark'taki Türkçe makaleleri doğrudan tarar. |
| **Veri Gizliliği** | ❌ Verileriniz şirketin sunucularına gider. | ❌ Verileriniz internetteki bulutta tutulur. | ✅ **Güvenli:** Dosyalar doğrudan kendi Masaüstünüze kaydedilir. |
| **İstatistik ve Hesaplama** | ❌ Matematiksel hesaplarda hata yapabilir. | ❌ Genellikle analiz yapmaz, sadece makale özetler. | ✅ **Hatasız:** Python kütüphaneleriyle gerçek hesaplama yapar. |
| **Yapay Zekâ Benzerlik Oranı (Turnitin)** | ❌ %60-%80 arası yüksek benzerlik çıkar. | ⚠️ Yazım dili genellikle şablon ve monotondur. | ✅ **Doğal Dil:** Sade ve akıcı akademik dille yazar (<%15 benzerlik). |
| **Kullanım Ücreti** | Aylık 20$ - 200$ | Aylık 30$ - 100$ | ✅ **%100 Ücretsiz ve Açık Kaynak** |

---

## 📁 Proje Dizin Yapısı

```text
scholar_direct/
├── .agent/
│   └── skills/
│       └── academic-research-guardian/
│           └── SKILL.md             # Doğal akademik dil, gerçek metotlar ve APA 7 kuralları
├── scholar_direct.py                # 7 temel akademik aracı sunan FastMCP sunucusu
├── requirements.txt                 # Gerekli bilimsel, ekonometrik ve ofis Python paketleri
├── LICENSE                          # MIT Lisansı
├── README.tr.md                     # Türkçe dokümantasyon
└── README.md                        # Ana İngilizce dokümantasyon ve kıyaslamalar
```

---

## 📁 Masaüstünüzde Oluşturulan 5 Klasör Yapısı

ScholarDirect-MCP bir araştırma başlattığınızda Masaüstünüzde otomatik olarak 5 düzenli klasör oluştutur:

```text
Masaüstü/Academic_Research_Workspace/<Proje_Adı>_<Tarih>/
├── 01_Literature_and_Bibliometrics/
│   ├── verified_literature.xlsx      # Renkli ve filtreli Excel makale listesi
│   ├── verified_references.bib       # LaTeX ve tez yazımı için BibTeX dosyası
│   ├── apa7_bibliography.docx        # Word formatında hazır APA 7 kaynakçası
│   └── bibliometric_gap_report.docx  # Literatürdeki eksiklikleri anlatan Word raporu
├── 02_Empirical_Datasets/
│   ├── raw_dataset.csv               # İnternetten indirilen ham veri seti
│   ├── cleaned_dataset.xlsx          # Temizlenmiş veri ve korelasyon tablosu
│   └── descriptive_stats.docx        # Ortalama, standart sapma vb. özet tabloları
├── 03_Models_and_Scripts/
│   └── run_model_<model>.py          # Bilgisayarınızda çalışan çalıştırılabilir Python kodu
├── 04_Figures_and_Tables/
│   ├── citation_trend_by_year.png    # Yıllara göre yayın grafiği (300-DPI)
│   ├── methodology_gap_heatmap.png   # Konu ve yöntem boşluk haritası (300-DPI)
│   └── model_diagnostics.png         # Model test ve sonuç grafikleri
└── 05_Manuscript_Drafts/
    ├── <Proje_Adı>_manuscript.md      # Makale taslağının Markdown hali
    └── <Proje_Adı>_manuscript.docx    # Başlıkları ve tabloları hazır Word makalesi
```

---

## 🛠️ MCP Araçları Referansı (7 Temel Araç)

1. `search_verified_literature`: Konunuzla ilgili gerçek makaleleri arar, özetlerini çıkarır ve Excel olarak Masaüstünüze kaydeder.
2. `evaluate_paper_fit`: Bulunan makalelerin sizin konunuza ve metodunuza ne kadar uygun olduğunu 0-100 arasında puanlar.
3. `bibliometric_gap_and_journal_report`: Literatürde hangi konuların az çalışıldığını gösterir, net grafikler çizer ve çalışabileceğiniz 3 model önerir.
4. `generate_deterministic_apa7`: Makalelerin kaynakçasını APA 7 kurallarına göre (Türkçe için "vd." ve "ve" ekleyerek) Word ve BibTeX olarak hazırlar.
5. `fetch_empirical_dataset`: Dünya Bankası'ndan veya piyasalardan gerçek verileri indirir; ortalama, en küçük, en büyük gibi özet istatistikleri çıkarır.
6. `run_quantitative_or_qualitative_model`: Regresyon analizi, karar verme (AHP-TOPSIS) veya tahmin modellerini çalıştırıp sonuç tablosunu üretir.
7. `export_academic_manuscript`: Tüm bu adımları birleştirip giriş, yöntem, bulgular ve kaynakçası olan derli toplu bir Word makale taslağı oluşturur.

---

## 💬 Başlangıç İçin Örnek Promptlar (Hemen Kopyalayıp Kullanın)

Yapay zekâ asistanınıza (Antigravity, Claude Desktop veya Cursor) tek bir açık yönerge vererek tüm süreci kolayca çalıştırabilirsiniz:

```markdown
ScholarDirect-MCP araçlarını kullanarak benim için şu konuda bir araştırma projesi yürüt:
"Gelişmekte Olan Ülkelerde FinTech ve Dijital Bankacılığın Ekonomik Büyüme Üzerindeki Etkisi"

Lütfen sırasıyla şu adımları tamamla:
1. OpenAlex ve DergiPark üzerinden konuyla ilgili doğrulanmış 15 makale bul.
2. Makaleleri konuma uygunluğuna göre puanla ve en temel kaynakları belirle.
3. Literatürdeki eksiklikleri gösteren grafikleri oluştur.
4. Dünya Bankası'ndan Türkiye ve benzer ülkeler için GSYİH büyüme verisini indirip özet istatistik tablosunu hazırla.
5. Veriler üzerinden regresyon modelini çalıştır ve sonuçları çıkar.
6. Tüm kaynakları APA 7 formatında düzenle.
7. Sonuçları Masaüstümdeki Academic_Research_Workspace klasörüne hazır bir Word (.docx) makale taslağı olarak kaydet.

Veri gizliliği kuralına dikkat et: Tüm dosyalarımı yerel Masaüstü klasörümde tut, verileri internete sızdırma. Dili sade, akıcı ve doğal bir akademik üslupla yaz.
```

---

## 📦 Gereksinimler ve Hızlı Kurulum

### 1. Ön Koşullar ve Gereksinimler (Prerequisites)
* **Python (3.10+)**
* **Git**
* **Playwright Chromium** (`playwright install chromium`)
* MCP uyumlu bir yapay zekâ terminali (**Antigravity CLI / IDE**, **Claude Desktop**, **Cursor**) veya yerel **Ollama** kurulumu.

### 2. Elle (Manuel) Kurulum
Repoyu klonlayın, Python bağımlılıklarını yükleyin ve Playwright tarayıcısını kurun:
```bash
git clone https://github.com/netizen4-bit/scholar_direct.git
cd scholar_direct
pip install -r requirements.txt
playwright install chromium
```

### 3. Google Antigravity ile Otomatik Kurulum
Google Antigravity kullanıyorsanız, hiçbir şeyi elle kurmanıza gerek yoktur. Aşağıdaki yönergeyi kopyalayıp Antigravity sohbetine yapıştırmanız yeterlidir:

````markdown
ScholarDirect MCP sunucusunu Antigravity ortamıma otomatik olarak kur ve bağla:

1. https://github.com/netizen4-bit/scholar_direct adresindeki repoyu `~/.gemini/antigravity/scholar-direct-mcp` klasörüne klonla.
2. `requirements.txt` dosyasındaki tüm kütüphaneleri yükle (`pip install -r requirements.txt`) ve Playwright Chromium tarayıcısının kurulu olduğundan emin ol (`playwright install chromium`).
3. Sunucuyu Antigravity MCP yapılandırmasına (`~/.gemini/antigravity/config.json`) ekle:
   - Sunucu adı: `scholardirect`
   - Komut: `python`
   - Dosya: `scholar_direct.py` tam mutlak yolu (ters eğik çizgilerin kaçışlı olduğundan emin ol)
   - Ortam Değişkeni: `SCHOLARDIRECT_WORKSPACE_DIR` değerini `Desktop/Academic_Research_Workspace` olarak ayarla.
4. Birlikte gelen beceriyi (`.agent/skills/academic-research-guardian/SKILL.md`) `~/.gemini/config/skills/academic-research-guardian/` dizinine kopyala.
5. `scholar_direct.py` dosyasını test et ve 7 MCP aracının sorunsuz yüklendiğini onayla.
````

Antigravity asistanı repoyu çekecek, `config.json` dosyasını yapılandıracak, eksik paketleri kuracak ve araçları kullanıma hazır hale getirecektir.

---

## 🔌 Yapay Zekâ Terminalinize Bağlama (MCP JSON Yapılandırması)

ScholarDirect sunucusunu `claude_desktop_config.json`, `config.json` veya Cursor ayarlarınıza ekleyin:

> ⚠️ **Windows Yolları İçin Not:** JSON dosyalarında ters eğik çizgiler (`\`) kaçışlı (`\\`) yazılmalı veya düz eğik çizgi (`/`) kullanılmalıdır.

```json
{
  "mcpServers": {
    "scholardirect": {
      "command": "python",
      "args": [
        "C:\\Users\\KULLANICI_ADINIZ\\.gemini\\antigravity\\scholar-direct-mcp\\scholar_direct.py"
      ],
      "env": {
        "SCHOLARDIRECT_WORKSPACE_DIR": "C:\\Users\\KULLANICI_ADINIZ\\Desktop\\Academic_Research_Workspace"
      }
    }
  }
}
```

---

## 📄 Lisans & Destek

Bu proje **MIT Lisansı** ile korunmaktadır. Detaylar için `LICENSE` dosyasına bakabilirsiniz.

* **Açık Kaynak Geliştirmeyi Destekleyin:** [Patreon](https://www.patreon.com/netizen4_bit)  
* **Akademik & Kurumsal İletişim:** [LinkedIn](https://www.linkedin.com/in/nihatkasim)
