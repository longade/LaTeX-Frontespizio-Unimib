# LaTeX-Frontespizio-Unimib
Title page in LaTeX for thesis for degree in Computer Science (Unimib)

## Introduction
This page is created using 'Frontespizio' package https://www.ctan.org/pkg/frontespizio. It is independent from the rest of the document, so margins, font etc. are set only for this page. It represents the conversion from the .docx version taken from elearning unimib website.

## How it is made
I edited directly the file .sty of Frontespizio package adding a new template called **unimib**.

## How to use it
You have to do the following two things:
- make a backup of .sty file and replace the original with the new one
- create a title page (below a simple example)

For the first point, go to the folder of the _Frontespizio_ package, for a MikTeX Windows installation it is usually C:\Users\user\AppData\Local\Programs\MiKTeX\tex\latex\frontespizio\frontespizio.sty. Save a copy in this folder (or wherever you want) of this original file, for example I named it _frontespizio\_original.sty_. Then replace this with the one edited by me.

Regarding the second point, in your main .tex file you have to create the title page, an ecample below:
```latex
  \begin{frontespizio}
    \Istituzione {Università degli studi di Milano - Bicocca}
    \Logo [2.5cm]{bicocca.eps}
    \Facolta {Scuola di Scienze\\
              Dipartimento di Informatica, Sistemistica e Comunicazione}
    \Corso [Laurea]{Informatica}
    \Titolo {Title of thesis}
    \Relatore {Prof. Ciccio Pasticcio}
    \NRelatore {Relatore}{}
    \Correlatore {Dott. Franco Forte}
    \NCorrelatore {Correlatore}{}
    \Candidato[XXXXXX]{Lino Banfi}
    \NCandidato {Relazione della prova finale di}
    \Rientro {1.5cm}
    \Annoaccademico {2019-2020}
  \end{frontespizio}
```
Remember to save a copy of unimib logo in the same folder of your main .tex file.

After you compile _your\_main\_tex\_file.tex_, a file named _your\_main\_tex\_file-frn.tex_ is automatically generated. So, you have to compile this new file too.

Summing up, compile main .tex file, then frn .tex and finally main .tex again.

That's it!
