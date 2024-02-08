# Overleaf Vorlage für ein EMS Poster
Die Vorlage orientiert sich an der offiziellen Vorlage, ist jedoch, auch Latex geschuldete nicht 1:1 gleich.

[Beispiel](images/EMS_Template-1.pdf)


# Beschreibung
Das Modul ist in der initialen Phase, daher sind Befehle nur sehr rudimentär gescriptet. 

* Cropmarks.sty ist verantwortlich für die erstellung der Schnittmarken. In Zeile 39 kann auch ein zuätzlicher Rand ein ung ausgeblendet werden.
```latex
% Draw crop marks
\newcommand{\drawcropmarks}{
   \begin{tikzpicture}[remember picture, overlay]  
        %\drawoutlines
        \drawcropmarkbottomleft
        \drawcropmarkbottomright
        \drawcropmarktopright
        \drawcropmarktopleft
        %\drawCenterCross
    \end{tikzpicture}
}
 ```

* beamercolorthemeems.sty
Erlaubg die Anpssung der Farbegung des Tempaltes

* beamerthemeems.sty
Das eigentliche Template. Hier sind enebfalls anpassungen möglich. Einige spezielle Anpassungen sind:
- Zeile 64ff: Erlaubt das setzen von Überschriften innerhalb eines Blocks. Subsections/Paragraphs können hinzugefügt werden. 
- Zeile 93ff: Sollten zusätzliche Inputs für das Template notwendig sein (bspw. Projektpartner, etc.) könnten diese hier als newcommand hinzugefüht und dann in der Fuß/Kopfzeile eingefügt werden.
- Zeile 113ff: Setzt die Ränder des Templates


# Fehler und Fehlerkorrekturen
Die Vorlage ist nicht fehlerfrei. Es kann passieren, dass in Spezialfällen zB Farben angepasst oder Formatierungen manuell geändert werden müssen. 
# Adaptionen
Sind Adaptionen notwendig und erscheinen diese für alle User sinnvoll (z.B Farbanpassungen) können diese gepusht werden. Bei spezifischen Adaptionen (zB Inklusion von Firmenpartner) kann ein eigener Branch geöffnet werden.

