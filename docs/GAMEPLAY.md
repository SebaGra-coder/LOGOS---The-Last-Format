# Gameplay e sistemi

## Struttura della demo

La demo giocabile è composta da tre livelli e un'arena finale. Ogni livello presenta corridoi, tutorial, differenti tipologie di nemici e un'arena da completare per accedere all'area successiva. La durata media indicativa è di 15–30 minuti e varia in base all'abilità del giocatore.

## Aster e combattimento

Aster è il protagonista controllato dal giocatore. I sistemi implementati comprendono movimento, gestione della vita e dei danni, stati cromatici, combattimento e combo.

Lo **Stylus** è l'arma da combattimento ravvicinato. Il sistema supporta attacchi concatenati e gestione dei danni.

Il **Vettore di Collisione** è un dash offensivo: Aster attraversa lo spazio e può danneggiare i nemici.

## Nemici e boss

La navigazione dei nemici utilizza Unity NavMesh. Lo spawn nel mondo è randomizzato a partire da punti predefiniti, con parametri per quantità e raggio.

**Critical Failure** è il boss finale. È stato realizzato come controparte di Aster e utilizza il dash come attacco e comportamento di inseguimento; non dispone dello Stylus.

## Arene e ambiente

Le arene sono configurate in anticipo e gestiscono il blocco dell'area e le ondate di nemici. La distribuzione dei nemici nel resto del mondo utilizza punti di spawn e parametri configurabili.

La de-allocazione dinamica agisce sulle singole piattaforme: queste si disattivano/scompaiono e in seguito ricompaiono e risalgono.

## Fallimento e respawn

È presente il respawn quando Aster cade fuori dal mondo e in seguito al Game Over. Non sono presenti checkpoint intermedi.

## Elementi non completati

Il sistema completo di progressione previsto dal GDD non è stato implementato. UI/HUD, menu e alcuni shader/VFX sono parziali. Il menu disponibile è minimale e consente di mettere in pausa, iniziare o uscire.
