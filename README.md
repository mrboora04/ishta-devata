# Ishta Devata

Which character walks with you? An 8-question quiz that matches you to one of 49 gods, heroes, sages and asuras from the Ramayana, the Mahabharata and the Puranas, shown as a collectible card with its story, beliefs, turning points and facts.

Live site: https://mrboora04.github.io/ishta-devata/

## How it's organised

| File | What it holds |
|---|---|
| `index.html` | The whole app: design, animations, quiz logic |
| `data/characters.json` | The 49 characters: name, Devanagari, rarity, light/shadow/lesson, and their profile on 8 qualities |
| `data/questions.json` | The question bank (45 questions, 8 asked per person) |
| `data/stories/<id>.json` | Each character's story, beliefs, turning points and facts, loaded only when someone draws that card |
| `og-image.jpg` | The preview image WhatsApp, Telegram and others show for the link |

## Adding content

- **More facts or a longer story:** edit that character's file in `data/stories/`. Nothing else changes.
- **A new question:** add it to `data/questions.json`. Each answer lists how much it moves the 8 qualities: `dev` (devotion), `dha` (dharma), `jna` (wisdom), `fie` (fire), `ego`, `bond` (attachment), `joy`, `cun` (cunning), each from -2 to 2.
- **A new character:** add it to `data/characters.json` with a profile `p` of 8 numbers in the same order, and create `data/stories/<id>.json`.

## Card ranks

Rarities use the Mahabharata's own ranking of warriors: Ardharathi, Rathi, Atirathi, Maharathi and Atimaharathi.
