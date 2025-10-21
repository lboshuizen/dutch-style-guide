# Fabric Pattern: Improve Dutch Writing

This Fabric pattern analyzes and improves Dutch text according to the 37 rules from the Dutch Style Guide.

## What It Does

The pattern systematically checks Dutch text for violations and provides:

- **Improved text** — Corrected version following all rules
- **Change analysis** — Detailed breakdown of improvements made
- **Quality scores** — Ratings for clarity, professionalism, Dutch purity, conciseness
- **Recommendations** — Suggestions for further improvement

## Installation

### Copy to Fabric Patterns Directory

```bash
# From repository root
cp -r fabric-pattern ~/.config/fabric/patterns/improve_dutch_writing
```

### Verify Installation

```bash
fabric --list | grep improve_dutch_writing
```

## Usage

### Basic Usage

```bash
echo "Deze PR bevat comprehensive changes voor het fixen van issues" | fabric --pattern improve_dutch_writing
```

### From File

```bash
fabric --pattern improve_dutch_writing < commit-message.txt
```

### Save Output

```bash
fabric --pattern improve_dutch_writing < input.txt > output.txt
```

### With Stream (for longer texts)

```bash
fabric --pattern improve_dutch_writing --stream < documentation.md
```

## Example

**Input:**
```
Deze applicatie biedt comprehensive functionaliteit voor het managen van users
en het tracken van hun activities. Het is een robust solution die extensively
tested is.
```

**Output:**

### VERBETERDE TEKST
```
Deze applicatie beheert gebruikers en registreert hun activiteiten.
```

### ANALYSE VAN WIJZIGINGEN

**Belangrijkste verbeteringen:**

1. Engelse leenwoorden vervangen: `comprehensive functionaliteit` → geschrapt, `managen` → `beheert`, `users` → `gebruikers`, `tracken` → `registreert`, `activities` → `activiteiten`
2. Overbodige woorden geschrapt: `biedt`, `functionaliteit`
3. AI-stijl taal verwijderd: `robust solution`, `extensively tested` → geschrapt
4. Zinnen ingekort van 26 naar 9 woorden

**Gevonden problemen per categorie:**

- Engels naar Nederlands: 7 vervangingen
- AI-stijl verwijderd: 3
- Passief naar actief: 0
- Zinnen ingekort: 1
- Vage termen vervangen: 2
- Overbodige woorden verwijderd: ~5

### KWALITEITSBEOORDELINGEN

**Helderheid:** A - Tekst is direct en begrijpelijk
**Professionaliteit:** A - Geschikt voor professionele documentatie
**Nederlands puurheid:** 100% Nederlandse termen
**Beknoptheid:** 65% woordreductie (van 26 naar 9 woorden)

## What Gets Checked

The pattern enforces these rules:

1. **English loanwords** → Dutch alternatives
2. **Passive voice** → Active constructions
3. **AI-style language** → Factual statements
4. **Vague terms** → Concrete specifics
5. **Needless words** → Removed
6. **Long sentences** → Split to ~20 words max
7. **Inconsistent terminology** → Standardized

## Configuration

The pattern uses two files:

- **`system.md`** — Complete instructions and rules for the AI
- **`user.md`** — Simple template for input text

You can customize `system.md` to adjust:
- Which rules to prioritize
- Output format preferences
- Strictness level

## Reference

See [`../dutch-style-guide.md`](../dutch-style-guide.md) for all 37 rules with examples.

See [`system.md`](system.md) for the complete pattern implementation.

## Requirements

- [Fabric](https://github.com/danielmiessler/fabric) installed and configured
- Access to an AI provider (OpenAI, Claude, etc.)

## License

CC BY 4.0 — Same as the main guide.
