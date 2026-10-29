# Un trimestre, tre clienti, un'unica elaborazione

## Il lavoro da semplificare
Scenario simulato: uno studio riceve export mensili con strutture diverse e deve preparare report periodici per tre aziende. Il passaggio ripetitivo è riordinare le colonne, calcolare gli stessi indicatori e impaginare documenti distinti. Non è stata osservata o misurata una procedura reale di studio.

## Prima e dopo
| Passaggio | Preparazione manuale ipotizzata | Flusso nella demo |
| --- | --- | --- |
| Dati | Riordinare ogni export | Due tracciati riconosciuti; mappatura manuale per altre intestazioni |
| Copertura | Controllare i mesi per azienda | Matrice mesi/aziende e blocco dei target incompleti |
| Analisi | Ripetere formule per ogni cliente | Calcoli comuni sulle aziende selezionate |
| Documenti | Preparare ogni report | Modello unico, tre PDF e tre riepiloghi CSV in uno ZIP |

## Riproduci il caso
1. Apri la demo e premi **Prova con 6 export fittizi**. Sono gli stessi file della cartella examples: aprile-settembre 2026, due tracciati alternati, 319 record complessivi.
2. Verifica la copertura per **2026-Q3**: tre aziende complete, confronto con 2026-Q2 disponibile.
3. Scegli **Approfondimento organizzativo**; lascia commenti e componenti attivi.
4. Genera il lotto. Seleziona Officine Emilia, cambia misura e seleziona un mese nell'anteprima.
5. Scarica il pacchetto ZIP. Nella cartella report ci sono tre PDF, ciascuno di tre pagine. Gli altri file sono Riepilogo_studio.csv, Reparti.csv, Copertura.csv e LEGGIMI.txt.

## Risultati attesi
Importi arrotondati qui e nei PDF; i valori decimali sono disponibili in [risultati-attesi.json](risultati-attesi.json).

| Azienda | Costo trimestre | Variazione costo | FTE medi | Costo trimestrale/FTE | Persone a fine periodo |
| --- | ---: | ---: | ---: | ---: | ---: |
| Logistica Adriatica | 179.533 € | 0,7% | 16,2 | 11.105 € | 17 |
| Officine Emilia | 228.286 € | 7,3% | 21,7 | 10.536 € | 24 |
| Studio Aurora | 113.278 € | 3,3% | 11 | 10.298 € | 12 |

Per Officine Emilia il costo cresce del 7,3% e gli FTE medi del 3,2%. È una lettura congiunta di due misure, non una spiegazione causale. Il costo/FTE usa gli FTE medi prima dell'arrotondamento.

## Prova anche un caso incompleto
Torna ai file e rimuovi Export_B_2026-09.csv. Ripeti la copertura su 2026-Q3: settembre risulta mancante per tutte le aziende e la generazione è disabilitata. Ricarica il lotto dimostrativo per ripristinare i dati.

Rimuovendo invece un mese di riferimento, il target può essere generato ma il confronto rimane non disponibile. Un file duplicato blocca il lotto: il codice persona deve essere univoco per azienda e mese.

## Cosa dimostra
Normalizzazione di input, controlli di completezza, indicatori riproducibili, visualizzazione interattiva e generazione documentale in lotto. Nessuna percentuale di risparmio di tempo è dichiarata: richiederebbe una prova misurata su una procedura reale.

Il [video illustrativo](../media/ReportFlow_Caso_Uso.mp4) dura 62 secondi e usa schermate reali e didascalie. È senza audio e non rappresenta tempi di esecuzione.
