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
### Problema
{{% /fragment %}}

---

## Dataset di un IDS

{{% fragment %}} 
![](dataset.svg)
{{% /fragment %}}

---

## Una soluzione

{{% fragment %}} 
**Generare** nuovi dati a partire da quelli già esistenti per migliorare i modelli di Machine Learning
{{% /fragment %}}

{{% fragment %}} 
- Soft-Brownian-Offset
{{% /fragment %}}

---


{{% fragment %}} 
**Generare** nuovi dati a partire da quelli già esistenti per migliorare i modelli di Machine Learning
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

## Soft-Brownian-Offset

Algoritmo di generazione di dati 


