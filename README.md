# English Textbook Data

Public JSON data for Grade 8 / Grade 9 English textbook units. Intended for voice agents, study tools, and the private [english](https://github.com/Jinni73/english) learning app (via git submodule at `books/`).

## Layout

```
Grade 9 Book/units/
├── Unit_01.json              # Vocabulary (source of truth)
├── Unit_02.json
├── listening/Unit_01.json    # Listening conversation scripts
└── word-links/
    ├── Unit_01.compounds.json
    └── Unit_01.derivations.json
```

## Raw URLs (voice agents)

Replace branch `main` if you use another default branch.

**Grade 9 Unit 1 vocabulary**

```
https://raw.githubusercontent.com/Jinni73/english-textbook/main/Grade%209%20Book/units/Unit_01.json
```

**Grade 9 Unit 1 listening**

```
https://raw.githubusercontent.com/Jinni73/english-textbook/main/Grade%209%20Book/units/listening/Unit_01.json
```

**Grade 8 Unit 7 vocabulary**

```
https://raw.githubusercontent.com/Jinni73/english-textbook/main/Grade%208%20Book/units/Unit_07.json
```

## Vocabulary JSON shape

Each `Unit_XX.json` file:

```json
{
  "unit": 1,
  "title": "Unit 1",
  "vocabulary": [
    {
      "id": 1,
      "english": "bring about",
      "pronunciation": "",
      "partOfSpeech": "phrase",
      "chinese": "带来；引起",
      "example_sentence": "This policy will bring about significant changes.",
      "essential": false
    }
  ]
}
```

## Audio

MP3 files are **not** stored in this repo. They are generated locally with the private app's TTS scripts and bundled at build time.

## License

Personal study materials extracted from school textbooks. Public JSON access is provided for integration with learning tools only.
