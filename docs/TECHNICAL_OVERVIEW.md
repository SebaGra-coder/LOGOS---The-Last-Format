# Panoramica tecnica

## Ambiente di sviluppo verificato

I file di configurazione presenti nella repository indicano:

- Unity Editor: **6000.3.16f1**
- Universal Render Pipeline: **17.3.0**
- Input System: **1.19.0**
- AI Navigation: **2.0.12**
- C# come linguaggio di scripting del progetto.

La configurazione dei pacchetti è consultabile in [Packages/manifest.json](../Packages/manifest.json), mentre la versione esatta dell'editor è riportata in [ProjectSettings/ProjectVersion.txt](../ProjectSettings/ProjectVersion.txt).

## Sistemi di gioco descritti dall'autore

Le meccaniche della demo sono suddivise in script distinti, con responsabilità separate per i singoli sistemi. Questa documentazione descrive il comportamento funzionale dichiarato; la repository pubblica non contiene il codice gameplay completo e quindi non viene proposta una mappa di classi o API non verificata.

### Movimento e input

Il controllo del protagonista utilizza il nuovo Unity Input System. Il movimento è separato dai sistemi di combattimento e gestione degli stati.

### Combattimento

Il combattimento ravvicinato utilizza lo Stylus e un sistema di combo. Il Vettore di Collisione è un dash offensivo che attraversa e danneggia i nemici.

### AI e spawn

La navigazione dei nemici utilizza NavMesh. Lo spawn nel mondo è randomizzato entro parametri definiti: punti di spawn, quantità e raggio. Le arene sono predisposte e gestiscono le proprie ondate.

### Object Pooling

È implementato un sistema di Object Pooling per il riutilizzo degli oggetti, incluso il ciclo di gestione dei nemici.

### De-allocazione ambientale

La de-allocazione agisce sulle singole piattaforme: queste si disattivano/scompaiono e successivamente ricompaiono e risalgono. Non si tratta di generazione procedurale dell'intero livello.

### Rendering e VFX

Sono presenti shader utilizzate per gestire la resa cromatica di elementi dell'altare e delle colonne nell'arena finale. Sono inoltre presenti effetti particellari associati al dash del giocatore. Il comparto shader/VFX nel suo complesso è parziale.

### Audio

Il progetto include un Audio Manager e un mixer principale. Il volume dei nemici viene regolato in funzione della distanza dal giocatore. Il sound design combina risorse esterne con suoni creati, modificati e mixati dall'autore.

## Limiti tecnici noti

- Il sistema completo di progressione non è stato implementato.
- UI/HUD e menu sono parziali.
- Sono presenti bug non bloccanti.
- Non sono state effettuate ottimizzazioni specifiche delle prestazioni.
- Il codice sorgente gameplay non è distribuito in questa repository.
