Artikel schreiben in RMarkdown - Eine Einführung
========================================================
author: Matthias Weiler
date: 11.09.2018
autosize: true
transition: concave

Folien online
========================================================

https://mrweiler.github.io/r_writing


Ziele für heute
========================================================

- Word-Dokument erstellen und formatieren  
- Statistische Kennwerte einfügen
- Literaturverzeichnis einfügen  


Zur Erinnerung: R Markdown
========================================================
- Auszeichnungssprache zur Erstellung von Dokumenten 
- [R Markdown Übersicht]  
  (https://rmarkdown.rstudio.com/)
- [R Markdown Basics]
  (https://rmarkdown.rstudio.com/authoring_basics.html)
  

Word-Dokument in RStudio erstellen
========================================================

- Mit Hilfe des R-Pakets _knitr_ können  
  RMarkdown-Dokumente in Markdown  
  umgewandelt werden
- Pandoc kann daraus dann Word-Dokumente  
  (oder pdf, html, ...) erstellen


Übung
========================================================

- Erstellt ein RMarkdown-Dokument mit  
  "Word" als Output Format und speichert  
  dieses ab
- Klickt auf "knitr", um daraus ein  
  Word-Dokument zu erstellen


Word-Dokument formatieren
========================================================

- Pandoc benutzt automatisch die Standard  
  Formatvorlagen von Microsoft Word
- Um dies zu ändern ist es möglich ein  
  Referenz-Dokument anzugeben


Übung
========================================================

- Speichert das soeben erstellte Word-Dokument  
  als _reference.docx_ ab.
- Passt ein paar der Formatvorlagen in Word an
- Ergänzt den yaml-Header eures  
  RMarkdown-Dokuments (Einrückung beachten!:  

```r
output:  
  word_document:  
    reference_docx: reference.docx
```


Statistische Kennwerte einfügen
========================================================

- Statistische Kennwerte können aus dem  
  RMarkdown-Dokument über Variablennamen  
  aufgerufen und in den Fließtext  
  eingebunden werden:

```r
... und einem Mittelwert von `r my_mean`.
```


Zur Erinnerung: externen R Code einbinden (1)
========================================================
- __Im R Skript:__ Label ergänzen

```r
## ---- my label ----
my_sum <- 100
my_count <- 10
my_mean <- my_sum / my_count
```


Zur Erinnerung: externen R Code einbinden (2)
========================================================
- __Im R Markdown Dokument:__ R Skript einlesen mit read_chunk():  
'''{r}  
knitr::read_chunk("ugly_code.R")  
'''
- __Im R Markdown Dokument:__ r label aufrufen:  
'''{r my label}  
'''


Übung
========================================================
- Erstellt ein R-Skript, in dem ein Mittelwert  
  berechnet wird
- Bindet diesen Abschnitt eures R Codes in eurem  
  RMarkdown Dokument ein
- Bindet den Mittelwert in einen Satz ein


Literaturverzeichnis einfügen  
========================================================

- 

Fragen?
========================================================


Links
========================================================

- [Folien online]
  (https://mrweiler.github.io/r_writing)  
- [R Markdown Übersicht]  
  (https://rmarkdown.rstudio.com/)
- [R Markdown Basics]
  (https://rmarkdown.rstudio.com/authoring_basics.html)
- [Bibliographies and Citations in RMarkdown]  
  (https://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html#bibliographies)