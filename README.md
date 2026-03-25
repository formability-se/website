# formability

**The skin and heart of Forma.**

Formability bäddar in direkt i Autodesk Forma och förstärker plattformen med verktyg byggda specifikt för byggbranschens vardag — utan nya inloggningar, utan nya system.

---

## Vad är Formability?

Formability är ett ekosystem av fokuserade moduler som lever inuti Autodesk Forma via ett webbläsartillägg. Varje modul gör en sak riktigt bra — och hänger ihop med de andra.

```
Modell → Kontrollplan → Formulär → Ärenden → Dagbok → Rapport → Modell
```

---

## Moduler

| Modul | Beskrivning | Status |
|-------|-------------|--------|
| **Project Home** | Anpassningsbar startsida per projekt och roll | 🔨 Under utveckling |
| **Formulärbyggaren** | Egenkontroller, besiktningsprotokoll, checklistor | 🔨 Under utveckling |
| **Ärendetavlan** | Kanban, kalender och listvy för avvikelser | 📋 Planerad |
| **Dagboken** | Digital byggdagbok enligt PBL-krav | 📋 Planerad |
| **Kontrollplanen** | Digitala kontrollprogram kopplade till BIM-objekt | 📋 Planerad |
| **Modellvalideraren** | IFC-validering mot projektspecifika krav | 📋 Planerad |

---

## Webbläsartillägget

Kärnan i Formability är ett Chrome-tillägg som bäddar in två ytor direkt i Forma:

- **Navigator** — en kontextuell sidopanel med snabbåtkomst till alla moduler, per projekt, per roll
- **Project Home overlay** — ersätter Formas standardvy med en konfigurerbar dashboard

---

## Repo-struktur

```
formability/
├── website/          # Formability.se
├── extension/        # Chrome-tillägget (navigator + overlay)
├── modules/
│   ├── project-home/
│   ├── forms/
│   ├── issues/
│   ├── diary/
│   ├── control-plan/
│   └── model-validator/
├── shared/           # Delade komponenter, typer, API-klienter
└── docs/             # Arkitektur, beslut, API-specifikationer
```

---

## Tech stack

| Lager | Val |
|-------|-----|
| Frontend | React + TypeScript |
| Tillägg | Chrome Extensions Manifest V3 |
| Backend | Railway (EU-region) |
| Databas | Supabase (Frankfurt) |
| Hosting | Vercel (frontend) + Railway (workers/agents) |
| AI-agenter | Anthropic Claude via MCP |
| BIM-integration | Autodesk Forma API + ACC API + IFC.js |

---

## Kom igång

> Formability är under aktiv utveckling. Kostnadsfri provperiod lanseras snart.

Håll dig uppdaterad på [formability.se](https://formability.se)

---

## Licens

Proprietär — © 2025 Formability. Alla rättigheter förbehållna.
