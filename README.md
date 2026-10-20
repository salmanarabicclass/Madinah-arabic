# Madinah Arabic Vocabulary

Flashcards and quizzes for the vocabulary in Madinah Arabic Book One.

The whole app is one self-contained file: `index.html`. It needs no build step. Open it in a browser, or serve it with GitHub Pages.

## Updating the vocabulary

The words come from the **RC Arabic Vocab** Google Sheet, which loads each time the page opens. To add or change words, edit the sheet. No code change is needed.

| Column | Example | Notes |
|---|---|---|
| Arabic | كِتَابٌ | Required |
| English | book | Required |
| Book | 1 | Becomes a "Book 1" filter |
| Lesson | 1 | Becomes a "Lesson 1" filter |
| Category | Noun | Becomes a category filter |
| Transliteration | kitābun | Optional. If present, the app offers a "Show pronunciation" option |

Filters appear only for columns with two or more different values. The sheet must be shared as **Anyone with the link: Viewer**, or the page can't read it. The sheet ID is set in `SHEET_ID` in `index.html`.

## Notes

- Students' "words to practice" lists are saved in their own browser (`localStorage`). Nothing is sent to a server.
- Fonts (Noto Naskh Arabic, Figtree) load from Google Fonts.
