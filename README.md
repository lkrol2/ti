# Notatki do Technologii Internetowych

<blockquote>
<p>Dzień bez kodowania jest dniem straconym<br>
<p>Włodek Bzyl
</blockquote>

> Dzień bez kodowania jest dniem straconym
>
> Włodek Bzyl

Znaczniki:

* p
* ul, ol
 * li
* img
* h

Szablon pliku HTML5:

```html
<!doctype html>
<html lang=pl>
<head>
  <meta charset=utf-8>
  <title>Szablon strony HTML5</title>
</head>
<body>
  <p>ąćęłńóśźż ĄĆĘŁŃÓŚŹŻ</p>
</body>
</html>
```
***

* **bold**      wpisać na początku i na końcu dwie * 
* _italic_        wpisać na początku i na końcu jeden _
* __bold__      wpisać na początku i na końcu dwa _
* ___bold + italic___    wpisać na początku i na końcu  trzy _
* #zwiększanie czcionki  <quote>wpisać na początku #</quote>
 **Jarosław Gowin**doskonale wie, __będąc__ w _polityce_ ___od dawna___, <br>że nie ma w polityce 
 czegoś takiego jak zupełnie zamknięte drzwi. <br>Nasze drzwi nie są zupełnie zamknięte - powiedział 
 rzecznik PiS. <br>Dopytywany, czy Prawo i Sprawiedliwość podjęłoby rozmowy z Gowinem, <br>Hofman odparł, 
 że jego partia jest gotowa "na rozmowy o zmianie władzy<br> w Polsce właściwie z każdym". - Na rozmowy 
 dla rozmów i przepychanki szkoda czasu - dodał.
 
 * * *
 
 link
 
 [wikipedia](http://www.wikipedia.org/)
 
 ***
 obrazek

![logo Wiki](http://upload.wikimedia.org/wikipedia/commons/6/63/Wikipedia-logo.png)

***
obrazek jako link

 [![logo Wiki](http://upload.wikimedia.org/wikipedia/commons/6/63/Wikipedia-logo.png)](http://www.wikipedia.org/)
***
> **Poieranie cudzego repozytorium**<br>
> * ___Fork___ - pobranie repozytorium <br>
> 
> **Wysyłanie naniesionych zmian**<br>
> * ___Pull Request___ - wysyłanie zmian<br>
> * podajemy w tytule co było zrobione i wysyłamy.<br>
> 
> **Odbieranie**
> * wejśc do repozytorium
> * wcisnąć ___Pull Requests___ na pasku obok network
> * po wejściu kliknąć na tytuł
> * ___Files Changed___ - żeby zobaczyć zmiany /na zielono podaje poprawki/

***
> **Dodawanie osób - współpracowników do repozytorium**
> * wejść do repozytorium
> * ___Settings___ na listwie po lewej
> * ___Collaborators___
> * podać nazwę użytkownika
> * ___Add___

***
**Aby uzyskać ładne wcęcia w kodzie korzystamy z programu *indent*.**

Wchodzimy na terminal i logujemy się na sigmie:

```sh
ssh akiszel@sigma.ug.edu.pl
```

Następnie wykonujemy kopiuj kod i wklej go na terminalu.
Przykładowo:

```sh
cat > zad5.c
... ctrl+shift+v lub wybieramy wklej z menu terminala
CTRL+d
```

Teraz wykonujemy na terminalu:

```
indent -kr zad5.c
``` 
