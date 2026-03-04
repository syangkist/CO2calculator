# 탄소 배출량 계산기 / Carbon Footprint Calculator
*Built by Claude Opus 4.6 and Claude Sonnet 4.6*
*Not everything is 100% confirmed*


**나의 연간 탄소 발자국을 계산하고, 어디에 집중해야 할지 알아보세요.**  
*Calculate your annual carbon footprint and find out where to focus.*


---

## Features / 주요 기능

| Tab | Korean | Description |
|-----|--------|-------------|
| Overview | 개요 | Compare your footprint vs Korea & world average |
| My Data | 입력 | Enter your transport, housing, flights & diet |
| Levers | 감축 | See which actions move the most tonnes |
| Small Steps | 작은 실천 | Everyday actions ranked by impact |
| Offset | 상쇄 | Offset costs and portfolio examples (2025 market prices) |

**Other features:**
- 🇰🇷 / EN bilingual toggle (persists across sessions)
- Live header updates as you adjust sliders
- National impact projection (if all 51.7M Koreans lived like you)
- NDC 2030 target gap calculator
- Offset portfolio builder with 2025 market prices (REDD+, ARR, Biochar, DAC, ERW)

---

## Methodology / 계산 방법

All emissions are in **tCO₂e per person per year**.

| Sector | Method | Source |
|--------|--------|--------|
| Transport | `km × (emission factor / efficiency) / occupants` | IPCC |
| Heating | `pyeong × gas factor × months × temp modifier / household` | Climate Transparency 2022 |
| Cooling & Electricity | `area-based kWh × grid intensity / household` | KEA, Climate Transparency |
| Hot water | `showers/week × 52 × gas factor / household` | IPCC |
| Aviation | `distance × RFI-adjusted EF × trips` | ICAO / Our World in Data |
| Diet | `kg/week × 52 × livestock EF` | IPCC AR6 |
| Fixed (infrastructure) | `6.0 t` flat (uncontrollable, Korea avg) | Worldometer 2022 |

**Key emission factors:**
- Korea grid: **420 g CO₂/kWh** (Climate Transparency 2022)
- City gas (LNG): **2.1 kg CO₂/Nm³** (IPCC)
- Gasoline: **2.31 kg CO₂/L** · Diesel: **2.68 kg CO₂/L**
- Beef: **27 kg CO₂e/kg** · Pork: **12.1** · Chicken: **6.9**

---

## Usage / 사용법

No installation or build step required. Just open `index.html` in a browser.

```bash
git clone https://github.com/[your-username]/carbon-calculator
cd carbon-calculator
open index.html   # or double-click the file
```

To deploy on GitHub Pages:
1. Push `index.html` to the `main` branch root
2. Go to **Settings → Pages → Deploy from branch → main / root**
3. Your app goes live at `https://[your-username].github.io/carbon-calculator`

---

## Files

```
carbon-calculator/
├── index.html          # Self-contained app (React via CDN, no build needed)
└── README.md
```

---

## Data Sources (Not verified, it came from the Claude Opus 4.6)

- **Korea average (12.3 t):** Worldometer 2022, Global Carbon Project 2023
- **World average (4.7 t):** Global Carbon Project 2023
- **Grid intensity:** Climate Transparency 2022 — 411 g/kWh
- **Aviation EFs:** ICAO Carbon Calculator methodology
- **Livestock EFs:** IPCC AR6 WG3 Ch.7
- **Korea NDC:** 727 Mt (2018 baseline) → 436 Mt by 2030 (40% reduction target)
- **Offset prices (2025):** Sylvera, MSCI ARR Index, BCG, Senken, Green-e

---

## 🛠 Built With

- [React 18](https://react.dev/) (via CDN, no bundler)
- [Babel Standalone](https://babeljs.io/docs/babel-standalone) (in-browser JSX transform)
- Pure CSS-in-JS, no external UI library

---

## 👤 Author

**Sungeun Yang** — Principal Research Scientist, KIST  
Hydrogen Energy Materials Research Division · SSEMS Lab  
Seoul, Korea

---

## 📄 License

CC BY 4.0
