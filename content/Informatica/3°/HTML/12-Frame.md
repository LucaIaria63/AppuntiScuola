# Cos'è il frame?
- Il frame è un pezzo di codice per far mettere due siti in uno solo
## Metafora per spiegare
### Immaginate il codice come un "panino"

![[Schema-12-Up-Down.png]]

#### Spiegazione 
1. Iniziare il "panino" con ```<FRAMESET>```: ogni panino che si rispetti ha degli ingredienti e noi decideremmo come saranno inseriti e cosa saranno:
	- Partiamo dal come, se il panino deve avere gli ingredienti messi a "righe" (uno sopra l'altro) si userà ```<FRAMESET ROWS="">``` e tra le virgolette si inseriranno
2. ```<FRAME SRC="sito1.htm">``` diciamo uno dei due ingredienti, tramite il parametro ```SRC``` che significa origine, tradotto dal inglese source, chiede da dove prendere il primo ingrediente che deve sempre essere un sito, si ripete la stessa logica per il secondo ingrediente
3.  Chiudere con  ```</FRAMESET>``` diciamo che il "panino" è finito
## Esempio pratico:

![[Cartelle-12.png]]
- Abbiamo 3 file:
	- un sito in cui vogliamo mettere due in uno solo (SitoConFrame.htm)
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

2. Successivamente dobbiamo inserire andare in ```<HEAD>``` e usare ```<FRAMESET>```
## 

```
<FRAMESET COLS="50%,50%">
	<FRAME SRC="sito1.htm">
	<FRAME SRC="sito2.htm">
</FRAMESET>
```