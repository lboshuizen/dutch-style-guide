# Claude Code Skill: Dutch Writing

This Claude Code skill enforces the 37 rules from the Dutch Style Guide automatically when writing Dutch text.

## What It Does

The skill triggers when you write any Dutch prose and checks for common violations:

- **English loanwords** — Replaces `updaten` → `bijwerken`, `fixen` → `oplossen`, etc.
- **Passive voice** — Changes `wordt ingevuld` → `medewerker vult in`
- **AI-style language** — Removes superlatives, statistics without context, opinion words
- **Vague terms** — Replaces `diverse aspecten` with concrete specifics
- **Needless words** — Removes `in het geval dat` → `als`
- **Long sentences** — Enforces ~20 word maximum per sentence

## Installation

### Option 1: Copy to Claude Code Skills Directory

```bash
cp -r examples/claude-code-skill ~/.claude/skills/dutch-writing
```

### Option 2: Symlink (for development)

```bash
ln -s $(pwd)/examples/claude-code-skill ~/.claude/skills/dutch-writing
```

## Usage

The skill activates automatically when you write Dutch text in Claude Code:

- Commit messages
- Documentation (README, API docs, guides)
- UI text (error messages, notifications, help text)
- Business communication (reports, emails)
- Code comments

### Example

**Before (with violations):**
```
Fix issue met checken van empty fields en updaten van de database
```

**After (skill applied):**
```
Voeg validatie toe voor lege velden en werk database bij
```

## What Gets Checked

The skill enforces these critical rules:

### 1. No English Loanwords
- ❌ `updaten`, `checken`, `fixen`
- ✅ `bijwerken`, `controleren`, `oplossen`

### 2. Active Voice
- ❌ `Het formulier wordt ingevuld`
- ✅ `De medewerker vult het formulier in`

### 3. No AI-Style Language
- ❌ `comprehensive solution`, `significant improvement`
- ✅ Specific facts and details

### 4. Concrete Language
- ❌ `diverse aspecten en mogelijkheden`
- ✅ `gebruikersbeheer met rollen en rechten`

### 5. Short Sentences
- ❌ 35-word sentences with nested clauses
- ✅ ~20 words maximum, clear structure

### 6. No Needless Words
- ❌ `in het geval dat`, `met betrekking tot`
- ✅ `als`, `over`

## Reference

See [`SKILL.md`](SKILL.md) for the complete skill implementation.

See [`../../dutch-style-guide.md`](../../dutch-style-guide.md) for all 37 rules with examples.

## License

CC BY 4.0 — Same as the main guide.
