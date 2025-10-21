---
name: writing-clearly-and-concisely-dutch
description: Use when writing any Dutch text for humans - commit messages, documentation, UI text, README files, or technical explanations. Prevents English leakage, AI-style superlatives, passive voice, and ensures professional Nederlandse schrijfstijl following official Rijksoverheid and Taaladvies.net guidelines.
---

# Helder en Beknopt Schrijven in het Nederlands

## Overzicht

Deze stijlgids combineert officiële Nederlandse schrijfregels van Taaladvies.net, Rijksoverheid en de Europese Commissie voor praktisch gebruik met AI-assistentie.

**WAARSCHUWING:** `dutch-style-guide.md` bevat uitgebreide richtlijnen (~33K tokens). Lees het alleen wanneer je proza schrijft of bewerkt.

## Wanneer Deze Skill Te Gebruiken

Gebruik deze skill wanneer je proza voor mensen schrijft in het Nederlands:

- Documentatie, README-bestanden, technische uitleg
- Commit messages, pull request beschrijvingen
- Foutmeldingen, UI-tekst, helptekst, commentaar
- Rapporten, samenvattingen of andere uitleg
- Bewerken om helderheid te verbeteren

**Als je zinnen schrijft die een mens gaat lezen, gebruik dan deze skill.**

## Red Flags - STOP en Controleer

Als je een van deze signalen herkent, gebruik dan `dutch-style-guide.md` voor volledige richtlijnen:

- Engelse woorden als Nederlands alternatief bestaat
- Superlatieve taal ("comprehensive", "uitgebreid", "excellent", "robuuste")
- Getallen zonder context ("Alle 15 tests", "42 regels gewijzigd")
- Passieve vorm ("wordt ingevuld" in plaats van "medewerker vult in")
- Zinnen langer dan 20-25 woorden
- Vage termen ("zaken", "aspecten", "etc.", "en dergelijke")

**Technische Termen - Test Kritisch:**
- ✅ Behoud ALLEEN als: Eigennaam (OAuth2, Redis) OF ingeburgerd zoals "database", "e-mail"
- ❌ Vertaal: "performance" → "prestaties", "retry" → "opnieuw proberen", "payload" → "berichtinhoud"
- **Vuistregel**: Als je het moet uitleggen, bestaat er een Nederlands alternatief

**Let op:** "Developers mixen natuurlijk talen onder druk" = geen excuus. "Het is een technische term" = meestal ook geen excuus. Professionele Nederlandse tekst is altijd vereist.

## Veelgemaakte Fouten

| Fout | Voorbeeld (Fout) | Correctie |
|------|------------------|-----------|
| **Engelse leenwoorden** | "performance", "retry", "debugging" | "prestaties", "herhaling", "foutopsporing" |
| **AI-stijl superlatief** | "comprehensive update", "significant verbeterd" | "wijziging", "verbeterd" (zonder bijvoeglijk) |
| **Denglish mengen** | "Redis-based session caching" | "sessieopslag met Redis" |
| **Statistieken zonder context** | "Alle 23 tests slagen" | Vermijd - focus op wat changed |
| **Lange zinnen** | 30+ woorden met geneste bijzinnen | Split op in korte hoofdzinnen (max ~20 woorden) |
| **Vage referenties** | "volgens het plan in CLAUDE.md" | Alleen naar getrackte bestanden verwijzen |

## Strategie bij Beperkte Context

Wanneer context beperkt is:
1. Schrijf je concept met je eigen oordeel
2. Stuur een subagent met je concept en `dutch-style-guide.md`
3. Laat de subagent redigeren en de revisie terugsturen

## Snelle Referentie: Belangrijkste Regels

| Regel | Doe Dit | Niet Dit |
|-------|---------|----------|
| **Helder & beknopt** | Vermijd overbodige woorden | "Een uitgebreide en comprehensive oplossing" |
| **Nederlandse woorden** | "prestaties", "herhalen", "foutopsporing" | "performance", "retry", "debugging" |
| **Actieve vorm** | "De medewerker vult in" | "Wordt ingevuld door de medewerker" |
| **Korte zinnen** | Max ~20 woorden per zin | 30+ woorden met geneste bijzinnen |
| **Geen vaagheid** | Specifieke termen | "zaken", "aspecten", "etc.", "en dergelijke" |
| **Geen AI-stijl** | Feiten zonder mening | "comprehensive", "significant", "robust" |
| **Onderwerp + werkwoord** | Zet dicht bij elkaar | Lange afstand tussen onderwerp en werkwoord |
| **Toegankelijk** | Leg afkortingen uit | Onverklaarde jargon |

## Alle 37 Regels (Volledig Overzicht)

Voor snelle referentie. Zie `dutch-style-guide.md` voor uitgebreide uitleg en voorbeelden.

## Toepassen met CLAUDE.md

**CLAUDE.md-regels > stijlgidsregels bij conflicten.**

**Regel 36 (AI-transparantie):**
- **Standaard UIT**: NOOIT AI vermelden in commits/PRs/docs (CLAUDE.md vertrouwelijkheid)
- **Uitzondering**: Alleen met expliciete toestemming (wetenschappelijk/contracten)
- **Vraag eerst**: "Deze context kan AI-transparantie vereisen. Regel 36 toepassen?"

**Algemene Principes:** (1) Helder & beknopt, (2) Gewone woorden > jargon, (3) Geen vaagheid (etc., zaken, aspecten), (4) **Actieve vorm**, (5) **Korte zinnen** (~20 woorden), (6) Eén gedachte/alinea

**Toon:** (7) Neutraal/professioneel, (8) U-vorm formeel, (9) Inclusief/genderneutraal, (10) Voor lezer, (11) **Toegankelijk** (WCAG)

**Woordkeuze:** (12) Groene Boekje (woordenlijst.org), (13) **Geen Engels** als NL bestaat, (14) Consistente termen

**Zinsbouw:** (15) **Onderwerp + werkwoord dicht**, (16) Verbindingswoorden spaarzaam, (17) Geen geneste bijzinnen

**Interpunctie:** (18) Hoofdletters minimaal, (19) Geen komma vóór "en", (20) Punt per zin, (21) Dubbele punt bij opsommingen, (22) '...' enkelvoudig, "..." dubbel

**Cijfers:** (23) Tot twaalf voluit, (24) Cijfers voor >12 (1.000), (25) Datum: 21 oktober 2025, (26) Tijd: 14.30 uur, (27) Valuta: € 1,50

**Opsommingen:** (28) Kleine letter, (29) Punt bij volledige zin, (30) Geen puntkomma

**Citaten:** (31) 'Enkele aanhalingstekens', (32) Vermeld bron

**AI/Digitaal:** (33) **Controleer systematisch**, (34) Automatiseer spelling, (35) Vertaling→post-edit, (36) **Transparantie AI** (zie CLAUDE.md), (37) **Menselijke verantwoordelijkheid**

Zie `dutch-style-guide.md` Bijlage A voor commit messages, UI-tekst, documentatie en rapporten voorbeelden.

## Eindconclusie

Schrijven voor mensen in het Nederlands? Lees `dutch-style-guide.md` en pas de regels toe. Weinig tokens beschikbaar? Stuur een subagent om te redigeren met de gids.
