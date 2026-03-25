# Formability Website

> Se `~/.claude/CLAUDE.md` för övergripande Formability-kontext.

## Om detta repo
- **URL:** https://formability.se
- **Repo:** github.com/formability-se/website (public)
- **Stack:** Ren HTML/CSS/JS i en enda fil (`index.html`), inga ramverk
- **Hosting:** GitHub Pages

## Sektioner på sidan
1. **Nav** — logo + länkar + "Håll mig uppdaterad"-knapp
2. **Hero** — animerad logo, tagline, CTA-knapp, videoplats
3. **Logos-strip** — Autodesk Forma-logotyp
4. **Moduler** — 6 kort + "Saknar du en modul?"-knapp
5. **Extension-sektion** — mörk bakgrund, webbläsartillägget förklarat + mockup
6. **Proof** — 3 stats (0 nya system, 6 moduler, ∞ anpassningar)
7. **CTA** — "Redo att forma byggbranschen?" + "Håll mig uppdaterad"-knapp
8. **Footer**

## Formulär
Två formulär, båda via EmailJS med delade templates (gratisnivå = max 2 templates):

### "Håll mig uppdaterad" (kontakt)
- Fält: Namn*, Email*, Företag, Meddelande
- Autosvar: `message_body` = intresse-text
- Notis: `subject_line` = "Ny intresseanmälan från [namn]"

### "Saknar du en modul?" (modulförslag)
- Fält: Namn*, E-post*, Modulförslag*
- Autosvar: `message_body` = tack-för-förslag-text
- Notis: `subject_line` = "Nytt modulförslag från [namn]"

## EmailJS
- **Service ID:** `service_trk3ry1`
- **Public Key:** `TCG67WDH3_RPqu2Ut`
- **Template autosvar:** `template_t361sqj` (Auto-Reply typ, `{{message_body}}` för dynamisk text)
- **Template notis:** `template_nqhtnp3` (Content typ, `{{subject_line}}` för dynamisk subject)
- **Gratisnivå:** 200 req/mån, 2 templates
- **Säkerhet:** Nycklar i publik repo. "Allow non-browser API" av, "Use Private Key" på. Lägg till domänrestriktion vid uppgradering.

## Filer
- `index.html` — hela sidan (HTML + CSS + JS)
- `context.md` — detaljerad projektkontext (gitignored, stannar lokalt)
- `CLAUDE.md` — denna fil
- `.gitignore` — exkluderar context.md, .env, etc.
