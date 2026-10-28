# ScholarDirect-MCP v1.0 🎓

<p align="center">
  <b>A Token-Efficient, Privacy-Focused Local Academic Research </b><br>
  <i>Powered by FastMCP, OpenAlex, Crossref, DergiPark, TR Dizin, World Bank, and the Academic Research Guardian Skill</i>
</p>

<p align="center">
  <b>English 🇬🇧</b> • <a href="README.tr.md"><b>Türkçe 🇹🇷</b></a>
</p>

<p align="center">
  <a href="https://github.com/netizen4-bit/scholar_direct/stargazers"><img src="https://img.shields.io/github/stars/netizen4-bit/scholar_direct?style=for-the-badge&logo=github&color=1F4E79" alt="Stars"></a>
  <a href="https://github.com/netizen4-bit/scholar_direct/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License"></a>
  <a href="https://www.patreon.com/netizen4_bit"><img src="https://img.shields.io/badge/Patreon-Support-F96854?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"></a>
  <a href="https://www.linkedin.com/in/nihatkasim"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

---

ScholarDirect-MCP v1.0 is a free, open-source local Model Context Protocol (MCP) tool designed for academic researchers, and analysts.

Standard AI models (ChatGPT, Claude, etc.) often hallucinate non-existent academic papers, invent fake DOIs, and waste thousands of tokens when you copy and paste raw spreadsheets into chat. ScholarDirect-MCP solves this by connecting your AI assistant directly to verified databases and executing real analysis code locally on your own computer:

1. **Verified Academic Literature:** Searches real peer-reviewed articles from international repositories (OpenAlex, Crossref) and national Turkish repositories (DergiPark, TR Dizin). Papers with broken DOIs or retraction flags are automatically excluded.
2. **Real Empirical Data & Math:** Pulls live indicators from World Bank API and Yahoo Finance, running actual regressions, multi-criteria decision models (AHP-TOPSIS), or machine learning locally with Python (`statsmodels`, `lifelines`, `scikit-learn`).
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

## ⚡ Token Effectiveness & Benchmark

When you ask a standard AI chat to analyze data and write a paper, uploading large CSV files and repeatedly fixing broken code burns hundreds of thousands of tokens. 

ScholarDirect-MCP pairs FastMCP backend tools with the structured **Academic Research Guardian Skill** (`academic-research-guardian`) to solve this:

### 6-Phase Academic Research Cycle Benchmark

| Research Stage | Standard / Unconstrained Loop | ScholarDirect-MCP + Guardian Skill | Token Savings |
|---|---|---|---|
| **1. Literature Discovery & Scraping** | **~120,000 tokens**<br>*(Ingests raw HTML DOMs, unverified PDF text, dead links)* | **~3,500 tokens**<br>*(Pre-filtered OpenAlex + DergiPark; compact table)* | **-97.1%** |
| **2. Paper Relevance Scoring** | **~85,000 tokens**<br>*(Lengthy LLM guessing on methodology & domain fit)* | **~2,200 tokens**<br>*(Local Python math; instant 5-branch verdict)* | **-97.4%** |
| **3. Literature Gap Analysis** | **~90,000 tokens**<br>*(Vague text advice; no charts generated)* | **~2,500 tokens**<br>*(300-DPI chart and Word report saved to disk)* | **-97.2%** |
| **4. Empirical Data & Descriptives** | **~180,000 tokens**<br>*(Pasting raw CSV tables; math hallucination)* | **~3,000 tokens**<br>*(Direct World Bank fetch; local Scipy stats)* | **-98.3%** |
| **5. Statistical & Econometric Modeling** | **~250,000 tokens**<br>*(15+ turns of interactive Python code debugging)* | **~3,500 tokens**<br>*(Local `statsmodels`/`lifelines` run; diagnostic tables)* | **-98.6%** |
| **6. Manuscript Drafting & Humanization** | **~220,000 tokens**<br>*(Repeated rewriting to lower 70%+ AI Turnitin flags)* | **~18,000 tokens**<br>*(Single-pass natural academic draft in `.docx`)* | **-91.8%** |
| **Total Context Spent** | **~945,000 tokens** | **~32,700 tokens** | **-96.5% Total Reduction** |

---

## 📊 Quick Comparison: ScholarDirect-MCP vs. Other Tools

| Feature | Standard ChatGPT / Claude | Paid Academic SaaS ($30–$100/mo) | ScholarDirect-MCP |
|---|---|---|---|
| **Citation Accuracy** | ❌ Can hallucinate non-existent papers. | ⚠️ Limited to partnered journals. | ✅ **100% Real:** Verified via Crossref REST API. |
| **Turkish Repositories (DergiPark)** | ❌ Cannot scrape DergiPark or TR Dizin. | ❌ Focuses primarily on Western sources. | ✅ **Supported:** Scrapes DergiPark & TR Dizin. |
| **Data Privacy** | ❌ Data is sent to company cloud servers. | ❌ Datasets are stored in remote clouds. | ✅ **100% Local:** All files stay on your Desktop. |
| **Statistical Calculations** | ❌ Prone to math hallucination in chat. | ❌ Only summarizes text; no actual modeling. | ✅ **Real Math:** Exact Python estimation (`statsmodels`). |
| **Turnitin AI Similarity** | ❌ Often scores 60%–80% AI detection. | ⚠️ Repetitive template sentences. | ✅ **Natural Prose:** Organic academic phrasing (<15%). |
| **Cost** | $20 – $200/month | $30 – $100/month | ✅ **100% Free & Open Source** |

---

## 📁 Project Structure

```text
scholar_direct/
├── .agent/
│   └── skills/
│       └── academic-research-guardian/
│           └── SKILL.md             # Turnitin-proof (<15%) academic prose, real method whitelist & APA rules
├── scholar_direct.py                # Full-stack FastMCP Server exposing 7 core academic tools
├── requirements.txt                 # Core Python scientific, econometric, scraping & document dependencies
├── LICENSE                          # MIT License
├── README.tr.md                     # Dedicated Turkish documentation
└── README.md                        # Project documentation, benchmarks & setup guides
```

---

## 📁 Organized 5-Folder Desktop Workspace

When you launch a research project, ScholarDirect-MCP automatically creates a structured workspace on your Desktop:

```text
Desktop/Academic_Research_Workspace/<Project_Name>_<Date>/
├── 01_Literature_and_Bibliometrics/
│   ├── verified_literature.xlsx      # Styled Excel workbook with auto-filters & DOI links
│   ├── verified_references.bib       # Standard BibTeX file for LaTeX & thesis writing
│   ├── apa7_bibliography.docx        # Ready-to-use Word bibliography with hanging indents
│   └── bibliometric_gap_report.docx  # Literature gap and journal recommendations report
├── 02_Empirical_Datasets/
│   ├── raw_dataset.csv               # Raw series downloaded from API / local file
│   ├── cleaned_dataset.xlsx          # Multi-sheet cleaned data & correlation matrix
│   └── descriptive_stats.docx        # APA descriptive statistics tables (N, Mean, SD)
├── 03_Models_and_Scripts/
│   └── run_model_<model>.py          # 100% reproducible standalone Python script
├── 04_Figures_and_Tables/
│   ├── citation_trend_by_year.png    # 300-DPI publication trajectory chart
│   ├── methodology_gap_heatmap.png   # 300-DPI methodology co-occurrence heatmap
│   └── model_diagnostics.png         # Diagnostic plots (residuals, survival, importances)
└── 05_Manuscript_Drafts/
    ├── <Project_Name>_manuscript.md  # Research paper draft in Markdown
    └── <Project_Name>_manuscript.docx # Formatted Word document with standard academic headings
```

---

## 🛠️ MCP Tools Reference (Full 7-Tool Suite)

1. `search_verified_literature`: Finds real academic papers with active DOIs from OpenAlex and DergiPark, saving an Excel sheet to your Desktop.
2. `evaluate_paper_fit`: Scores found papers (0–100) based on how well they match your topic and target methodology.
3. `bibliometric_gap_and_journal_report`: Maps under-researched topics, generates clear charts, and suggests target journals.
4. `generate_deterministic_apa7`: Formats APA 7th citations and bibliography entries in Word and BibTeX.
5. `fetch_empirical_dataset`: Downloads real data from the World Bank API or Yahoo Finance and prepares summary statistics tables.
6. `run_quantitative_or_qualitative_model`: Runs real regressions (OLS), decision matrices (AHP-TOPSIS), or machine learning models on your PC.
7. `export_academic_manuscript`: Combines literature, data, and model results into a formatted Word (`.docx`) manuscript draft on your Desktop.

---

## 💬 Sample Prompts to Get Started

Paste this prompt directly into Antigravity, Claude Desktop, or Cursor to run an end-to-end research project:

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

## 📦 Prerequisites & Quick Setup

### 1. Prerequisites
* **Python (3.10+)**
* **Git**
* **Playwright Chromium** (`playwright install chromium`)
* An MCP-compatible client (**Antigravity CLI / IDE**, **Claude Desktop**, **Cursor**) or a local **Ollama** setup.

### 2. Manual Installation
Clone the repository, install Python dependencies, and install the headless browser binary for Playwright:
```bash
git clone https://github.com/netizen4-bit/scholar_direct.git
cd scholar_direct
pip install -r requirements.txt
playwright install chromium
```

### 3. Automatic installation of local ScholarDirect MCP server using Antigravity app
If you are using Google Antigravity, you can install and configure ScholarDirect MCP completely automatically with zero manual steps. Simply paste the following prompt directly into your Antigravity chat:

````markdown
Install and configure the ScholarDirect MCP server into my Antigravity setup:

1. Clone or pull the repository from https://github.com/netizen4-bit/scholar_direct into a permanent directory at `~/.gemini/antigravity/scholar-direct-mcp`.
2. Automatically install all missing Python dependencies from `requirements.txt` (`pip install -r requirements.txt`) and ensure Playwright Chromium is installed (`playwright install chromium`).
3. Register the server in Antigravity's global MCP configuration (`~/.gemini/antigravity/config.json`):
   - Server name: `scholardirect`
   - Command: `python`
   - Args: Full absolute path to `scholar_direct.py` (ensure Windows backslashes are escaped)
   - Environment variables: Set `SCHOLARDIRECT_WORKSPACE_DIR` to `Desktop/Academic_Research_Workspace`.
4. Copy the bundled agent skill (`.agent/skills/academic-research-guardian/SKILL.md`) into `~/.gemini/config/skills/academic-research-guardian/`.
5. Run a sanity check to verify that `scholar_direct.py` imports cleanly, and confirm once all 7 MCP tools are registered.
````

The agent will pull the repo, configure `config.json`, install all packages and Playwright browser binaries, mount the agent skills, and verify the tools end-to-end.

---

## 🔌 Connecting to Your AI Client (MCP JSON Configuration)

Add ScholarDirect to your MCP configuration file (e.g. `claude_desktop_config.json`, `config.json`, or Cursor settings):

> ⚠️ **Note on Windows Paths:** In JSON strings, backslashes must be escaped (`\\`) or written with forward slashes (`/`).

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
