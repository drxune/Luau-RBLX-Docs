# TextTruncate | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/TextTruncate
Scraped: 2026-01-11T02:44:43.982075Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [TextTruncate](/docs/reference/engine/enums/TextTruncate)

English

Feedback

Engine Enum

TextTruncate

---

Controls the truncation of text when using the TextTruncate property.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | Text is not truncated. |
| AtEnd | 1 | Text is truncated at the end of the text; extra graphemes that cannot fit into the space are replaced with .... Word boundaries are respected if possible.  For example, if the control is between -> and <- like so:  ->Long text is truncated at the en<-d of the last complete word  The text will be:  Long text is truncated at the... |
| SplitWord | 2 | If the end of the line occurs in the middle of a word, the text is truncated inside of that word. Extra graphemes that cannot fit into the space are replaced with ....  For example, if the control is between -> and <- like so:  ->Long text is truncated at the en<-d of the last complete word  The text will be:  Long text is truncated at the en... |