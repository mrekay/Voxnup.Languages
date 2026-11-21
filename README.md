# Voxnup Languages

Open translation files for the **Voxnup** app. Every string you see in Voxnup lives here as a JSON key, so anyone can spot a wrong translation, fix it, or help add a new language.

## Languages

| Code | Language | Keys | Status |
|---|---|---|---|
| `en` | English | 2993 | Complete (reference) |
| `tr` | Türkçe | 2993 | Complete |
| `de` | Deutsch | 1862 | 1131 keys missing |
| `ru` | Русский | 1862 | 1131 keys missing |
| `az` | Azərbaycan | 1862 | 1131 keys missing |

Missing keys fall back to English in the app.

## File format

Each language is a single file named after its code (`en.json`, `tr.json`, ...). The file holds an array with one object of `KEY: "text"` pairs:

```json
[
  {
    "ALREADY_FRIEND": "This person is already your friend!",
    "TYPING_ONE": "%s is typing...",
    "TYPING_TWO": "%s and %s are typing..."
  }
]
```

Rules:

- `en.json` is the reference. Every key in it should exist in the other files, and other files should not add keys of their own.
- Translate only the values. Never rename or remove keys.
- Keep placeholders such as `%s` exactly as they are, and in the same count.
- Save files as UTF-8.

## Contributing

1. Fork the repository and edit the language file you want to fix.
2. Check that the JSON is still valid and placeholders are unchanged.
3. Open a pull request describing what you changed.

Found a bad translation but don't want to edit it yourself? Open an issue with the key name and the suggested text.

To add a new language, copy `en.json` to `<code>.json` and translate the values. If you'd like to join as a regular collaborator, contact us through Voxnup.

## Tools

`Voxnup.Languages.lslp` is the project file for [LS Language Studio](https://github.com/mrekay/LS-Language-Studio), which gives you a side-by-side editor for all languages.

Project LSLP version: 1.7
