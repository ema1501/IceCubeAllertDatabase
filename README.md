# IceCubeAllertDatabase
[![DOI](https://sandbox.zenodo.org/badge/822978894.svg)](https://sandbox.zenodo.org/doi/10.5072/zenodo.78811)

Questo catalogo raccoglie di avvisi delle allerte in tempo reale per tracce di tipo Gold e Bronze di IceCube e per gli eventi di tipo Cascade. Ogni voce rappresenta un singolo evento di neutrino potenzialmente di origine astrofisica. 
Questo catalogo include avvisi emessi in tempo reale tramite avvisi/circolari GCN, così come eventi osservati in IceCube dal momento dell'inizio della raccolta dati con il rilevatore completo di IceCube nel 2011 che avrebbero attivato un avviso se il programma fosse stato in funzione.

Gli eventi nel database IceCube_Gold_and_Bronze consistono in eventi di tracce di muoni generati dall'interazione a carica corrente di eventi di neutrini ad alta energia (superiore a ~100 TeV) osservati presso l'Osservatorio di Neutrini IceCube (https://icecube.wisc.edu) situato sotto il Polo Sud geografico, Antartide. A queste energie, gli eventi di neutrini hanno una significativa probabilità di provenire da una fonte astrofisica.

La direzione migliore è derivata da una scansione iterativa di massima verosimiglianza di tutte le possibili direzioni degli eventi che viene eseguita dopo l'identificazione dell'evento di allarme, e viene pubblicata come aggiornamento per gli avvisi in tempo reale. 

Ogni voce è rappresentata da una voce nella tabella riassuntiva CSV.

Per ogni evento, la tabella CSV contiene:

- RUNID,EVENTID: Combinazione unica di RunID e EventID dal sistema DAQ di IceCube\\
- START,EVENTMJD: Data/ora del rilevamento dell'evento\\
- I3TYPE: Identificazione del tipo di selezione dell'evento (vedi pubblicazione di supporto per i dettagli). Tipi gfu-gold, gfu-bronze, ehe-gold, hese-gold o hese-bronze
- OTHER_I3TYPES: Lista degli altri tipi di selezione di eventi I3TYPE che questo evento ha superato.
- RA,DEC [deg] (e _ERR): Migliore direzione di adattamento in coordinate equatoriali J2000, con confini rettangolari dell'errore CL asimmetrico al 90%.
- ENERGY:[TeV] Energia del neutrino più probabile che avrebbe prodotto questo evento. Calcolato assumendo un flusso di potenza di neutrini astrofisici E^(-2.19).
- FAR: [yr^(-1)] Tasso di eventi di sfondo attesi per eventi di allarme a questa energia e posizione celeste.
- SIGNAL: Probabilità che l'evento sia di origine astrofisica, calcolata assumendo un flusso di potenza di neutrini astrofisici E^(-2.19).
- *_SCR: Probabilità da classificatore basato su rete neurale convoluzionale post-allarme applicato a ciascun evento per distinguere meglio il segnale topologico di ciascun evento nel rilevatore
- THRGOING_SCR: Vertice primario dell'evento fuori dal rilevatore e una traccia simile a un muone è osservata passare attraverso il volume strumentato
- START_SCR: Vertice primario dell'evento all'interno del volume strumentato e una traccia simile a un muone è osservata
- CASCADE_SCR: Vertice primario dell'evento all'interno del volume strumentato e una doccia (traccia non simile a un muone) è osservata
- SKIMMING_SCR: Vertice primario dell'evento fuori dal rilevatore e poca o nessuna energia depositata all'interno del volume strumentato
- STOP_SCR: Vertice primario dell'evento fuori dal rilevatore e una traccia simile a un muone è osservata fermandosi nel volume strumentato
- CR_VETO: Significativa attività di cascata di raggi cosmici in tempo rilevata nell'array di superficie IceTop, indicando che questo evento è probabilmente un evento di sfondo.


# Referenze
  - https://gcn.gsfc.nasa.gov/amon_icecube_gold_bronze_events.html
  - https://gcn.gsfc.nasa.gov/doc/IceCube_High_Energy_Neutrino_Track_Alerts_v2.pdf
  - https://gcn.gsfc.nasa.gov/amon_icecube_cascade_events.html
  - https://arxiv.org/abs/2304.01174

