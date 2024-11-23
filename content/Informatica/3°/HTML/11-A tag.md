# Cos'è ```<A>```?
- ```<A>``` è un tag per inserire un collegamento a un altro sito al interno di ```<BODY>```, [[Pagina a cui sei arrivato cliccando un testo fatto con un A|tipo questa frase subordinata]].
# Come funziona ```<A>```:
## Come formare ```<A>```
1. Inserire  ```<A>```
```
<A>
```
2. Inserire ```HREF=""```
```
<A HREF="">
```
3. Inserire il sito a cui ci vogliamo collegare nel nostro caso sito1.htm
```
<A HREF="sito1.htm">
```
4. Mettiamo il testo che vogliamo, nel nostro caso sarà TESTO
```
<A HREF="sito1.htm"> TESTO
```
5. Chiudiamo con ```</A>```
```
<A HREF="sito1.htm"> TESTO </A>
```
6. Fatto
## Casi di ```<A>```:

### ```<A>``` è al interno di un ```<P>```

Questo caso è quando vogliamo un collegamento in una singola parte di testo e non in tutto il testo, facciamo un esempio di testo: Il cane abbaia
1. Noi vogliamo cane che porti a sito1.htm quindi verrebbe da scrivere:
```
<A HREF="sito1.htm"> Il cane abbaia </A>
```
2. Ma così tutta la frase è un collegamento ma noi vogliamo **solo** cane, quindi partiamo dal testo come lo scriveremo normalmente
 ```
<P> Il cane abbaia </P>
```
3. Sostituiamo la parola cane con un  ```<A>``` quindi bisogna [[11-A tag#Come formare ```<A>```|formare un ```<A>``` con la parola cane]] (segui la guida sopra), dovresti ottenere 
```
<A HREF="sito1.htm"> cane </A>
```
4. E sostituiscilo
 ```
<P> Il <A HREF="sito1.htm"> cane </A> abbaia </P>
```
5. Fatto
