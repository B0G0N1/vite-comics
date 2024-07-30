<!-------------------------
    CONSEGNA ESERCIZIO
-------------------------->

Ciao ragazzi,
Esercizio di oggi: Vite DC Comics
nome repo: vite-comics
Descrizione:
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da
screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!
Numero minimo di push: 12
Se volete potete utilizzare bootstrap installandolo con npm. Per le icone di fontawesome potete installare il pacchetto oppure usare la cdn.
Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.

<!-------------------------
    PASSAGGI GENERICI
-------------------------->

[1] CREO L'APP

1.  Eseguo 'npm create vite@latest vite-comics -- --template vue' da cmd sulla cartella nella quale voglio creare la cartella del progetto (per creare progetto con Scaffolding di VUE)
2.  Eseguo 'npm install' subito dopo quindi dentro la cartella appena creata, oppure aprendo il terminale nel nostro progetto (per installare le dipendenze)
3.  Stessa cosa del punto precedente eseguo 'npm run dev' (per avviare il live server, e quindi l'applicazione)

[2] INSTALLO TUTTE LE RISORSE NECESSARIE E PREPARO IL PROGETTO

1.  Importo le risorse, le immagini le copio dentro una cartella che creo nominata img dentro src
2.  Importo immagini layout dentro una cartella che creo nominata screenshot/layout nel root
3.  Elimino il file HelloWorld.vue dalla cartella components
4.  Elimino il file style.css (in src), e lo rimuovo dal main (import './style.css')
5.  Cancello tutto il contenuto del file App.vue (dentro a src), e con comando 'VueInit' ricreo la struttura, spostando la parte dello script in testa.
6.  Creo una cartella styles dentro a 'src' e all'interno creo un file nominato 'generals.scss' (che userò per i miei stili generici in linquaggio scss). Per usare questo file scss lo metto in 'App.vue', dentro al tag style metto 'lang=scss', e all'interno di style incollo la riga '@use './styles/generals.scss'
7.  Installo SASS, eseguendo da terminale 'npm add -D sass' (aggiungendolo come dipendenza di sviluppo, e non del progetto), se installo sass, devo ricordarmi di mettere lang=scss a tutti i tag style
8.  Installo Bootstrap (se prevedo di usarlo), facendo su terminale da vs 'npm install bootstrap', e sucessivamente importo bootstrap all'interno del file 'generals.scss' aggiungendo la riga '@import "../node_modules/bootstrap/scss/bootstrap"' (che è una direttiva per importare le dipendenze, mi dice il percorso preciso)
9.  Se voglio importo un carattere scrivendo sul file 'generals.scss' questa riga di codice @import url("link della lingua preso da google font solo con link https senza parentesi graffe minori ecc."), e agigungo al body da scss

[3] GESTIRE PROGETTO

1.  Controllo da quante parti sarà composto il progetto, in questo caso probabilmente HEADER,MAIN CONTENT SECTION,PROMOTIONAL SECTION,FOOTER
2.  Per ogni sezione, creo una sezione (parte di app) .vue dentro a components (esempio AppHeader.vue), all'interno con 'VueInit' mi creo la struttura dell'App (spostando sempre il tag script sopra), e inserisco il mio contenuto.
3.  Dopo bisognerà aggiungere queste "parti di app" nel App.vue (app principale) scrivendo:
    Dentro allo script importo AppHeader (presa dal suo percorso), ma devo anche dichiarare i componenti che uso.
    <script>
    import AppHeader from './components/AppHeader.vue';
    
    export default {
    components: {
        AppHeader
    }
    }
    </script>

    Infine la inserisco dove voglio nel template
    <template lang="">
    <div>
        <AppHeader/>
    </div>
    </template>

4.  Ogni sezione avrà un <style>, dovre dovrò mettere 'scoped' per limitare lo stile in quella singola App e non nelle altre.
5.  Via via creerò le sezioni e le aggiungerò nell'App.

[4] NOTE UTILI

1.  Immagini su ./src/img
2.  ./src/components/AppHeader.vue è un componente singolo (in questo caso Header) che poi verrà innestato nell'App principale
3.  ./src/App.vue è l'app principale che verrà montata (che contiene le altre sezioni che abbiamo creato)
4.  ./package.json è un testo con tutte le risorse usate dal mio programma: nome, versione, le dipendenze finali, e le dipendenze durante la programmazione
5.  ./gitignore contiene tutte le cartelle che con git push non devono essere caricate su github
6.  ./main.js è il js principale che importa e crea l'app di Vue
7.  ./src/styles/generals.scss contiene il scss generico, lo utilizziamo anche per importare cose come Bootstrap, GoogleFont, FontAwesome, etc.
8.  ./src/components/AppHeader.vue ogni app di vue, ha 3 parti; <script> che deve stare in alto dove inserisco gli script specifici a quella pagina/app/sezione, <template> dove inserisco il contenuto html di quella pagina, e <style> dove inserisco lo stile di quella pagina (attenzione il css è condiviso, se vuoi renderlo valido solo per quella pagina utilizzare 'scope')
