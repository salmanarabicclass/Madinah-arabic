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
| Type | اسم | Shown small in the top-right corner of each flashcard (اسم، فعل، حرف). Not a filter |
| Sample Sentence Arabic | هَذَا *كِتَابٌ*. | Optional. Shown under the Arabic word on the Arabic side of the card |
| Sample Sentence Translation | This is a *book*. | Optional. Shown on the English side of the card |
| Transliteration | kitābun | Optional. If present, the app offers a "Show pronunciation" option |

In the sample sentences, wrap the vocabulary word in asterisks (`*كِتَابٌ*`) to show it in bold. Without asterisks, the app bolds the word if it finds it in the sentence. Sentences should use only words from the same lesson or earlier ones.

The **Word bank** link at the top of the page opens the sheet.

If the column names can't be found, the app uses the column order above. Filters appear only for columns with two or more different values. The sheet must be shared as **Anyone with the link: Viewer**, or the page can't read it. The sheet ID is set in `SHEET_ID` in `index.html`.

## Notes

- Students' "words to practice" lists are saved in their own browser (`localStorage`). Nothing is sent to a server.
- Fonts (Noto Naskh Arabic, Figtree) load from Google Fonts.
