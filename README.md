# STEAMOS: Raccolta di Guide e Plugin per ALLY e LEGION GO
Guide, consigli e strumenti utili per STEAMOS UFFICIALE

## Indice
- [Download e installazione](#download-e-installazione)
- [Primi Passi dopo l'installazione](#primi-passi)
- [Guide principali](#guide-principali)
- [Contribuire](#contribuire)
- [Licenza](#licenza)

---

## Download e Installazione

- Scaricare il file immagine da sito Valve a [questo link](https://store.steampowered.com/steamos/download/?ver=steamdeck&snr=100601___)
- Creare un supporto USB avviabile, preferibilmente su un supporto USB veloce (Valve consiglia di usare Rufus su Windows, Balena Etcher su MacOS/Linux)
- Inserire la USB nella handheld e premere vol+ durante l'avvio per richiamare il boot menu, e avviare il supporto USB (Valido sia su ally che legion)
- Dopo un po' si avvia il sistema Steamos da USB, aprire la voce sul desktop "WIPE DATA AND INSTALL STEAMOS" per avviare l'installazione (nota: se usate un supporto USB lento potrebbe volerci molto tempo sia per l'avvio del sistema che per l'installazione)
- Dopo l'installazione la handheld si riavvierà (NOTA: la prima volta perde molto tempo ad avviarsi, attendere con pazienza)
- A quel punto si avvierà la configurazione guidata di Steam, e avrete completato l'installazione!

#### NOTA IMPORTANTE: 
Se provate a installare SteamOS su un SSD in cui è già presente un'altra distro di linux (esempio: Bazzite), l'installazione potrebbe non partire (cliccando su "WIPE DATA AND INSTALL STEAMOS" si apre il terminale ma crasha subito dopo). In tal caso è consigliato togliere SSD e inserirlo esternamente su windows, e usare un gestore partizioni come DiskGenius per eliminare tutte le partizioni e formattare l'SSD. 
Se sull'SSD è presente un'installazione di steamos o windows non ci sono problemi, mentre con un'installazione bazzite non sono riuscito a eliminare le partizioni da linux in nessun modo, e sono stato costretto a usare windows con diskgenius per farlo.

## Primi Passi

### 1. Impostare una password di root per linux

Una volta avviato steam, andare in desktop mode e aprire il menu "start", cliccare sull'icona accanto al nome utente e si aprirà un menu: a quel punto cliccare su "cambia password" e impostare la password. 
Questa password verrà richiesta durante l'esecuzione di programmi che modificano il sistema, installazione di plugin, o l'uso di comandi da terminale.

### 2. Installazione Decky Loader e Plugin NECESSARI

- **Decky loader:** Tool che permette di installare numerosi plugin utilissimi, di cui alcuni NECESSARI. <br>&emsp; Aprire [questo link](https://decky.xyz/) e cliccare la voce download in alto a destra. Aprire il file scaricato, inserire la password precedentemente impostata e attendere l'installazione. A quel punto andare in gaming mode e poi riavviare per completare l'installazione correttamente
  
- **SimpleDeckyTDP:** Plug-in per Decky loader necessario per impostare il TDP e altre funzioni utili su Ally e Legion GO. <br>&emsp; Per installarlo basta inserire questo comando da terminale
  <pre> curl -L https://github.com/aarron-lee/SimpleDeckyTDP/raw/main/install.sh | sh </pre>

### 📚 Programmazione
- [Guida Python](https://esempio.com/python) - Introduzione a Python per principianti
- [Guida JavaScript](https://esempio.com/js) - Nozioni base di JavaScript

### 🎨 Design
- [Guida UX](https://esempio.com/ux) - Principi di user experience design

---

## Guide principali
- [Come usare GitHub](https://esempio.com/github) - Guida passo-passo per principianti

---

## Contribuire
Se vuoi contribuire aggiungendo guide o correzioni, leggi il file CONTRIBUTING.md...

---

## Licenza
Questa raccolta è distribuita con licenza MIT. Vedi il file LICENSE per i dettagl
