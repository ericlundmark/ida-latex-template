# ida-latex-template
En liten guide för hur man använder latexmallen från Institutionen för datavetenskap (IDA) vid LiU
#Hämta mallen
Den senaste versionen verkar vara den här
http://www.ida.liu.se/edu/ugrad/thesis/templates/latex/index.sv.shtml

Lägg till den i ditt latex projekt. Använder du share latex är det bara att ladda upp alla filer till root mappen i projektet.
#Användning
Mallen kräver ett par steg för att allt ska se korrekt ut.
## Inladdning
Som det står i idathesis.cls ska man ange en av följande i början av huvuddokumentet
```latex
\documentclass[cropmarks, frame, swedish]{idamasterthesis}
\documentclass[cropmarks, frame, english]{idamasterthesis}
\documentclass[cropmarks, frame, english]{idalichesis}
\documentclass[cropmarks, frame, english]{idaphdthesis}
\documentclass[cropmarks, frame, english, philosophy]{idaphdthesis}
```
## Författarinformation
Fyll sedan i den information som känns vettig utifrån det du angivit ovan. Den information som kan anges är följande.
```latex
\titleenglish{ENGLISHTITLE}
\titleswedish{SWEDISHTITLE}
\publicationmonth{PUBMONTH}
\publicationyear{PUBYEAR}
\isbn{ISBN}
\thesisnumber{THESISNUMBER}
\thesisyearnumber{THESISYEARNUMBER}
\abstract{ABSTRACT}
\swedishabstract{SWEDISHABSTRACT}
\dateofpublication{DATEOFPUBLICATION}
\supervisor{SUPERVISOR}
\examiner{EXAMINER}
\degreesubject{Engineering}
\supportedby{SUPPORTEDBY}

\division{DIVISION}
\divisionshort{DIVISIONSHORT}
\titlebibpage{TITLEBIBPAGE}
\keywords{KEYWORDS}
\nyckelord{NYCKELORD}

\degreetype{teknologie}
\presentationplace{PRESENTATIONPLACE}
\presentationhouse{PRESENTATIONHOUSE}
\presentationhus{PRESENTATIONHUS}
\presentationdate{PRESENTATIONDATE}
\presentationdatum{PRESENTATIONDATUM}
\presentationtime{PRESENTATIONTIME}
\degreesubject{DEGREESUBJECT}
\degreesubjectswedish{DEGREESUBJECTSWEDISH}
\facultyexaminername{OPPONENT NAME}
\facultyexaminertitle{OPPONENT TITEL}
\facultyexamineraddress{OPPONENT ADDRESS}
\thesisurl{http://XXX}
\departmentseries{DEPARTMENTSERIES No. XXX}
```
## Titelsida, innehållsförteckning etc.
Titelsida, abstract, innehållsförteckning samt tomma sidor ska inte inkluderas manuellt. Detta görs istället genom att köra `latex \makeintropages`

#Tips
Använd `latex \chapter{}` för huvudrubriker och `latex \section{}` för underrubriker. Annars kommer du få rubriker som börjar på 0 t.ex. 0.2 0.2.3.
