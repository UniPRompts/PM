
```toc
```
## Layout codificato

Nello storyboard è possibile aggiungere delle sottoviste alla vista del view-controller trascinando un oggetto vista dalla palette degli oggetti. Dopo averlo inserito questo avrà una posizione, che però alla rotazione dello schermo non rimarrò uguale quindi bisognerebbe avere una UI che adatta l'orientazione automaticamente.

## Layout Automatico

Il Layout automatico prende delle regole definite dall'utente e le trasforma in vicoli. 

##### Esempio

Il label ha uno spazio finale fisso

```C
Control.centerY = Superview.centerY
Control.right = Superview.right - <padding>
```


Il layout automatico è un sistema di layout basato su vincoli, che rende più semplice risolvere automaticamente molti problemi di layout complessi senza una manipolazione manuale della vista, semplificando i problemi rilevanti:
- L'orientamento
- Differenti dimensioni dello schermo

Quindi si può dire che questo tipo di layout è descritto attraverso vincoli, ed i frame sono calcolati automaticamente. I vincoli sono definito come relazione tra le viste, permettendo così di descrivere relazioni molto complesse.

> Nota
> Il layout automatico mantiene il software più libero da bug dovuti a manipolazione manuale delle viste


### I vincoli

Un vincolo è una sorta di rappresentazione matematica di una dichiarazione esprimibile da un uomo.

##### Esempio

Il lato sinistro deve essere 20 punti distanti dal lato sinistro della vista che lo contiene = `button.left = (container.left + 20)`

Il vincono potrebbe essere rappresentato dalla formula $y = m\cdot x+b$ dove:
- $x$ e $y$ rappresentano gli attributi delle viste
- $m$ e $b$ sono dei valori floating point

Gli attributi possono essere:
- `left`
- `right`
- `top`
- `bottom`
- `leading`
- `trailing`
- `width`
- `height`
- `centerX`
- `centerY`
- `baseline`

### Utilizzare il layout automatico

In xcode il layout automatico è gestito graficamente, nella storyboard nell'angolo in basso a destra sono presenti i controlli

![[controlli-autolayout.png]]

Che voglio dire da sinistra a destra:
- "Cambia la vista tra la dimensione dello schermo di un iPhone X a quella di un iPhone Y"
- "Imposta i vincoli di allineamento", crea dei vincoli di allineamento, come centrare una vista nel suo container, o allineare il lato sinistro di due viste
- "Imposta i vincoli di pin", crea dei vincoli spaziali, come definire l'altezza di una vista o specificare la distanza orizzontale da un altra vista
- "Risolvi i problemi relativi al layout automatico", risolve i problemi relatici al layout aggiungendo o resettando i vincoli su richiesta
- "Ridimensionamento", specifica come il ridimensionamento ha effetto sui vincoli

### Aggiunge i vincoli

I vincoli possono essere aggiunti in 3 modi
- Trascinamento (ctrl)
- Menù di allineamento e pin
- Aggiungendo un vincolo mancante o suggerito

### Eliminare e modificare i vincoli

I vincoli possono essere selezionati e:
- eliminati, premendo il tasto `delete`
- modificati, utilizzando il menù apposito


### Il processo del layout automatico

Quando si lavora con il layout automatico, tipicamente un processo iterativo viene eseguito

![[process-autolayout.png]]

![[process2-autolayout.png]]

![[process3-autolayout.png]]

![[process4-autolayout.png]]


![[process-complete-autolayout.png]]