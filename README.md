# Curricolo

App web per creare il CV in formato europeo (Europass) e la lettera di presentazione.
È una pagina statica: non serve nessuna installazione né server.

## Pubblicare su GitHub Pages

1. Crea un nuovo repository su GitHub (per esempio `curricolo`).
2. Carica tutto il contenuto di questa cartella nella radice del repository
   (`index.html`, `manifest.webmanifest`, `.nojekyll` e le cartelle `icons` e `lib`).
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

- `index.html`: l'app (tutta la logica è in questo file: per gli aggiornamenti futuri basta sostituire solo questo)
- `lib/`: le librerie per creare PDF e Word (`pdf-lib` e `docx`, licenza MIT). Si caricano solo quando esporti un file
- `manifest.webmanifest`: nome, colori e icone dell'app
- `icons/apple-touch-icon.png`: icona per iPhone e iPad (180x180)
- `icons/icon-192.png`, `icon-512.png`, `icon-512-maskable.png`: icone per Android e per i browser
- `icons/favicon.svg`, `favicon-32.png`: icona della scheda del browser

## Cosa fa

- Profili multipli, salvati automaticamente sul dispositivo (restano anche dopo aver chiuso l'app).
- Backup: esporta e importa tutti i profili in un file.
- CV in 7 modelli (3 standard leggibili dai sistemi di selezione, 4 creativi), con formattazione del testo toccando le parti del CV.
- Esportazione del CV e della lettera in **PDF** (con testo selezionabile e leggibile dai sistemi di selezione) e in **Word**.
- Caricamento di un CV esistente (PDF, Word o testo): carica due librerie da internet.

## Note

- Il PDF riproduce il modello scelto. Il file Word ha un'impaginazione lineare e pulita: i modelli creativi (barra laterale, banner, due colonne) non si riproducono in Word.
- Il PDF usa i caratteri standard (Helvetica o Times): il font scelto nell'app viene approssimato a uno dei due.
- Su iPhone, dopo l'esportazione si apre il foglio di condivisione: scegli **Salva su File**.

## Icone
Le icone dei contatti e delle date (modelli creativi) sono disegni vettoriali, non caratteri di testo, quindi non disturbano la lettura dei sistemi di selezione. Hanno sempre lo stesso colore del testo accanto.

## Licenze

- Icone: Material Design Icons di Google, licenza Apache 2.0 (incorporate in `index.html`, avviso in `lib/LICENSE-material-icons.txt`).
- `pdf-lib` (Andrew Dillon): licenza MIT, file `lib/LICENSE-pdf-lib.md`.
- `docx` (Dolan Miu): licenza MIT, file `lib/LICENSE-docx.txt`.
- Solo quando carichi un CV esistente, l'app scarica da internet `pdf.js` (Mozilla, Apache 2.0) e `mammoth` (Michael Williamson, BSD 2-Clause).
- Il resto dell'app (`index.html`, logo, icone dell'app) è tuo.
