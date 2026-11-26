# LOGOS – The Last Format

**LOGOS – The Last Format** è un action game 3D isometrico sviluppato individualmente con **Unity 6 e C#** nell'ambito di un progetto universitario.

Ambientato in **SYNTÁXIS**, un'architettura digitale prossima al collasso, il gioco segue Aster, un protocollo di sanitizzazione incaricato di eseguire il Format Totale. L'esperienza combina combattimento ravvicinato, movimento offensivo, nemici con comportamenti distinti e ambienti soggetti a de-allocazione.

> **Stato:** demo giocabile completata; progetto non attualmente in sviluppo attivo.

## Panoramica

| | |
|---|---|
| Genere | Action 3D isometrico |
| Engine | Unity 6 — **6000.3.16f1** |
| Linguaggio | C# |
| Piattaforma della demo | Windows PC |
| Sviluppo | Individuale – MONAD STUDIO |
| Durata di sviluppo | Circa 5 mesi |
| Durata media della demo | 15–30 minuti |

## La demo

La demo realizzata per l'esame comprende **tre livelli e un'arena finale**. I livelli includono corridoi, tutorial, differenti tipologie di nemici e un'arena da completare per accedere all'area successiva. La durata indicativa è di 15–30 minuti, in base all'abilità del giocatore.

La build Windows e il video gameplay sono conservati privatamente e non sono distribuiti da questa repository.

## Sistemi implementati

- Movimento del protagonista tramite Unity Input System.
- Combattimento ravvicinato con Stylus e sistema di combo.
- **Vettore di Collisione:** dash offensivo che attraversa e danneggia i nemici.
- Gestione della vita, dei danni e degli stati cromatici di Aster.
- AI dei nemici basata su NavMesh.
- Spawn randomico dei nemici tramite punti, quantità e raggi configurabili.
- Object Pooling.
- Lock-in arenas e gestione delle ondate.
- Boss fight contro Critical Failure.
- Gestione della telecamera.
- Audio Manager, mixer e sound design contestuale.
- De-allocazione dinamica del pavimento: le singole piattaforme si disattivano/scompaiono e successivamente ricompaiono e risalgono.

## Art direction e asset

Il gioco adotta uno stile low-poly / poly-art, con architetture geometriche, piattaforme modulari e contrasti cromatici. Gli asset 3D presenti nella demo sono stati modellati dall'autore. Aster parte da una base stilizzata del corpo umano, successivamente modificata e adattata. Le animazioni sono state integrate utilizzando risorse Mixamo e animazioni disponibili in Unity.

I livelli sono stati costruiti manualmente combinando asset 3D, prefab e strumenti Tilemap.

## Audio

Il sound design è stato curato individualmente, combinando risorse audio esterne con suoni creati, modificati e mixati appositamente. Un sistema contestuale regola il volume dei nemici in base alla distanza dal giocatore; il comparto è gestito anche tramite un mixer principale.

## Tecnologie

Unity 6 · C# · Unity Input System · AI Navigation / NavMesh · Coroutine · Object Pooling · Prefab · Tilemap · Shader · Particle System · Mixamo · Inno Setup.

## Stato e limitazioni

Il sistema completo di progressione e potenziamento previsto dal Game Design Document non è stato implementato. UI/HUD, menu e alcuni shader/VFX sono parziali. Il menu disponibile è minimale. La demo presenta alcuni bug non bloccanti; non sono state svolte ottimizzazioni specifiche delle prestazioni.

## Documentazione

- [Gameplay e sistemi](docs/GAMEPLAY.md)
- [Panoramica tecnica](docs/TECHNICAL_OVERVIEW.md)
- [Processo di sviluppo](docs/DEVELOPMENT.md)
- [Crediti e risorse](docs/CREDITS.md)
- [Ambito della repository](docs/REPOSITORY_SCOPE.md)

## Autore

**Sebastiano Gravili – MONAD STUDIO**

Game design, programmazione, modellazione degli asset 3D, level design, integrazione delle animazioni e sound design.

---

*Progetto indipendente realizzato a fini universitari e presentato sotto forma di demo giocabile.*
