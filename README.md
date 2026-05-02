# BHARAT·SIGNAL

**A leading-indicator-first equity signal board for Indian investors.**

> Separate project from BHARAT·MACRO. Focused on predictive signals, not just current data.

## What makes this different from BHARAT·MACRO

| BHARAT·MACRO | BHARAT·SIGNAL |
|---|---|
| 60+ coincident indicators | 18+ leading indicators as primary focus |
| 6 flat tabs | Signal Board as homepage |
| No composite scores | 3 composite scores (Leading / Coincident / Sentiment) |
| No yield curve | India + US yield curves with spread analysis |
| No forward estimates | FY26E / FY27E consensus estimates |
| No earnings revision ratio | Analyst upgrade/downgrade ratio |
| No capacity utilisation | RBI CU survey tracked |
| No MF cash levels | Dry powder indicator |
| No promoter pledge | Distress early warning |

## The 3 Signal Scores

| Score | What it measures | Lead time |
|---|---|---|
| **Leading Score** | PMI new orders, yield curve, credit impulse, revision ratio, PCR, A/D | 1–4 quarters |
| **Coincident Score** | GDP, CPI, repo rate, GST, bank credit, PMI headline | Current |
| **Sentiment Score** | VIX, FII futures OI, 200DMA position, Hi/Lo ratio, gold | 1–8 weeks |

**Overall signal = average of 3 scores → BUY / HOLD / REDUCE**

## Setup (5 minutes)

1. Create new GitHub repo: `bharat-signal` (Public)
2. Upload files maintaining folder structure from this ZIP
3. Settings → Secrets → Actions → `FRED_API_KEY` (free at fred.stlouisfed.org)
4. Settings → Pages → Branch: main / root
5. Actions → Refresh Signal Data → Run workflow (first run)

Dashboard: `https://your-username.github.io/bharat-signal`

## AI Analysis (free)
Get Groq key at console.groq.com → API Keys → free, no card needed
Paste in the key field at bottom of dashboard → click Analyse
Uses llama-3.3-70b · 14,400 requests/day free

## Folder structure
```
bharat-signal/
├── index.html                    ← Dashboard
├── data/macro.json               ← Updated by Actions
├── scripts/fetch_signal.py       ← Data fetcher
├── .github/workflows/refresh.yml ← 9AM + 3:30PM IST daily
└── requirements.txt
```
