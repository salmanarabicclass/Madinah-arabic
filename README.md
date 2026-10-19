# Madinah Arabic Vocabulary

Flashcards and quizzes for the vocabulary in Madinah Arabic Book One.

The whole app is one self-contained file: `index.html`. It needs no build step. Open it in a browser, or serve it with GitHub Pages.

## Updating the vocabulary

The words live in the `RAW` array in `index.html`. Each entry has four parts:

```js
["كِتَابٌ", "kitābun", "book", "L1"]   // [Arabic, transliteration, English, set id]
```

To add a lesson, add an entry to `SETS`, for example `{ id: "L4", name: "Lesson 4" }`, then add words tagged `"L4"`.

## Notes

- Students' "words to practice" lists are saved in their own browser (`localStorage`). Nothing is sent to a server.
- Fonts (Amiri, Figtree) load from Google Fonts.
