---
description: Answer a question using the wiki as the knowledge source
argument-hint: <question>
---

$ARGUMENTS

Answer the question above using the content of the `wiki/` folder.

1. **Find relevant pages.** Read `wiki/index.md` first to locate candidates, then read the linked pages.
2. **Answer from the wiki.** Cite source pages in parentheses for each piece of information (e.g. `([[transformer]])`). If the answer is not in the wiki, say so clearly — do not fill in from general knowledge without explicitly flagging it as such.
3. **Suggest capitalizing.** If the answer has lasting value, suggest running `/save` on it to turn it into a wiki page.
