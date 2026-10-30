# India-Stocks-2371-2400-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2371 to 2400)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2371-2400-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2371 to 2400)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2371 | `TARMAT` | Tarmat Limited | `TARMAT.NS` |
| 2372 | `TARSONS` | Tarsons Products Limited | `TARSONS.NS` |
| 2373 | `TASTYBITE` | Tasty Bite Eatables Limited | `TASTYBITE.NS` |
| 2374 | `TATVA` | Tatva Chintan Pharma Chem Limited | `TATVA.NS` |
| 2375 | `TBZ` | Tribhovandas Bhimji Zaveri Limited | `TBZ.NS` |
| 2376 | `TCC` | TCC Concept Limited | `TCC.NS` |
| 2377 | `TCI` | Transport Corporation of India Limited | `TCI.NS` |
| 2378 | `TCIEXP` | TCI Express Limited | `TCIEXP.NS` |
| 2379 | `TCIFINANCE` | TCI Finance Limited | `TCIFINANCE.NS` |
| 2380 | `TCPLPACK` | TCPL Packaging Limited | `TCPLPACK.NS` |
| 2381 | `TEAMGTY` | Team India Guaranty Limited | `TEAMGTY.NS` |
| 2382 | `TEAMLEASE` | Teamlease Services Limited | `TEAMLEASE.NS` |
| 2383 | `TECHNOCRAF` | Technocraft Ventures Limited | `TECHNOCRAF.NS` |
| 2384 | `TECHNVISN` | TechNVision Ventures Limited | `TECHNVISN.NS` |
| 2385 | `TECILCHEM` | TECIL Chemicals and Hydro Power Limited | `TECILCHEM.NS` |
| 2386 | `TEMBO` | Tembo Global Industries Limited | `TEMBO.NS` |
| 2387 | `TEMPSENS` | Tempsens Instruments (India) Limited | `TEMPSENS.NS` |
| 2388 | `TERAI` | Terai Tea Company Limited | `TERAI.NS` |
| 2389 | `TERASOFT` | Tera Software Limited | `TERASOFT.NS` |
| 2390 | `TEXINFRA` | Texmaco Infrastructure & Holdings Limited | `TEXINFRA.NS` |
| 2391 | `TEXMOPIPES` | Texmo Pipes and Products Limited | `TEXMOPIPES.NS` |
| 2392 | `TEXRAIL` | Texmaco Rail & Engineering Limited | `TEXRAIL.NS` |
| 2393 | `TFCILTD` | Tourism Finance Corporation of India Limited | `TFCILTD.NS` |
| 2394 | `TFL` | Transwarranty Finance Limited | `TFL.NS` |
| 2395 | `TGBHOTELS` | TGB Banquets And Hotels Limited | `TGBHOTELS.NS` |
| 2396 | `TGVSL` | TGV Sraac Limited | `TGVSL.NS` |
| 2397 | `THACKER` | Thacker & Company Limited | `THACKER.NS` |
| 2398 | `THAKDEV` | Thakkers Developers Limited | `THAKDEV.NS` |
| 2399 | `THEINVEST` | The Investment Trust Of India Limited | `THEINVEST.NS` |
| 2400 | `THEJO` | Thejo Engineering Limited | `THEJO.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream TARMAT 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2371-2400-Historical-Data/main/TARMAT/1m/2026/10/TARMAT_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
