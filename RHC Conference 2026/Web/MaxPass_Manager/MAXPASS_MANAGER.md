# MAXPASS MANAGER

Nella pagina di atterraggio c'è una form dove possiamo creare un utente e loggarci

![](./images/1-register-form.png)

Una volta loggati vediamo che questa app è un password manager e sotto la scritta di benvenuto dice ci loggarci come admin per vedere la flag

![](./images/2-dashboard.png)

Nel codice sorgente, dentro routes/index.js, si può fare una chiamata GET a /api/passwords/:uuid, e specificando un id utente, sarà possibile vedere tutti i suoi dati, serve solo essere autenticati, con qualsiasi utente

![](./images/3-from-uuid.png)

Dentro il file database.js vediamo che lo uuid di admin è 73

![](./images/4-uuid-admin.png)

Quindi facendo una richesta get a http://\<ip>:\<porta>/api/passwords/73 è possibile vedere la psw di admin

![](./images/5-psw-admin.png)

Ora loggandoci con le credenziali di admin possiamo vedere la flag

![](./images/6-flag.png)