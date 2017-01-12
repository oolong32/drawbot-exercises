# DrawBot Übungen

Basierend auf Armin Hofmanns Buch «[Methodik der Form- und Bildgestaltung](http://www.niggli.ch/de/methodik-der-form-und-bildgestaltung.html)», Niggli Verlag 1965.

## Vorgehensweise

Am besten ist es, die nachfolgenden Übungen zu zweit zu machen: Eine Person ist Fahrerin und schreibt Code. Die andere ist Navigatorin: Sie sagt, was zu tun ist, schaut bei Syntax-Fragen in der DrawBot- oder Python-Dokumentation nach, usw.

Jede Übung umfasst eine oder mehrere Abbildungen. Wählt eine davon aus und diskutiert die Regeln, nach denen das darin enthaltene Bild gezeichnet wurde. Notiert diese Regeln auf Papier, bevor ihr mit Coden beginnt. Meist hilft es auch, einige Skizzen zu machen.

Dann schreibt ihr mit DrawBot ein Programm, das ein Bild nach diesen Regeln generiert. Es ist dabei nicht so wichtig, den zuvor entwickelten Regeln bis ins Detail gerecht werden. Manchmal ist es notwendig, die Regeln zu vereinfachen, um vorwärts zu kommen.

Es ist übrigens nicht verkehrt, die Notizen als Kommentare ins Eingabefeld von DrawBot zu übertragen, z.B. als Überschriften für einzelne Abschnitte des Programms.

Link zur [DrawBot Dokumentation](http://www.drawbot.com/quickReference.html).

## Dokumentation

Es wird darum gebeten, oft Screenshots zu machen und sie in geeigneter Art und Weise öffentlich zu machen (Slack?).

DrawBot schreibt den Output mit der Funktion `saveImage()` in eine Datei.

```python
from time import strftime

# der Zeitstempel im Dateinamen verhindert das Überschreiben der Datei
timestr = strftime('%Y%m%d-%H%M%S')

# der Dateiname definiert das Format: jpg, png, gif, mov, pdf
saveImage('~/Desktop/name_' + timestr + '.jpg')
```

## Hofmann S. 105, Abb. 119–122

![Abb. 1](./hofmannPics/hofmann_105-119-120-121-122.jpg)

### Tipp

```python
# Linie zeichnen
line((x1, y1), (x2, y2))

# Füllfarbe
fill(0)

# Linienfarbe, Wert zwischen 0 und 1
stroke(0)

# Liniendicke
strokeWidth(x)
```

## Hofmann S. 52, Abb. 6/7

![Abb. 2](./hofmannPics/hofmann_52_6.jpg)
![Abb. 3](./hofmannPics/hofmann_52_7.jpg)

### Tipp

Um einen Raster zu zeichnen, müssen zwei for-Loops verschachtelt werden. Einer für die Y-Achse, einer für die X-Achse.

## Hofmann S. 53, Abb. 10–12

![Abb. 4](./hofmannPics/hofmann_53-10-11-12.jpg)

### Tipp

Auch hier bruacht es einen Raster, gezeichnet wird aber nur, wenn bestimmte Beidngungen erfüllt werden.

## Hofmann S. 56, Abb. 20/22/24

![Abb. 5](./hofmannPics/hofmann_56-20.jpg)
![Abb. 6](./hofmannPics/hofmann_56-22.jpg)
![Abb. 7](./hofmannPics/hofmann_56-24.jpg)

### Tipp

Kein Tipp.

## Hofmann S. 59, Abb. 30

![Abb. 8](./hofmannPics/hofmann_59-30.jpg)

### Tipp

Für die zunehmende Liniendicke (Progression) könnte eine Variable mit jeder Iteration des for-Loops vergrössert werden.

```python
sw = 1

for n in range(r):
    strokeWidth(sw)
    line((x, y), (xx, yy))
    sw += 1 # das ist eine verkürzte Schreibweise für sw = sw + 1
```

## Hofmann S. 60, Abb. 32/33

![Abb. 9](./hofmannPics/hofmann_60-32-33.jpg)

### Tipp

Kein Tipp.

## Hofmann S. 62, Abb. 39

![Abb. 10](./hofmannPics/hofmann_62-39.jpg)

### Tipp

Kein Tipp.

### Tipp

Um zu verhindern, dass sich Kreise überlappen, müssen die Positionen aller Kreise in einer Liste gespeichert werden. Die Position jedes neuen Kreises muss mit den in der Liste enthaltenen Werte verglichen werden, bevor er akzeptiert oder verworfen wird.

Das ist für Einsteiger etwas ambitioniert, deshalb würde ich vorschlagen, Überlappungen fürs Erste als glückliche Zufälle willkommen zu heissen, oder wie es bei Bob Ross heisst: ‘happy accidents’.

## Hofmann S. 80, Abb. 65–69

![Abb. 11](./hofmannPics/hofmann_80-65.jpg)
![Abb. 12](./hofmannPics/hofmann_80-66.jpg)
![Abb. 13](./hofmannPics/hofmann_80-67.jpg)
![Abb. 14](./hofmannPics/hofmann_80-68.jpg)
![Abb. 15](./hofmannPics/hofmann_80-69.jpg)

### Tipp

Kein Tipp.

## Hofmann S. 96, Abb. 99–103

![Abb. 16](./hofmannPics/hofmann_96-99-100-101-102-103.jpg)

### Tipp

Kein Tipp.
