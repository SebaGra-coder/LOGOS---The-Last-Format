# Panoramica tecnica

## Stack

- Unity 6 e C#
- Unity Input System
- Unity NavMesh
- Coroutine
- Object Pooling
- Prefab e Tilemap
- Shader e Particle System
- Audio Manager e Unity Audio Mixer

## Organizzazione

Le meccaniche sono suddivise in script distinti, con responsabilità separate per i singoli sistemi di gioco. Questa documentazione descrive il comportamento funzionale; non include il codice sorgente né una mappa delle classi.

## Movimento e input

Il controllo del protagonista utilizza il nuovo Unity Input System. Il movimento è separato dai sistemi di combattimento e gestione degli stati.

## AI e spawn

La navigazione dei nemici utilizza NavMesh. Lo spawn nel mondo è randomizzato entro parametri definiti: punti di spawn, quantità e raggio. Le arene sono invece predisposte e gestiscono le proprie ondate.

## Object Pooling

È implementato un sistema di Object Pooling per il riutilizzo degli oggetti, incluso il ciclo di gestione dei nemici.

## De-allocazione ambientale

La de-allocazione agisce sulle singole piattaforme: il pavimento si disattiva/scompare e successivamente ricompare e risale. Non si tratta di generazione procedurale dell'intero livello.

## Rendering e VFX

Sono presenti shader utilizzate per gestire la resa cromatica di elementi dell'altare e delle colonne nell'arena finale, dove erano presenti colori combinati. Sono inoltre presenti effetti particellari associati al dash del giocatore. Il comparto shader/VFX nel suo complesso è parziale.

## Audio

Il progetto include un Audio Manager e un mixer principale. Il volume dei nemici viene regolato in funzione della distanza dal giocatore. Il sound design combina risorse esterne con suoni creati, modificati e mixati dall'autore.

## Limiti tecnici noti

- Il sistema completo di progressione non è stato implementato.
- UI/HUD e menu sono parziali.
- Sono presenti bug non bloccanti.
- Non sono state effettuate ottimizzazioni specifiche delle prestazioni.
- Il codice sorgente non è distribuito in questa repository.
