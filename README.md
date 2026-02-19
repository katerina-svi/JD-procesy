# Proces: Změna / zrušení představení — Jihočeské divadlo

> **Interaktivní BPMN diagram** — mapování AS-IS procesu z digitálního auditu 2025/2026

[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-blue?style=flat-square)](https://TVUJ-USERNAME.github.io/jd-bpmn-audit/)

![Screenshot](screenshot.png)

---

## 🚀 Spuštění

### Varianta 1: GitHub Pages (doporučeno)
1. Forkněte / naklonujte tento repozitář
2. V Settings → Pages zapněte GitHub Pages z větve `main`
3. Diagram bude dostupný na `https://TVUJ-USERNAME.github.io/jd-bpmn-audit/`

### Varianta 2: Lokálně
```bash
git clone https://github.com/TVUJ-USERNAME/jd-bpmn-audit.git
cd jd-bpmn-audit
# Otevřete index.html v prohlížeči — žádný build nepotřebujete
open index.html
```

Žádné závislosti, žádný build, žádný framework. Čistý HTML + SVG + vanilla JS.

---

## 📊 Co diagram zobrazuje

Mapování současného procesu (AS-IS) zpracování změny termínu nebo zrušení představení v Jihočeském divadle. Data pochází z **17 kvalitativních rozhovorů** a **dotazníkového šetření** (40 respondentů).

### Aktéři (6 swim lanes)

| Pool | Role | Klíčová osoba |
|------|------|---------------|
| **Iniciátor změny** | Režisér, šéf souboru, produkční | Kdokoli |
| **Vedení** | Schvalování kritických změn | Ředitelka Schlegelová |
| **Produkční souborů** | Posouzení, eskalace, informování | Krejčová, Ondrová, Prašničková |
| **Milena Chumlenová** | Centrální bod — zápis do Fermana | Milena Chumlenová |
| **UTP** | Příjem informací, úprava práce | Bajzeková, mistři |
| **Doprava** | Přeplánování dopravy | Bajzeková |

### Interakce
- **Scroll** = zoom
- **Drag** = posun
- **Hover** na úkol = detail procesu a identifikovaný problém
- **Tab „Problémy"** = přehled všech 8 problémů

---

## ⚠️ Identifikované problémy

| # | Problém | Dopad |
|---|---------|-------|
| P1 | Nestrukturovaný vstup změny (telefon/mail/WA/osobně) | Riziko ztráty informace |
| P2 | Single point of failure — zápis pouze Milena | Zastavení procesu při nepřítomnosti |
| P3 | Ruční přepis do 5+ nepropojených systémů | 5–10 h/týden, nekonzistence dat |
| P4 | Chybí formalizovaná kategorizace závažnosti | Chaotické řízení změn |
| P5 | Ferman nemá notifikace | Zaměstnanci neví o změnách |
| P6 | Chybí potvrzení přijetí informace | Nikdo neví, kdo o změně ví |
| P7 | Krátký plánovací horizont (1 týden) | Nemožnost plánovat dopředu |
| P8 | Opakované zkoušky se zadávají ručně | Zbytečná práce a chyby |

---

## 📁 Struktura repozitáře

```
├── index.html          # Interaktivní diagram (standalone, zero dependencies)
├── zmena-predstaveni.bpmn   # BPMN 2.0 XML (pro Camunda Modeler / bpmn.io)
└── README.md
```

### BPMN soubor
Soubor `zmena-predstaveni.bpmn` lze otevřít v:
- [bpmn.io demo](https://demo.bpmn.io/) — přetáhněte do prohlížeče
- [Camunda Modeler](https://camunda.com/download/modeler/) — desktop
- VS Code s [BPMN Editor](https://marketplace.visualstudio.com/items?itemName=nicecatch.vscode-bpmn-editor)

---

## 🔗 Vazba na doporučení auditu

| ID | Doporučení | Priorita |
|----|-----------|----------|
| C2.4 | Ferman — audit, integrace, optimalizace | 1 |
| C3.1 | Master tabulka a synchronizace dat | 1 |
| C4.1 | Týmová pravidla komunikace | 1 |
| C4.2 | Proces informování o změnách | 1 |
| C4.3 | Digitální infotabule a nástěnky | 2 |
| C7.1 | Dokumentace kritických procesů | 2 |
| C1.3 | Propojení tabulek pomocí vzorců | 1 |

---

## Licence

Součást digitálního auditu Jihočeského divadla 2025/2026.  
Zpracovala: **Mgr. Kateřina Švidrnochová** · katerina@svidrnochova.cz
