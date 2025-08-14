# STEAMOS: Raccolta di Guide e Plugin per ALLY e LEGION GO
Guide, consigli e strumenti utili per STEAMOS UFFICIALE

## Indice
- [Download e installazione SteamOS](#download-e-installazione-steamos)
- [Primi Passi e Tool Necessari](#primi-passi)
  - [1. Password di root](#1-impostare-una-password-di-root-per-linux)
  - [2. Decky Loader e Tool Necessari](#2-installazione-decky-loader-e-tool-necessari)
- [Plugin Consigliati](#plugin-consigliati)
  - [1. Plugin non presenti nello Store](1-plugin-non-presenti-nello-store-decky)
  - [2. Plugin presenti nello Store](1-plugin-presenti-nello-store-decky)
- [Tool e Utility](#tool-e-utility)
  - [1. Tool non presenti in Discover](1-tool-non-presenti-in-discover)
  - [1. Tool presenti in Discover](1-tool-presenti-in-discover) 

---

## Download e Installazione SteamOS

- Scaricare il file immagine da sito Valve a [questo link](https://store.steampowered.com/steamos/download/?ver=steamdeck&snr=100601___)
- Creare un supporto USB avviabile (preferibilmente su un supporto USB veloce). Valve consiglia di usare Rufus su Windows, Balena Etcher su MacOS/Linux
- Inserire la USB nella handheld e premere vol+ durante l'avvio per richiamare il boot menu, e avviare il supporto USB (Valido sia su ally che legion)
- Dopo un po' si avvia il sistema Steamos da USB, aprire la voce sul desktop "WIPE DATA AND INSTALL STEAMOS" per avviare l'installazione (nota: se usate un supporto USB lento potrebbe volerci molto tempo sia per l'avvio del sistema che per l'installazione)
- Dopo l'installazione la handheld si riavvierà (NOTA: la prima volta perde molto tempo ad avviarsi, attendere con pazienza)
- A quel punto si avvierà la configurazione guidata di Steam, seguire i passaggi per completare l'installazione.

#### NOTA IMPORTANTE: 
Provando a installare SteamOS su un SSD in cui è già presente un'altra distro di linux (esempio: Bazzite), l'installazione potrebbe non partire (cliccando su "WIPE DATA AND INSTALL STEAMOS" si apre il terminale ma crasha subito dopo). In tal caso è consigliato togliere SSD e inserirlo esternamente su windows, e usare un gestore partizioni come DiskGenius per eliminare tutte le partizioni e formattare l'SSD. 
Se sull'SSD è presente un'installazione di steamos o windows non ci sono problemi, mentre con un'installazione bazzite non sono riuscito a eliminare le partizioni da linux in nessun modo, e sono stato costretto a usare windows con diskgenius per farlo.

## Primi Passi

### 1. Impostare una password di root per linux

Una volta avviato steam, andare in desktop mode e aprire il menu "start", cliccare sull'icona accanto al nome utente e si aprirà un menu: a quel punto cliccare su "cambia password" e impostare la password, ma rifiutate di impostare la password per il wallet.
Questa password verrà richiesta durante l'esecuzione di programmi che modificano il sistema, installazione di plugin, o l'uso di comandi da terminale.

### 2. Installazione Decky Loader e Tool NECESSARI

- **Decky loader:** [Link Download](https://decky.xyz/) <br>
Tool che permette di installare vari plugin utilissimi, di cui alcuni necessari. Presenta uno store interno, ma alcuni vanno comunque scaricati esternamente. <br> 
**💿 Installazione:** <br>
  Aprire il link e scaricare dal pulsante in alto a destra. Aprire il file da gestore file, inserire la password root impostata prima e attendere l'installazione. A quel punto andare in gaming mode e riavviare il sistema per una corretta installazione. Il plugin si troverà nel menù laterale destro di steam, con l'icona di una 🔌. Andare nelle opzioni⚙️ del plugin per attivare la modalità sviluppatore, in modo da poter installare plugin manualmente tramite file zip. 
  
- **SimpleDeckyTDP:** [Link Repository](https://github.com/aarron-lee/SimpleDeckyTDP) <br>
Plug-in per Decky loader necessario per impostare il TDP e altre funzioni utili su Ally e Legion GO. <br>
**💿 Installazione:** <br>
  Inserire questo comando da terminale
  ```
  curl -L https://github.com/aarron-lee/SimpleDeckyTDP/raw/main/install.sh | sh
- **InputPlumber** [NECESSARIO SOLO SU LEGION GO]: [Link Repository](https://github.com/ShadowBlip/InputPlumber) <br>
Permette il corretto funzionamento del controller Legion, e l'utilizzo contemporaneo di più controller. <br>
**💿 Installazione:** <br>
  Inserire questo comando da terminale
  ```
  sudo pacman -S inputplumber 
  ```
  In seguito inserire questo comando per avviare i servizi inerenti:
  ```
  sudo systemctl enable inputplumber
  sudo systemctl enable inputplumber-suspend
  sudo systemctl start inputplumber
  ```

## Plugin Consigliati

### 1. Plugin non presenti nello store di Decky
**PREMESSA:** Se non specificato diversamente, i file zip dei plugin vanno installati manualmente dalle opzioni(⚙️) di Decky Loader(🔌). È necessario attivare la modalità sviluppatore di Decky per far apparire l'opzione.

- **Decky Framegen:** [Link Download ZIP](https://github.com/xXJSONDeruloXx/Decky-Framegen/releases) <br>
Plugin che tramite optiscaler permette di convertire gli input DLSS in XESS 2.1, inclusa frame generation se disponibile. <br>

- **Decky Lossless Scaling:** [Link Download Zip](https://github.com/xXJSONDeruloXx/decky-lossless-scaling-vk/releases) <br>
Plugin che permette di utilizzare Lossless Scaling su linux in pochi click, per avere la frame generation in tutti i giochi. È necessario acquistare Lossless Scaling su steam per il funzionamento.

- **NonSteamLauncher:** [Link Installer](https://github.com/moraroy/NonSteamLaunchers-On-Steam-Deck/releases) <br>
  Plugin che permette facilmente l'installazione di altri launcher (es. Epic, Gog, Ubisoft, EA). Inoltre permette l'installazione di servizi streaming come webapp chrome, utilizzabili con controller (es. Gamepass, Geforce, Luna, Youtube). <br>
  **💿Installazione:** <br>
  Scaricare NSLPLUGIN.desktop e avviarlo dal gestore file per avviare l'installazione o l'aggiornamento del plugin.

### 2. Plugin presenti nello store di Decky

- **SteamGriDB:** Permette di modificare facilmente artwork e banner di ogni gioco/app steam.
  
- **ProtonDB Badges:** Nella schermata di ogni gioco appare un badge che indica la fruibilità del gioco su linux.
    
- **HLTB:**: Nella schermata di ogni gioco ne indica la durata effettiva, secondo le stime di HowLongToBeat.

- **Wine Cellar:** Permette di installare diverse versioni di proton.

- **MangoPeel:** Permette di personalizzare l'overlay delle prestazioni di steam.

- **DeckSP:** Equalizzatore e volume booster con varie opzioni utili.

- **AutoFlatpaks:** Permette di aggiornare i flatpak installati su linux direttamente dalla gaming mode.

- **Pause Games:** Permette di freezare in memoria i giochi, per aprirne più in contemporanea.

- **FreeLoader:** Notifica la presenza di giochi in regalo nelle varie piattaforme.

## Tool e utility

### 1. Tool non presenti in Discover

- **Driver per Dongle USB XBOX::** [Link Repositoty](https://github.com/SavageCore/xone-steam-deck-installer) <br>
**💿 Installazione:** Da terminale eseguire questo comando:
  ```
  wget -O /tmp/bootstrap.sh https://github.com/SavageCore/xone-steam-deck-installer/releases/latest/download/bootstrap.sh && sh /tmp/bootstrap.sh
  ```
  Al termine verranno aggiunte 4 icone sul desktop; se va tutto a buon fine apparirà un popup che conferma l'installazione invita a inserire il dongle XBOX. Secondo i miei test, invece, ci sarà un errore e l'installazione non andrà a buon fine. <br>
  In questo caso, basta inserire questo comando:
  ```
  sudo pacman -S linux-neptune-611
  ```
  In seguito riavviare il sistema, e poi aprire sul desktop l'icona con la dicitura "DEBUG" tra le 4 icone precedentemente apparse. A quel punto apparirà finalmente il popup di conferma. Riavviare per poi testare il funzionamento del dongle.

### 2. Tool presenti in Discover

- **ProtonTricks:** Permette di eseguire script, aprire exe, o installare dependencies all'interno di uno specifico prefisso Wine.

- **ProtonPlus:** Manager per installare nuove versioni di proton (più completo del plugin winecellar)

- **Lutris:** Permette di installare giochi o programmi tramite file exe o cartelle. Permette anche l'installazione semplice di launcher di store alternativi. Dal sito Lutris esistono degli script per installare direttamente retrogame per windows.

- **PortProton:** Alternativa a Lutris con dei vantaggi/svantaggi

- **Heroic Launcher:** Vari store gaming in un'unica app. Alternativa al plugin NonSteamLauncher.
  
  



