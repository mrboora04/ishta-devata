# Ishta Devata

Which character walks with you? An 8-question quiz, in English and Hindi, that matches you to one of 55 gods, heroes, sages and asuras from the Ramayana, the Mahabharata, the Puranas and the Upanishads, shown as a collectible card with its story, beliefs, turning points and facts.

Live site: https://mrboora04.github.io/ishta-devata/

## How it's organised

| File | What it holds |
|---|---|
| `index.html` | The whole app: design, animations, quiz logic |
| `data/characters.json` | The 55 characters: name, Devanagari, rarity, light/shadow/lesson, and their profile on 8 qualities |
| `data/questions.json` | The question bank (55 questions, 8 asked per person) |
| `data/hi/` | The Hindi text: `characters.json` (card text by id), `questions.json` (same order as the English file) and `stories/` |
| `data/stories/<id>.json` | Each character's story, beliefs, turning points and facts, loaded only when someone draws that card |
| `og-image.jpg` | The preview image WhatsApp, Telegram and others show for the link |

## Adding content

- **More facts or a longer story:** edit that character's file in `data/stories/`. Nothing else changes.
- **A new question:** add it to `data/questions.json`. Each answer lists how much it moves the 8 qualities: `dev` (devotion), `dha` (dharma), `jna` (wisdom), `fie` (fire), `ego`, `bond` (attachment), `joy`, `cun` (cunning), each from -2 to 2.
- **A new character:** add it to `data/characters.json` with a profile `p` of 8 numbers in the same order, and create `data/stories/<id>.json`.
- **Hindi:** every English addition needs its Hindi twin in `data/hi/`. A missing Hindi line falls back to English for questions. Hindi answers are written in a gender-neutral style ("उसे निभाना", not "निभाता हूँ") so they read right for everyone.

## Languages

The site picks Hindi for browsers set to Hindi, and anyone can switch with the button at the top right. Links carry the language: `?lang=hi` opens the Hindi version, so a shared Hindi card opens in Hindi.

## Card ranks

Rarities use the Mahabharata's own ranking of warriors: Ardharathi, Rathi, Atirathi, Maharathi and Atimaharathi.
