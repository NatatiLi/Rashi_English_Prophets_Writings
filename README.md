# Rashi on the Prophets and Writings: an English Translation (AI-assisted, CC0, 2026)

An English translation of Rashi's commentary on the Prophets (Neviim) and the Writings (Ketuvim), released into the public domain under CC0 1.0.
**Status: AI-assisted draft. It has NOT had independent scholarly review.** Please read the "Limitations" section before relying on any passage.

## What this is

- A comment-by-comment English rendering of Rashi on the Prophets and Writings.
- Each entry is keyed to a book, chapter, verse and comment number, and carries the English lemma (as it appears in the JPS 1917 translation), the English translation of Rashi's comment, an optional translator's note, and a flag for passages whose reading is uncertain.
- The Hebrew text of Rashi is **not included** in this repository. Entries are identified by reference only. To read the Hebrew alongside, use the corresponding comment on [Sefaria](https://www.sefaria.org) or another edition.

## Data format

Files are provided as JSON and CSV with the same content. Each entry has these fields:

| Field | Meaning |
|---|---|
| `id` | Unique key: `BOOK.chapter.verse.comment_no` (e.g. `JOS.1.18.1`) |
| `book` | Book name in English (e.g. Joshua) |
| `chapter` | Chapter number |
| `verse` | Verse number |
| `comment_no` | Position of the comment within that verse (1, 2, 3 ...) |
| `english_lemma_JPS` | The phrase Rashi comments on, rendered in the wording of the JPS 1917 English Bible (public domain) |
| `english_translation` | English translation of Rashi's comment |
| `translator_note` | Optional note, for example a printed reference that does not match the Hebrew Tanakh, an Old French gloss that could not be matched, or a difference from another translation. Empty if there is nothing to note |
| `flagged_uncertain` | `yes` if the reading of the Hebrew or Aramaic is uncertain or open to interpretation; otherwise `no` or empty |

Example:

```json
{
  "id": "JOS.1.18.1",
  "book": "Joshua",
  "chapter": 1,
  "verse": 18,
  "comment_no": 1,
  "english_lemma_JPS": "shall rebel",
  "english_translation": "He will provoke (anger over) your words.",
  "translator_note": "",
  "flagged_uncertain": "yes"
}
```

## Method

The translation was produced with Anthropic's Claude Sonnet 5.5, used as a translation and collation tool under constraints set by the project owner. It translated from the Hebrew and Aramaic of Rashi using the reference works listed below, which were supplied to it as project files.

- Each comment was translated literally, keeping Rashi's wording and citations. Quotations of biblical verses follow the JPS 1917 text.
- Printed chapter and verse references, and quoted verses, were checked against the Hebrew Tanakh. Errors found in printed references are noted in `translator_note`.
- Old French glosses (la'az) were read against Darmesteter. Where a gloss is not in Darmesteter, or its printed spelling could not be matched, the note says so and no guess is given.
- A sample of comments was translated blind and compared with the Sefaria Community Translation of Rashi (CC0). That comparison found errors and truncations in that text, so it was used only as a cross-check and was not copied.
- Doubtful readings are flagged `flagged_uncertain: yes`. Translation of older Hebrew and Aramaic involves interpretation.
- Several audit rounds were run to check accuracy and licensing. These audits were run by the same AI system that produced the translation. They are not independent review.

## Limitations

- **No independent human scholarly review has been done.** The project owner is not a professional translator of medieval Hebrew and Aramaic.
- Errors in meaning, not just wording, are likely to remain, especially in dense halakhic or midrashic comments, Aramaic and Targum quotations, and Old French glosses.
- Same-system audits are good at catching slips (dropped clauses, wrong references) and weaker at catching systematic misreadings.
- Please do not cite this as an authoritative translation. Treat it as a draft aid, and check against public-domain Hebrew sources.

## Sources consulted

- **Rashi's Hebrew commentary (the text translated):** *Rashi On Your Way*. Source: [mobile.tora.ws](http://mobile.tora.ws/). Digitization: Sefaria. License: Public Domain.
- **Hebrew Tanakh (used to check cited verses):** all files used were listed by Sefaria as CC0 / Public Domain.
- **JPS 1917 English translation of the Bible** (public domain), for lemmata and biblical quotations.
- **Sefaria Community Translation of Rashi (CC0):** used only as a cross-check and never copied.

All other works below were obtained from Internet Archive uploads listed as public domain. Each is an edition no longer under copyright because of its date of publication.

- Multiple Public-domain Aramaic Targums (All editions/prints were made before the year 1910).
- Darmesteter, *Les gloses françaises de Raschi dans la Bible* (1909), for Old French glosses.
- Godefroy, *historical dictionary of Old French* (1883).
- Blondheim, David Simon, *Contribution à la lexicographie française d'après des sources rabbiniques* (1910).
- Dunash ben Labrat, *Teshuvot* (1866 edition).
- Brown-Driver-Briggs *Hebrew and English Lexicon* (1906).
- Margolis, *A Manual of the Aramaic Language of the Babylonian Talmud* (1910).
- Jastrow, *Dictionary of the Targumim, Talmud Babli, Yerushalmi and Midrashic Literature* (1903).
- *The Jewish Encyclopedia* (1906).
- *Revue des études juives* (1907).
- *Machberet Menachem* (1854 edition).
- *Machzor Yom Kippur* (1890 edition).
- *Mikraot Gedolot, Venice* (1548).

## License

This translation is dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/). You may copy, modify, publish and use it for any purpose without asking permission.
Citation/credit is appreciated but never required (See citation at the end for details).

## Corrections and contributions

Reviewers, especially readers of Rashi, are very welcome to send in corrections. If you find an error:

1. Open an Issue with the `id` of the entry, what you think is wrong, and a suggested correction.
2. Or send a pull request that edits the JSON directly.
3. You should include how/where you obtained the information for the correction to help maintain copyright public-domain (example: Your own understanding of Aramaic and Old French).

**Corrections must not come from copyrighted sources or translations.** They must **come from your own understanding** of the text. Do not copy or closely paraphrase any copyrighted translation, commentary or dictionary. 
Corrections you contribute are accepted under the same CC0 terms and therefore must come from public-domain sources. Users who contribute any form of copyrighted content are soley responsible for their own copyright 
violations and take full responsibility, and their edits will be removed upon notice.

## How to cite

Since this is released as public domain, no citation is required. However, if you want to help the project improve over time, the following citation would be appreciated:

"Rashi on the Prophets and Writings: English Translation (AI-assisted translation), v1.0. CC0, 2026. https://github.com/NatatiLi/Rashi_English_Prophets_Writings"
