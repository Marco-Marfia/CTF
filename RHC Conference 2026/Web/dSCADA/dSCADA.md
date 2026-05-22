# dSCADA

Sulla pagina principale c'è una form di login per gli amministratori, proviamo quindi con delle credenziali deboli, admin:admin funziona

![](./images/1-login.png)

Una volta loggati, nella pagina settings, vediamo che sotto la tab 'Serial' si possono fare dei check, provando uno dei due esempi, risponde mostrando il comando che viene lanciato lato server

![](./images/2-check.png)

Quello che scriviamo verrà messo dopo il 'grep -o', quindi separiamo i comandi con ';' e diamo un'occhiata alla root directory. Qui troviamo il file readflag

![](./images/3-readflag.png)

Proviamo ad aprirlo e vediamo che è un file ELF, quindi un eseguibile

![](./images/4-ELF.png)

Eseguendolo riusciamo ad ottenere la flag

![](./images/5-flag.png)