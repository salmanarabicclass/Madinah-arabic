# Madinah Arabic Practice

Flashcards and quizzes for the vocabulary and grammar in Madinah Arabic Book One. A switch at the top of the page chooses **Vocabulary** or **Grammar**.

Grammar mode is still being tested, so it only appears when the page address ends in `?grammar=true` (for example `https://salmanarabicclass.github.io/rcarabic/?grammar=true`). Without it, the page shows vocabulary only and doesn't load the Grammar tab. To publish grammar for everyone, set `GRAMMAR_ON` to `true` in `index.html`.

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

## Updating the grammar cards

Grammar cards come from the **Grammar** tab of the same sheet. Each row is one card. Cards with the same Topic form a deck, and topics become the filters in Grammar mode.

| Column | Example | Notes |
|---|---|---|
| Topic | Mubtada' & khabar | Groups cards; shown at the top of each card |
| Sentence | \*البَيْتُ\* كَبِيرٌ. | Wrap the part being asked about in asterisks to highlight it |
| Translation | The house is big. | Optional |
| Question | What is the highlighted part of the sentence? | Shown on the front |
| Answer | مُبْتَدَأٌ | The Arabic term; shown on the back |
| Answer English | Mubtada' (subject) | Shown under the answer, and under that term in quiz choices |
| Explanation | The mubtada' is usually definite… | Shown on the back and after a quiz answer |
| Choices | مُبْتَدَأٌ \| خَبَرٌ | Quiz options, separated by `\|`, in the order shown. Leave empty to use the answers from the same topic |

If the Grammar tab can't be loaded, vocabulary still works and Grammar mode shows the reason.

## Notes

- Students' "words to practice" lists are saved in their own browser (`localStorage`). Nothing is sent to a server.
- Fonts (Noto Naskh Arabic, Figtree) load from Google Fonts.
