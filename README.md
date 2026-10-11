# Curricolo

App web per creare il CV in formato europeo (Europass) e la lettera di presentazione.
È una pagina statica: non serve nessuna installazione né server.

## Pubblicare su GitHub Pages

1. Crea un nuovo repository su GitHub (per esempio `curricolo`).
2. Carica tutto il contenuto di questa cartella nella radice del repository
   (`index.html`, `manifest.webmanifest`, `.nojekyll` e la cartella `icons`).
3. Vai in **Settings, Pages**. In "Build and deployment" scegli **Deploy from a branch**,
   branch `main`, cartella `/ (root)`, poi **Save**.
4. Dopo uno o due minuti l'app è online su `https://TUO-UTENTE.github.io/curricolo/`.

## Mettere l'icona sulla Home dell'iPhone

1. Apri l'indirizzo qui sopra in **Safari** (deve essere Safari).
2. Tocca il tasto Condividi, poi **Aggiungi alla schermata Home**.
3. L'icona (la c con la spunta) compare sulla Home e l'app si apre a schermo intero.

Se hai già aggiunto una versione precedente, rimuovila e aggiungila di nuovo:
iOS conserva la vecchia icona.

## Contenuto

- `index.html`: l'app (tutto in un unico file)
- `manifest.webmanifest`: nome, colori e icone dell'app
- `icons/apple-touch-icon.png`: icona per iPhone e iPad (180x180)
- `icons/icon-192.png`, `icon-512.png`, `icon-512-maskable.png`: icone per Android e per i browser
- `icons/favicon.svg`, `favicon-32.png`: icona della scheda del browser

## Limiti di questa versione

I dati dei profili restano solo nella pagina aperta: se la chiudi o la ricarichi si perdono.
I tasti di backup, importazione ed esportazione in PDF e Word mostrano per ora un avviso.
Il caricamento di un CV esistente (PDF, Word o testo) funziona e carica due librerie da internet.
