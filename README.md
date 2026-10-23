# Canto Deck

A Cantonese flashcard deck: flip-card practice and a word list, with Jyutping, two example sentences per word, tappable words in examples, and spoken pronunciation.

## Files

- `index.html` – the deck page. It runs as a Claude artifact on claude.ai, where it loads cards from the artifact's database and can add new cards by asking Claude.
- `cards.json` – a backup of every card (deck, characters, Jyutping, meaning, examples).
- `decks.json` – the list of decks. Each card's `deck` field is one of these ids.

## Card format

```json
{
  "deck": "test",
  "han": "湖",
  "jp": "wu4",
  "en": "lake",
  "ex": [
    { "tok": ["公園", "入面", "有", "個", "好", "靚", "嘅", "湖", "。"], "jp": "gung1 jyun2 ...", "en": "There's a beautiful lake in the park." }
  ]
}
```

`tok` is the sentence split into words, with each punctuation mark as its own item.

## Audio

Pronunciation uses the device's text-to-speech with a Cantonese (Hong Kong) voice. Browsers like Chrome and Edge include one; the Claude desktop app needs a Cantonese voice installed in the operating system.
