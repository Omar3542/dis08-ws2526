# Markdown Cheat Sheet

## Basic Formatting

### Headings
Headings werden mit einem oder mehreren `#` am Zeilenanfang erstellt.
Markdown-Code:
# Heading 1
## Heading 2
### Heading 3

---

### Paragraphs & Line Breaks
Absätze werden durch eine Leerzeile getrennt.  
Ein Zeilenumbruch entsteht durch zwei Leerzeichen am Zeilenende.

Beispiel-Ergebnis:
This is one paragraph.

This is another paragraph.

Line one  
Line two

Markdown-Code:
This is one paragraph.

This is another paragraph.

Line one␠␠
Line two

---

### Bold
Fetter Text wird mit zwei Sternchen oder zwei Unterstrichen umschlossen.

Beispiel-Ergebnis:
**Bold text**

Markdown-Code:
**Bold text**

---

### Italic
Kursiver Text wird mit einem Sternchen oder Unterstrich umschlossen.

Beispiel-Ergebnis:
*Italic text*

Markdown-Code:
*Italic text*

---

### Strikethrough
Durchgestrichener Text wird mit doppelten Tilden erzeugt.

Beispiel-Ergebnis:
~~Strikethrough~~

Markdown-Code:
~~Strikethrough~~

---

### Inline Code
Inline Code wird mit einfachen Backticks geschrieben.

Beispiel-Ergebnis:
Use `print()` to output text.

Markdown-Code:
Use `print()` to output text.

---

## Lists

### Unordered Lists
Ungeordnete Listen verwenden `-`, `*` oder `+`.

Beispiel-Ergebnis:
- Item A
- Item B
- Item C

Markdown-Code:
- Item A
- Item B
- Item C

---

### Ordered Lists
Geordnete Listen verwenden Zahlen mit Punkt.

Beispiel-Ergebnis:
1. First
2. Second
3. Third

Markdown-Code:
1. First
2. Second
3. Third

---

### Nested Lists
Verschachtelte Listen entstehen durch Einrückung mit zwei Leerzeichen.

Beispiel-Ergebnis:
- Main item
  - Sub item
    - Sub-sub item

Markdown-Code:
- Main item
  - Sub item
    - Sub-sub item

---

## Links & Images

### Inline Links
Inline Links bestehen aus Linktext in eckigen Klammern und der URL in runden Klammern.

Beispiel-Ergebnis:
[Markdown Tutorial](https://www.markdowntutorial.com/)

Markdown-Code:
[Markdown Tutorial](https://www.markdowntutorial.com/)

---

### Reference-style Links
Der Link wird über eine Referenz definiert, was längere Texte übersichtlicher macht.

Beispiel-Ergebnis:
[Markdown Guide](https://www.markdownguide.org/)

Markdown-Code:
[Markdown Guide][md]

[md]: https://www.markdownguide.org/

---

### Images
Bilder verwenden ein Ausrufezeichen vor der Link-Syntax.

Beispiel-Ergebnis:
![Placeholder Image](https://via.placeholder.com/150)

Markdown-Code:
![Placeholder Image](https://via.placeholder.com/150)

---

### Image + Link Combination
Ein Bild kann gleichzeitig als Link dienen.

Beispiel-Ergebnis:
Ein klickbares Bild, das zu GitHub führt.

Markdown-Code:
[![Logo](https://via.placeholder.com/100)](https://github.com)

---

## Code & Technical Content

### Fenced Code Blocks
Codeblöcke werden mit drei Backticks erstellt.

Beispiel-Ergebnis:
