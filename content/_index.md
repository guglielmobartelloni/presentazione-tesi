+++
title = "Utilizzo di Soft-Brownian-Offset per la generazione di attacchi ai fini dell’addestramento di rilevatori di intrusioni"
outputs = ["Reveal"]
[logo]
src = "logo.svg"
[reveal_hugo]
custom_theme = "reveal-hugo/themes/robot-lung.css"
margin = 0.2
+++

<h1 style="text-transform: inherit; font-size: 2em">Utilizzo di Soft-Brownian-Offset per la generazione di attacchi ai fini dell’addestramento di rilevatori di intrusioni</h1>


---

{{% fragment %}} 
### Intrusion Detection Systems (IDS)
{{% /fragment %}}
{{% fragment %}} 
Applicazione che monitora continuamente la rete per identificare attività malevole.
{{% /fragment %}}
{{% fragment %}} 
![](ids.svg)
{{% /fragment %}}

---

Nell’ultimo decennio si è iniziato ad utilizzare algoritmi di **Machine Learning** per gli IDS.

---

{{% fragment %}} 
### Machine Learning
{{% /fragment %}}
{{% fragment %}} 
La branca dell'**Intelligenza Artificiale** che sviluppa modelli per permettere alle macchine di imparare dai dati.
{{% /fragment %}}

---

{{% fragment %}} 
I modelli di Machine Learning sono sensibili ai dati di addestramento.
{{% /fragment %}}

---

## Dataset di un IDS

{{% fragment %}} 
![](dataset.svg)
{{% /fragment %}}

---

## Possibile metodo miglioramento

{{% fragment %}} 
**Generare** nuovi dati a partire da quelli già esistenti per migliorare i modelli di Machine Learning
{{% /fragment %}}

{{% fragment %}} 
- Soft-Brownian-Offset
{{% /fragment %}}

---

{{% fragment %}} 
## Scopo della tesi
{{% /fragment %}}

{{% fragment %}} 
Cercare di migliorare un IDS utilizzando Soft-Brownian-Offset
{{% /fragment %}}

{{% fragment %}} 
![](scopo.svg)
{{% /fragment %}}


---

## Soft Brownian Offset

{{% fragment %}}
Algoritmo di generazione di dati creato inizialmente per la generazione di eventi anomali.
{{% /fragment %}}

---

## Dataset utilizzati

{{% fragment %}}
- Adfanet
{{% /fragment %}}

<br/>

{{% fragment %}}
- CICIDS
{{% /fragment %}}

---

### Approcci di Generazione

Generazione a partire dalla tipologia di dati:

{{% fragment %}}
- Solo pacchetti normali
{{% /fragment %}}

<br/>

{{% fragment %}}
- Solo pacchetti attacchi
{{% /fragment %}}

<br/>

{{% fragment %}}
- Dataset completo
{{% /fragment %}}


---

## Grafici

Per una valutazione qualitativa degli approcci di generazione.

---

## Generazione
### A partire da pacchetti normali

![](cicids_normal.png)

<img src="legenda.png" style="height: 100px"/>

---

## Generazione
### A partire da pacchetti di attacchi

![](cicids_attack.png)

<img src="legenda.png" style="height: 100px"/>

---

### Approcci di Addestramento del modello

Addestramento usando:

{{% fragment %}}
- Dataset completo + Dati sintetici
{{% /fragment %}}

<br/>

{{% fragment %}}
- Solo pacchetti normali + Dati sintetici
{{% /fragment %}}

<br/>

{{% fragment %}}
- Solo dataset (senza dati generati)
{{% /fragment %}}

---

### Adfanet

|  | Pacchetti normali + Gen      | Dataset Completo + Gen | Solo Dataset |
| ----------- | ----------- | ----------- | ----------- |
| Gen Normali     | 0.3337       | 0.99839 | 0.93596 |
| Gen Attacchi     | 0.4404       | 0.99865 | 0.93596 |
| Gen Completo     | 0.3452       | 0.99854| 0.93596 |

---

{{< slide transition="none">}}

### Adfanet

|  | Pacchetti normali + Gen      | Dataset Completo + Gen | Solo Dataset |
| ----------- | ----------- | ----------- | ----------- |
| Gen Normali     | 0.3337       | 0.99839 | 0.93596 |
| Gen Attacchi     | 0.4404       | **0.99865** | 0.93596 |
| Gen Completo     | 0.3452       | 0.99854| 0.93596 |

---

### CICIDS

|  | Pacchetti normali + Gen      | Dataset Completo + Gen | Solo Dataset |
| ----------- | ----------- | ----------- | ----------- |
| Gen Normali     | -0.1153       | 0.92772 | 0.93596 |
| Gen Attacchi     | -0.1366       | 0.93428 |0.93596 |
| Gen Completo     | -0.1206       | 0.92493| 0.93596 |

---

{{< slide transition="none">}}

### CICIDS

|  | Pacchetti normali + Gen      | Dataset Completo + Gen | Solo Dataset |
| ----------- | ----------- | ----------- | ----------- |
| Gen Normali     | -0.1153       | 0.92772 | **0.93596** |
| Gen Attacchi     | -0.1366       | 0.93428 | **0.93596** |
| Gen Completo     | -0.1206       | 0.92493| **0.93596** |


---

### Conclusioni

{{% fragment %}}
Soft Brownian Offset è efficace nel caso di dataset **semplici**.
{{% /fragment %}}
{{% fragment %}}
In dataset **complessi** invece l'algoritmo non presenta miglioramenti.
{{% /fragment %}}

{{% fragment %}}
In quest'ultimo caso è necessario rivolgersi ad algoritmi differenti.
{{% /fragment %}}

---

### Grazie per l'attenzione
