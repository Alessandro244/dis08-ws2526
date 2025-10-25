# Markdown Cheatsheet

Ein kompakter Überblick über die wichtigsten Markdown-Funktionen, inkl. GitHub-spezifischer Features.

---

## Überschriften (Headings).

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```
Je mehr # Zeichen, desto kleiner die Überschrift.

## Paragraphs & Line Breaks

Dies ist ein Absatz.

Dies ist ein neuer Absatz.

Zeile mit zwei Leerzeichen am Ende  
Nächste Zeile im selben Absatz.

## Formatierung

**Fett**
__Fett__
*Kursiv*
_ Kursiv_
***Fett + Kursiv***
~~Dieser Text ist durchgestrichen~~

## Inline Code & Fenced Code Blocks

Inline Code: `Code`

Fenced Code Block:

```python
def hallo_welt():
    print("Hallo Welt")
```

Syntax Highlighting möglich: python, javascript, html, markdown etc.

## Listen

### Unordered Lists (ohne Reihenfolge)
- Apfel
* Banane
+ Kirsche

### Ordered Lists (mit Reihenfolge)
1. Erste Aufgabe
2. Zweite Aufgabe

### Verschachtelte Listen
- Obst
  - Apfel
  - Banane
- Gemüse
  1. Karotte
  2. Brokkoli

## Links & Images

### Inline Link
[Google](https://www.google.com)

### Reference Link
[Google][google]

[google]: https://www.google.com "Gehe zu Google"

### Inline Image
![Alt-Text](https://via.placeholder.com/150 "Titel")

### Image + Link
[![Alt-Text](https://via.placeholder.com/150)](https://www.google.com)

## Blockquotes
> Dies ist ein Zitat
> 
> **Mit Formatierungen**
>  **Liste**
> - _Code_

## Verschachtelte Blockquotes:
> > Zitat innerhalb eines Zitats

## Horizontal Rules / Divider (Drei mal zeichen -, * oder _)
---

## Tables

### Basic Table
| Name  | Alter | Stadt   |
|-------|:-----:|--------:|
| Anna  | 25    | Berlin  |
| Ben   | 30    | Hamburg |
Alignment: :--- (links), :---: (zentriert), ---: (rechts)
Complex Tables möglich mit Markdown innerhalb der Zellen (wie Fett oder Kursiv geschrieben).

## Task Lists / Checkboxes (GitHub-specific)
- [ ] Milch kaufen
- [x] Brot besorgen
- [ ] Eier prüfen
Interaktiv in Issues, Pull Requests, Discussions.

## GitHub Mentions, Issues & PRs
@username → Mention einer Person  
#42 → Verlinkt automatisch Issue/PR im selben Repo  

## GitHub Emojis
:smile: :thumbsup:

## Online & Collaborative Editors
StackEdit, Typora, Obsidian
