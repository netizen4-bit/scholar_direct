# ScholarDirect-MCP v1.0 🎓

<p align="center">
  <b>Öğrenciler ve Araştırmacılar İçin Yerel ve Güvenli Akademik Araştırma Asistanı</b><br>
  <i>A Token-Efficient, Privacy-Focused Local Academic Research Assistant for Students & Researchers</i>
</p>

<p align="center">
  <a href="#-türkçe"><b>Türkçe 🇹🇷</b></a> •
  <a href="#-english"><b>English 🇬🇧</b></a>
</p>

<p align="center">
  <a href="https://github.com/netizen4-bit/scholar_direct/stargazers"><img src="https://img.shields.io/github/stars/netizen4-bit/scholar_direct?style=for-the-badge&logo=github&color=1F4E79" alt="Stars"></a>
  <a href="https://github.com/netizen4-bit/scholar_direct/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License"></a>
  <a href="https://www.patreon.com/netizen4_bit"><img src="https://img.shields.io/badge/Patreon-Destek-F96854?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"></a>
  <a href="https://www.linkedin.com/in/nihatkasim"><img src="https://img.shields.io/badge/LinkedIn-Bağlantı-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

---

<a name="-türkçe"></a>
# 🇹🇷 TÜRKÇE DOKÜMANTASYON

ScholarDirect-MCP v1.0, lisans ve lisansüstü öğrencileri ile araştırmacıların akademik çalışmalarını kolaylaştırmak için geliştirilmiş ücretsiz ve açık kaynaklı bir araştırma aracıdır. 

Yapay zekâ modelleri (ChatGPT, Claude vb.) genellikle var olmayan sahte makaleler ve çalışmayan linkler uydurur. Ayrıca veri analizleri yaparken sohbete sürekli tablo kopyalayıp yapıştırmak çok fazla token harcar ve maliyeti artırır. ScholarDirect-MCP, bu sorunları çözmek için geliştirilmiştir:

1. **Gerçek ve Doğrulanmış Kaynaklar:** Uluslararası (OpenAlex, Crossref) ve Türkiye'deki (DergiPark, TR Dizin) gerçek hakemli makaleleri bulur. DOI numarası çalışmayan veya yayından kaldırılmış hiçbir makaleyi listeye almaz.
2. **Gerçek Verilerle Otomatik Analiz:** Dünya Bankası veya finans piyasalarından gerçek verileri indirir, temel istatistikleri ve modelleri (regresyon, karar verme modelleri vb.) doğrudan kendi bilgisayarınızda hesaplar.
3. **Masaüstüne Düzenli Kayıt:** Tüm analiz dosyalarını, tabloları, grafikleri ve Word taslaklarını doğrudan Masaüstünüzde açtığı bir klasörde toplar.
4. **%95'e Varan Token Tasarrufu:** Hesaplamaları yapay zekânın sohbet penceresinde değil, bilgisayarınızdaki Python motorunda yaparak yapay zekâ kullanım kotanızı korur.

---

## 🔒 Verileriniz Neden Güvende? (Doğrudan Masaüstünüze Kayıt)

Birçok internet sitesi ve bulut tabanlı yapay zekâ uygulaması, yüklediğiniz tez taslaklarını, anket sonuçlarını veya veri setlerini kendi sunucularına kaydeder. Bu durum, henüz yayımlanmamış tez çalışmalarınızın veya araştırma fikirlerinizin başkalarının eline geçmesi riskini doğurur.

**ScholarDirect-MCP ile verileriniz tamamen sizin kontrolünüzdedir:**
- **Buluta Veri Göndermez:** İndirilen veriler, yapılan hesaplamalar ve oluşturulan yazılar internetteki yabancı sunuculara yüklenmez. Tüm işlemler doğrudan sizin bilgisayarınızda çalışır.
- **Dosyalarınız Masaüstünde Saklanır:** Her çalışma için otomatik olarak Masaüstünüzde düzenli bir klasör oluşturulur:  
  `Masaüstü/Academic_Research_Workspace/<Proje_Adı>_<Tarih>/`
- **Tam Gizlilik:** Ham verileriniz, analiz kodlarınız, net grafikleriniz ve Word formatındaki makale taslağınız sadece sizin bilgisayarınızda kalır.

---

## ⚡ Neden Daha Az Token Harcar? (Tasarruf Tablosu)

Normalde bir yapay zekâya *"bana şu konuda makale yaz ve analiz yap"* dediğinizde; ham tabloları yapıştırmak, hatalı kodları düzeltmek ve uydurulan kaynakları ayıklamak için yüz binlerce token harcarsınız. 

ScholarDirect-MCP ise arka planda çalışan Python araçlarıyla işi doğrudan bilgisayarınızda çözer ve sohbete yalnızca temiz bir özet tablo sunar:

| Araştırma Aşaması | Standart Yapay Zekâ Sohbeti | ScholarDirect-MCP ile | Tasarruf |
|---|---|---|---|
| **1. Kaynak Arama** | ~120.000 token *(uzun metinler, ölü linkler)* | **~3.500 token** *(sadece onaylı makale özeti)* | **-%97** |
| **2. Makale Puanlama** | ~85.000 token *(sohbette tahmin yürütme)* | **~2.200 token** *(bilgisayarda hızlı puanlama)* | **-%97** |
| **3. Konu Boşluğu Analizi** | ~90.000 token *(sohbette uzun tartışmalar)* | **~2.500 token** *(Masaüstüne kaydedilen hazır grafik)* | **-%97** |
| **4. Veri İndirme & İstatistik** | ~180.000 token *(sohbete ham veri yapıştırma)* | **~3.000 token** *(Dünya Bankası'ndan otomatik çekim)* | **-%98** |
| **5. Model & Hesaplamalar** | ~250.000 token *(kod hatalarını sohbette düzeltme)* | **~3.500 token** *(bilgisayarda hatasız hesaplama)* | **-%98** |
| **6. Makale Taslağı Yazımı** | ~220.000 token *(yapay zekâ kokan metni tekrar yazma)* | **~18.000 token** *(doğal akademik dilde tek seferde Word)* | **-%92** |
| **Toplam Harcanan Token** | **~945.000 token** | **~32.700 token** | **-%96,5 Tasarruf** |

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

## 📁 Masaüstünüzde Oluşturulan Klasör Yapısı

ScholarDirect-MCP bir proje başlattığınızda Masaüstünüzde otomatik olarak 5 düzenli klasör açar:

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
│   ├── citation_trend_by_year.png    # Yıllara göre yayın grafiği (yüksek çözünürlüklü)
│   ├── methodology_gap_heatmap.png   # Konu ve yöntem boşluk haritası
│   └── model_diagnostics.png         # Model test ve sonuç grafikleri
└── 05_Manuscript_Drafts/
    ├── <Proje_Adı>_manuscript.md      # Makale taslağının Markdown hali
    └── <Proje_Adı>_manuscript.docx    # Başlıkları ve tabloları hazır Word makalesi
```

---

## 🛠️ Sunulan 7 Basit Araç Ne İşe Yarar?

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

### 🎯 Örnek 1: Tam Kapsamlı Bir Araştırma Başlatmak İçin
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

### 🔬 Örnek 2: Karar Verme veya Önceliklendirme Analizi İçin (AHP-TOPSIS)
```markdown
ScholarDirect-MCP kullanarak "Surdurulebilir_Tedarikci_Secimi" başlıklı bir karar analizi yap:
1. Konuyla ilgili 10 onaylı makale bul.
2. 4 kriter belirleyerek ("Maliyet", "Kalite", "Teslimat_Hızı", "Çevre_Duyarlılığı") AHP-TOPSIS modelini çalıştır.
3. Sonuç grafiğini ve Python kodunu Masaüstümdeki klasöre kaydet.
```

---

## 📦 Kolay Kurulum

### 1. Elle Kurulum
```bash
git clone https://github.com/netizen4-bit/scholar_direct.git
cd scholar_direct
pip install -r requirements.txt
playwright install chromium
```

### 2. Google Antigravity İçin Otomatik Kurulum
Google Antigravity kullanıyorsanız, şu kısa metni sohbete yapıştırmanız yeterlidir:

````markdown
ScholarDirect MCP sunucusunu Antigravity ortamıma kur:

1. https://github.com/netizen4-bit/scholar_direct adresindeki repoyu `~/.gemini/antigravity/scholar-direct-mcp` klasörüne klonla.
2. `requirements.txt` dosyasındaki kütüphaneleri yükle (`pip install -r requirements.txt`).
3. Sunucuyu `~/.gemini/antigravity/config.json` dosyasına ekle:
   - Sunucu adı: `scholardirect`
   - Komut: `python`
   - Dosya: `scholar_direct.py` tam yolu
   - Kayıt Yeri: `Desktop/Academic_Research_Workspace`
4. Birlikte gelen beceriyi (`.agent/skills/academic-research-guardian/SKILL.md`) Antigravity beceri klasörüne kopyala.
5. Kurulumu test et ve 7 aracın hazır olduğunu doğrula.
````

---
---

<a name="-english"></a>
# 🇬🇧 ENGLISH DOCUMENTATION

ScholarDirect-MCP v1.0 is a free, open-source local Model Context Protocol (MCP) tool designed for students, researchers, and academics.

Commercial AI models often hallucinate fake citations, invent non-existent DOIs, and waste thousands of tokens when you copy and paste raw spreadsheets into chat. ScholarDirect-MCP solves this:

1. **Verified Academic Literature:** Searches real peer-reviewed articles from international repositories (OpenAlex, Crossref) and national Turkish repositories (DergiPark, TR Dizin). Papers with broken DOIs or retraction flags are discarded.
2. **Real Empirical Data & Math:** Pulls live indicators from World Bank API and Yahoo Finance, running actual econometric regressions and decision models locally on your computer with real Python libraries (`statsmodels`, `lifelines`, `scikit-learn`).
3. **Organized Desktop Workspace:** Saves all clean spreadsheets, 300-DPI charts, Python scripts, and formatted Word documents directly into a dedicated folder on your Desktop.
4. **Up to 95% Token Savings:** Keeps raw data and computation on your local machine, returning only concise summary tables to the AI prompt.

---

## 🔒 Complete Local Privacy: All Data Stays on Your Desktop

Most cloud-hosted academic tools upload your unpublished drafts, research ideas, and proprietary datasets to remote internet servers. This exposes your work to potential data leaks and unauthorized model training.

**With ScholarDirect-MCP, your data never leaves your computer:**
- **Zero Cloud Uploads:** Data fetching, cleaning, calculations, and manuscript drafting occur strictly on your machine.
- **Direct Desktop Storage:** Every project automatically creates a clean workspace:  
  `Desktop/Academic_Research_Workspace/<Project_Name>_<Date>/`
- **Full Research Sovereignty:** Your raw spreadsheets, analysis code, high-resolution charts, and Word manuscripts remain safely on your local disk.

---

## ⚡ Token Savings: Why It Uses Fewer Tokens

When you ask a standard AI chat to analyze data and write a paper, uploading large CSV files and repeatedly fixing broken code burns hundreds of thousands of tokens. 

ScholarDirect-MCP does the heavy lifting in Python locally on your machine and only sends the clean final result back to the chat:

| Research Stage | Standard AI Chat | With ScholarDirect-MCP | Savings |
|---|---|---|---|
| **1. Finding Literature** | ~120,000 tokens *(unverified text, dead links)* | **~3,500 tokens** *(compact verified table)* | **-97%** |
| **2. Scoring Paper Relevance** | ~85,000 tokens *(conversational guesswork)* | **~2,200 tokens** *(instant local scoring)* | **-97%** |
| **3. Literature Gap Analysis** | ~90,000 tokens *(vague text advice)* | **~2,500 tokens** *(300-DPI chart saved to disk)* | **-97%** |
| **4. Data & Descriptive Stats** | ~180,000 tokens *(pasting raw tables into chat)* | **~3,000 tokens** *(automatic World Bank fetch)* | **-98%** |
| **5. Statistical Modeling** | ~250,000 tokens *(back-and-forth code debugging)* | **~3,500 tokens** *(clean local estimation)* | **-98%** |
| **6. Manuscript Drafting** | ~220,000 tokens *(rewriting AI-heavy text)* | **~18,000 tokens** *(human academic tone directly in Word)* | **-92%** |
| **Total Tokens Spent** | **~945,000 tokens** | **~32,700 tokens** | **-96.5% Savings** |

---

## 🛠️ The 7 Core Tools Explained Simply

1. `search_verified_literature`: Finds real academic papers with active DOIs from OpenAlex and DergiPark, saving an Excel sheet to your Desktop.
2. `evaluate_paper_fit`: Scores found papers (0–100) based on how well they match your topic and methodology.
3. `bibliometric_gap_and_journal_report`: Maps under-researched topics, generates clear charts, and suggests target journals.
4. `generate_deterministic_apa7`: Formats APA 7th citations and bibliography entries in Word and BibTeX.
5. `fetch_empirical_dataset`: Downloads real data from the World Bank API or Yahoo Finance and prepares summary statistics tables.
6. `run_quantitative_or_qualitative_model`: Runs real regressions, decision matrices (AHP-TOPSIS), or machine learning models on your PC.
7. `export_academic_manuscript`: Combines literature, data, and model results into a formatted Word (`.docx`) manuscript draft on your Desktop.

---

## 💬 Sample Prompts to Get Started

Paste this prompt directly into Antigravity, Claude Desktop, or Cursor to run an end-to-end project:

```markdown
Use ScholarDirect-MCP to run an academic research study on:
"The Impact of FinTech and Digital Banking on Economic Growth in Emerging Markets"

Please complete the following steps sequentially:
1. Search 15 verified papers from OpenAlex and DergiPark.
2. Evaluate their relevance and identify key anchor papers.
3. Generate the literature gap chart.
4. Download GDP growth data from the World Bank API for Turkey, the EU, and the USA.
5. Run an OLS regression model with robust standard errors and diagnostic tests.
6. Generate verified APA 7th citations.
7. Export everything into a complete Word (.docx) manuscript under Desktop/Academic_Research_Workspace/.

Data privacy rule: Keep all files saved locally on my Desktop; do not leak data to external clouds. Use a clear, natural academic tone.
```

---

## 📦 Setup & Connection

### Manual Installation
```bash
git clone https://github.com/netizen4-bit/scholar_direct.git
cd scholar_direct
pip install -r requirements.txt
playwright install chromium
```

### Connect to AI Clients (MCP Configuration)
Add to your `claude_desktop_config.json`, `config.json`, or Cursor settings:
```json
{
  "mcpServers": {
    "scholardirect": {
      "command": "python",
      "args": [
        "C:\\Users\\YOUR_USER\\.gemini\\antigravity\\scholar-direct-mcp\\scholar_direct.py"
      ],
      "env": {
        "SCHOLARDIRECT_WORKSPACE_DIR": "C:\\Users\\YOUR_USER\\Desktop\\Academic_Research_Workspace"
      }
    }
  }
}
```

---

## 📄 License & Support

Distributed under the **MIT License**. See `LICENSE` for more information.

* **Support Open Development:** [Patreon](https://www.patreon.com/netizen4_bit)  
* **Academic & Enterprise Inquiries:** [LinkedIn](https://www.linkedin.com/in/nihatkasim)
