SUPSI 2025-26  
Data Visualization course, C-D3202E 
Teacher Giovanni Profeta


# Project title
Authors: [Sasha Bravo](https://github.com/sasha-bravo), [Nathan Ferrari](https://github.com/NathaFerrari), [Andrea Frati](https://github.com/AndreaFrati-18),  [Manuel Grosso](https://github.com/J-Manu12)

[Well being evolution during crisis](https://nathaferrari.github.io/dataviz_project/)


## Abstract
Questo progetto analizza in modo approfondito l’evoluzione del benessere nei Paesi europei nel periodo compreso tra il 2000 e il 2024, con l’obiettivo di comprendere come le principali crisi economiche, sanitarie e geopolitiche abbiano influenzato la qualità della vita dei cittadini. Negli ultimi vent’anni, infatti, l’Europa è stata attraversata da eventi di portata storica come la crisi finanziaria globale del 2008, la crisi del debito sovrano, la pandemia di COVID-19, la fase di forte inflazione successiva alla pandemia e il conflitto in Ucraina, che hanno messo sotto pressione i sistemi economici, sociali e istituzionali.  

Per analizzare questi fenomeni in modo strutturato è stato costruito un Indice di Benessere Aggregato, ottenuto combinando variabili economiche, sociali e di stabilità, al fine di restituire una visione multidimensionale del benessere. Attraverso l’utilizzo di visualizzazioni interattive, in particolare mappe e grafici temporali, il progetto mette in luce le differenze territoriali tra i Paesi europei, le dinamiche di convergenza e divergenza nel tempo e l’impatto degli shock storici sulle diverse aree del continente.  

Un’attenzione specifica è rivolta alla Svizzera, che emerge come un caso di studio particolarmente interessante per i suoi elevati e stabili livelli di benessere lungo tutto l’arco temporale analizzato. Il confronto tra la Svizzera e il resto d’Europa consente di evidenziare i fattori di resilienza che caratterizzano il suo sistema economico e sociale. Nel complesso, il progetto si propone di offrire una lettura chiara, accessibile e scientificamente fondata delle trasformazioni del benessere in Europa negli ultimi venticinque anni.



## Introduction
Negli ultimi decenni, il concetto di benessere ha assunto un ruolo sempre più centrale nel dibattito economico, politico e sociale. La crescita del prodotto interno lordo non è più considerata un indicatore sufficiente per descrivere lo stato di salute di un Paese, poiché non è in grado di cogliere aspetti fondamentali come la qualità della vita, la sicurezza economica, la coesione sociale, l’accesso ai servizi e la stabilità istituzionale. In questo contesto, l’Europa rappresenta un laboratorio particolarmente interessante per lo studio del benessere, poiché riunisce Paesi con livelli di sviluppo, modelli di welfare e assetti economici molto diversi tra loro.  

Il periodo compreso tra il 2000 e il 2024 è stato caratterizzato da una successione di crisi che hanno inciso profondamente sugli equilibri europei. La crisi finanziaria globale del 2008 ha provocato una recessione diffusa e una forte perdita di occupazione in molti Paesi. Negli anni successivi, la crisi del debito sovrano ha colpito in modo particolare l’Europa meridionale, accentuando le disuguaglianze economiche e sociali. A partire dal 2020, la pandemia di COVID-19 ha rappresentato uno shock senza precedenti, con effetti rilevanti sulla salute pubblica, sull’economia e sulle relazioni sociali. Il periodo successivo è stato contrassegnato da un forte aumento dell’inflazione e, dal 2022, dallo scoppio del conflitto in Ucraina, che ha avuto importanti ripercussioni sui prezzi dell’energia, sulla sicurezza e sulla stabilità geopolitica del continente.  

All’interno di questo scenario complesso, emerge la necessità di analizzare come il benessere dei cittadini europei abbia reagito a questi shock e se esistano differenze significative tra le diverse aree del continente. L’obiettivo di questo progetto è proprio quello di ricostruire l’evoluzione del benessere in Europa attraverso un approccio comparativo e data-driven. A questo scopo è stato costruito un Indice di Benessere Aggregato che combina più dimensioni — economiche, sociali e di stabilità — in un unico indicatore sintetico, capace di restituire una visione complessiva ma allo stesso tempo articolata del fenomeno.  

Le visualizzazioni interattive sviluppate nel progetto consentono di esplorare in modo intuitivo sia la distribuzione geografica del benessere sia la sua evoluzione nel tempo. In particolare, l’utilizzo di una mappa dinamica con slider temporale permette di osservare come i diversi Paesi europei abbiano attraversato le fasi di crescita, crisi e ripresa, mettendo in evidenza pattern territoriali ricorrenti, differenze strutturali e momenti di rottura legati agli shock storici.  

Un elemento centrale dell’analisi è rappresentato dal focus sulla Svizzera. Pur non facendo parte dell’Unione Europea, la Svizzera è fortemente integrata nel contesto economico e sociale europeo e mostra livelli di benessere particolarmente elevati e stabili lungo tutto il periodo analizzato. Il suo comportamento rappresenta un interessante termine di confronto per comprendere quali caratteristiche economiche, istituzionali e storiche possano favorire una maggiore resilienza agli shock.  

Nel complesso, questo progetto si propone non solo di descrivere l’andamento del benessere in Europa, ma anche di offrire strumenti interpretativi utili a comprendere le dinamiche che lo governano. L’uso della data visualization permette di trasformare dati complessi in informazioni accessibili, favorendo una lettura critica dei fenomeni e stimolando una riflessione più consapevole sulle trasformazioni sociali ed economiche che hanno interessato l’Europa negli ultimi venticinque anni.


## Data sources  

### Elenco dei dataset utilizzati  
- OECD – *How’s Life? / Current Well-Being (DSD_HSL_CWB)*  
  Dataset ufficiale dell’Organizzazione per la Cooperazione e lo Sviluppo Economico (OECD), accessibile tramite la piattaforma **OECD Data Explorer**.  
  
[Main datasource](https://data-explorer.oecd.org/vis?lc=en&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_HSL%40DF_HSL_CWB&df[ag]=OECD.WISE.WDP&dq=CHE.1_1%2B1_2%2B1_4%2B1_5%2B2_1%2B2_2%2B2_3%2B2_4%2B2_5%2B2_7%2B2_8%2B2_8_DEP%2B2_8_VER%2B2_9%2B3_1%2B3_2%2B3_3%2B3_4%2B3_5%2B4_4%2B4_4_DEP%2B4_4_VER%2B5_1%2B5_2%2B5_2_DEP%2B5_3%2B6_1%2B6_1_DEP%2B6_1_VER%2B6_2%2B6_2_DEP%2B6_2_VER%2B6_3%2B6_3_DEP%2B6_3_VER%2B6_4_DEP%2B7_1%2B7_1_DEP%2B7_3%2B7_3_DEP%2B7_3_VER%2B7_4%2B8_1%2B8_1_DEP%2B8_2%2B9_1%2B9_2%2B9_3%2B10_1%2B10_2%2B10_2_DEP%2B10_3%2B11_1%2B11_1_DEP%2B11_1_VER%2B11_2%2B11_3.....HSL_1%2BHSL_2%2BHSL_3%2BHSL_4%2BHSL_5%2BHSL_6%2BHSL_7%2BHSL_8%2BHSL_9%2BHSL_10%2BHSL_11&pd=2004%2C2025&to[TIME_PERIOD]=false&vw=ov&lb=nm)

### Provenienza dei dati  
I dati sono prodotti dall’**OECD (Organisation for Economic Co-operation and Development)**, attraverso il programma dedicato al benessere, inclusione e sostenibilità (**WISE – Well-Being, Inclusion, Sustainability and Equal Opportunity**).  
Il database raccoglie informazioni statistiche ufficiali fornite dai Paesi membri e partner dell’OECD, garantendo alta affidabilità, comparabilità internazionale e aggiornamenti periodici.
### Motivazione della scelta  
Il dataset OECD è stato scelto perché:  
- È progettato specificamente per misurare il **benessere oltre il PIL**, includendo aspetti economici, sociali e di qualità della vita.  
- Offre una **copertura temporale estesa**, ideale per analizzare l’evoluzione del benessere prima e dopo le principali crisi (2008, 2010–2012, 2020, 2022).  
- Permette confronti **internazionali standardizzati** tra Paesi europei.  
- Include indicatori su **disuguaglianze, deprivazione e distribuzione del benessere**, fondamentali per uno studio completo dell’impatto delle crisi.  
- È ampiamente utilizzato in ambito accademico e istituzionale, aumentando la solidità scientifica del progetto.

### Variabili principali  
Il dataset comprende oltre **80 indicatori** suddivisi in **11 dimensioni del benessere**, tra cui:

- **Condizioni economiche e materiali**
  - Reddito disponibile delle famiglie  
  - Ricchezza  
  - Qualità dell’alloggio  
  - Sicurezza del lavoro  

- **Qualità della vita**
  - Stato di salute  
  - Istruzione e competenze  
  - Qualità ambientale  
  - Sicurezza personale  
  - Soddisfazione per la vita  
  - Equilibrio vita-lavoro  
  - Relazioni sociali  
  - Partecipazione civica e fiducia nelle istituzioni  

- **Disuguaglianze e deprivazione**
  - Indicatori per genere, età e livello di istruzione  
  - Misure di disuguaglianza interna  
  - Percentuale di popolazione in condizioni di svantaggio  

Queste variabili sono state combinate per costruire un **Indice di Benessere Aggregato**, utilizzato nelle visualizzazioni per analizzare l’evoluzione del benessere in Europa tra il 2000 e il 2024.

## Data pre-processing
Spiegare:  
- quali pulizie sono state fatte  
- quali colonne sono state eliminate  
- se sono stati gestiti valori nulli  
- se sono stati creati nuovi campi  


```Python
import pandas as pd

df = pd.read_csv('file.tsv', sep='\t')
print(df.columns)
```

## Data visualizations


### 1. Mappa europea del benessere  
**Cosa mostra:**  
- Una mappa interattiva dei Paesi europei con i valori dell’Indice di Benessere Aggregato dal 2000 al 2024.  
- I colori più scuri indicano un livello di benessere più alto, i colori più chiari valori inferiori.  
- Lo slider temporale permette di osservare come il benessere evolva negli anni.  

**Perché è importante:**  
- Permette di individuare pattern geografici: Nord Europa con valori più alti, Est e Sud Europa con valori più bassi o in recupero.  
- Evidenzia la resilienza dei Paesi durante gli shock economici e sociali (2008, pandemia COVID-19, inflazione 2021–2023, conflitto in Ucraina).  
- Facilita il confronto visivo tra Paesi, mostrando i divari e le aree di miglioramento o peggioramento.


[<img src="assets/images/03.png" width="800" alt="Placeholder image">]()

### 2. Evoluzione temporale del benessere in Europa 
**Cosa mostra:**  
- Grafico a linee che rappresenta l’andamento dell’Indice di Benessere Aggregato medio in Europa.  
- Mostra come i valori medi cambiano nel tempo e reagiscono agli eventi storici principali.  

**Perché è importante:**  
- Evidenzia le tendenze di lungo periodo del benessere europeo.  
- Mostra i picchi e le cadute in corrispondenza di crisi storiche, distinguendo effetti temporanei da trend strutturali.  
- Supporta l’analisi della resilienza complessiva dell’Europa.

[<img src="assets/images/04.png" width="800" alt="Placeholder image">]()

### 3. Confronto Svizzera vs resto d’Europa
**Cosa mostra:**  
- Grafico a barre o linee che confronta l’Indice di Benessere Aggregato della Svizzera con quello di altri Paesi europei.  
- La Svizzera mostra valori elevati e stabili lungo tutto l’arco temporale.  

**Perché è importante:**  
- Evidenzia la Svizzera come outlier positivo in Europa.  
- Permette di osservare quali Paesi sono più sensibili agli shock economici e quali mantengono stabilità.  
- Aiuta a capire le ragioni della resilienza svizzera: servizi di qualità, economia stabile, rete sociale forte.  
- Funziona come punto di riferimento per confrontare sistemi europei diversi.

[<img src="assets/images/04.png" width="800" alt="Placeholder image">]()


## Key findings
Dall’analisi dei dati e dalle visualizzazioni interattive emergono diversi risultati chiave relativi all’evoluzione del benessere in Europa tra il 2000 e il 2024:

1. **Differenze geografiche marcate**  
   - I Paesi del Nord Europa mostrano costantemente livelli di benessere più elevati rispetto a quelli del Sud e dell’Est Europa.  
   - Paesi come Finlandia, Norvegia e Svizzera si collocano tra i più alti in tutte le dimensioni analizzate, mentre alcuni Paesi dell’Europa meridionale e orientale mostrano valori più bassi o maggiormente sensibili agli shock.

2. **Impatto degli shock storici**  
   - Eventi come la crisi finanziaria del 2008, la crisi del debito sovrano (2010-2012), la pandemia di COVID-19 e l’aumento dell’inflazione tra il 2021 e il 2023 si riflettono chiaramente nelle serie temporali dell’indice di benessere.  
   - Durante questi periodi si osservano cali temporanei nei valori medi, con differenze tra Paesi più o meno resilienti.

3. **Tendenze di lungo periodo**  
   - Nonostante gli shock, il benessere europeo mostra un miglioramento graduale nel lungo periodo in molte regioni, soprattutto nei Paesi con economie stabili e sistemi di welfare solidi.  
   - Alcuni Paesi emergono per una progressiva riduzione dei divari interni, mentre altri mostrano una stagnazione o una maggiore vulnerabilità.

4. **Resilienza della Svizzera**  
   - La Svizzera si conferma come un outlier positivo, con valori elevati e stabili durante l’intero arco temporale.  
   - La sua stabilità distingue nettamente il Paese da molti membri dell’UE, evidenziando fattori strutturali di resilienza economica, sociale e politica.  
   - Questo comportamento suggerisce che la combinazione di istituzioni forti, servizi pubblici di qualità e coesione sociale può attenuare l’impatto delle crisi sul benessere.

5. **Pattern emergenti dalle visualizzazioni interattive**  
   - Le mappe e i grafici a linee permettono di identificare facilmente aree di recupero, zone di vulnerabilità e divergenze temporanee tra Paesi.  
   - Lo slider temporale evidenzia come i Paesi reagiscano diversamente agli stessi shock, fornendo indicazioni importanti per politiche mirate di benessere.

In sintesi, l’analisi conferma che il benessere europeo è influenzato sia da fattori strutturali a lungo termine sia da eventi storici specifici, con Paesi come la Svizzera che rappresentano modelli di resilienza da cui è possibile trarre importanti lezioni.

## Next steps
Tellus rutrum tellus pellentesque eu. Dictum sit amet justo donec enim. Aliquam malesuada bibendum arcu vitae elementum curabitur vitae. Sed faucibus turpis in eu mi bibendum neque egestas congue. Tellus in metus vulputate eu scelerisque felis imperdiet proin. Dolor magna eget est lorem ipsum dolor. Sit amet mattis vulputate enim nulla. Elit pellentesque habitant morbi tristique senectus et.