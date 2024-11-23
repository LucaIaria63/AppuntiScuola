# Cos'è il frame?
- Il frame è un pezzo di codice per far mettere due siti in uno solo
## Metafora per spiegare
### Immaginate il codice come un "panino"

![[Schema-12-Up-Down.png]]

#### Spiegazione 
Tutto questo codice è nella  ```<HEAD>``` 
##### 1. Iniziare il "panino" con ```<FRAMESET>```: 
- ogni panino che si rispetti ha degli "ingredienti" e noi decideremmo come saranno inseriti e quanto saranno:
	- Partiamo dal come, se il panino deve avere gli "ingredienti" messi a "righe" (uno sopra l'altro) si userà ```<FRAMESET ROWS="">``` e tra le virgolette si inseriranno le 2 percentuali dei nostri ingredienti, che sommate faranno 100 la quantità, esempi: 
		- ```<FRAMESET ROWS="50%,50%">``` primo "ingrediente" occuperà il 50% della pagina e il secondo "ingrediente" occuperà l'altro 50% della pagina ([[Schema-12-Up-Down.png|se noti bene è che ho messo per far capire l'idea]])
		- ```<FRAMESET ROWS="60%,40%">``` primo "ingrediente" occuperà il 60% e il secondo 40%
	- Se invece vogliamo mettere gli "ingredienti" a "colone" (uno accanto all'altro) si userà ```<FRAMESET COLS="">```  tra virgolette si inseriranno le 2 percentuali dei nostri ingredienti, che sommate faranno 100 la quantità, esempi: 
		- ```<FRAMESET COLS="50%,50%">``` primo "ingrediente" occuperà il 50% dello spazio messo dritto in verticale  e il secondo "ingrediente" occuperà l'altro 50% della pagina 
		- ```<FRAMESET COLS="60%,40%">``` primo "ingrediente" occuperà il 60% dello spazio  e il secondo 40% 
##### 2 Inserire gli ingredienti con ```<FRAME SRC="sito1.htm">``` 
- diciamo uno dei due ingredienti, tramite il parametro ```SRC``` che significa origine, tradotto dal inglese source, chiede da dove prendere il primo ingrediente che deve sempre essere un sito (un file .htm), si ripete la stessa logica per il secondo ingrediente
##### 3.  Finire il panino ```</FRAMESET>``` 
- Con ```</FRAMESET>```  si dice al computer che il panino è finito e che non vogliamo altro
## Esempio pratico:

![[Cartelle-12.png]]
- Abbiamo 3 file:
	- un sito in cui vogliamo mettere due siti messi a "colone" e che si dividano in metà lo spazio  (SitoConFrame.htm)
	- i due siti che vogliamo mettere (Sito1.htm e Sito2.htm)
### Codici:
#### Sito1.htm
```
<HTML>
	<HEAD>
		<TITLE> Sito1 </TITLE>
	</HEAD>
	<BODY>
		<H1> Questo è il Sito1 </H1>
	</BODY>
</HTML>
```
#### Sito2.htm
```
<HTML>
	<HEAD>
		<TITLE> Sito2 </TITLE>
	</HEAD>
	<BODY>
		<H1> Questo è il Sito2 </H1>
	</BODY>
</HTML>
```
# Ora programmiamo il codice per SitoConFrame.htm

1. Per programmarlo dobbiamo partire da un codice base quindi:

```
<HTML>
	<HEAD>
	</HEAD>
	<BODY>
	</BODY>
</HTML>
```

2. Successivamente dobbiamo pensare a come scrivere il codice, quindi dobbiamo mettere due siti quindi ci servirà:
```
<FRAMESET>
```
3. Lo vogliamo a colone quindi scriviamo:
```
<FRAMESET COLS="">
```
4. Vogliamo che si dividono a metà lo spazio quindi scriviamo 50%,50% tra le virgolette di ```COLS=```:
```
<FRAMESET COLS="50%,50%">
```
5. Ora tocca inserire i nostri ingredienti (sito1.htm e sito2.htm) quindi useremo ```<FRAME SRC="sito1.htm">``` per inserire sito1.htm e per inserire sito2.htm useremo ```<FRAME SRC="sito2.htm">```: 
```
<FRAMESET COLS="50%,50%">
	<FRAME SRC="sito1.htm">
	<FRAME SRC="sito1.htm">
```
6. Chiudiamo il "panino" con ```</FRAMESET>```:
```
<FRAMESET COLS="50%,50%">
	<FRAME SRC="sito1.htm">
	<FRAME SRC="sito1.htm">
</FRAMESET>
```
7.  Inseriamolo nel codice in ```<HEAD>```:

```
<HTML>
	<HEAD>
		<FRAMESET COLS="50%,50%">
			<FRAME SRC="sito1.htm">
			<FRAME SRC="sito1.htm">
		</FRAMESET>
	</HEAD>
	<BODY>
	</BODY>
</HTML>
```
8. Ammiriamo il risultato finale
![[Sito-Finale-12.png]]