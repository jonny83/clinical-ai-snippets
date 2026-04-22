# clinical-ai-snippets

**Short practical examples of how to use AI tools wisely in clinical and biomedical data workflows.**

---

## ⚠️ Who this is for

This repository is **not** for AI experts, data scientists, or machine learning researchers.

It is for clinicians, nurses, residents, and healthcare administrators who occasionally deal with data — spreadsheets, discharge records, operative reports, quality indicators — and who are curious about whether AI tools can help, without necessarily knowing how to code.

The examples here are deliberately simple. Each one starts from a real frustration, a real mistake, or a real misunderstanding, and shows one possible way to do the same thing more reliably.

---

## What you will find here

Each snippet is a self-contained `.Rmd` file that:

- generates a small synthetic dataset (no real patient data, ever)
- produces one or more visualizations
- installs any required R packages automatically if not already present
- compiles to a clean PDF via RStudio with a single click

You do not need to understand every line of code to learn something from these examples. Reading the comments and the output is enough.

---

## Why R and not just AI?

Good question — and it deserves an honest answer.

AI tools (Gemini, ChatGPT, Claude, and others) are genuinely useful. They can draft a summary, explain a statistical concept, translate a table, or suggest a visualization in seconds. We use them too.

But when the output is a chart that will inform a clinical decision, a quality report, or a presentation to hospital management, you want something **reproducible**: the same input should always produce the same output, the colors should be exactly what you specified, and the export should not silently corrupt your data.

That is what a short R script gives you. And here is the key insight: **you do not have to write the script yourself**. You can ask an AI to write it for you, then run it in RStudio. The AI generates the code; the code generates the chart. The chart is always the same.

---

## Example 001 — R vs Gemini on a surgical data chart

> *Triggered by a LinkedIn post from Giacomo, written between ICU handovers at 20:25.*

Giacomo asked Gemini to produce a percentage bar chart from a Google Sheet showing patient outcomes by surgical division. The first chart looked reasonable. Then he asked to change the colors. Then he exported to Sheets. Three steps, three progressively worse results.

This example recreates the same chart in R, adds two alternative visualizations of the same data, and explains in plain language why Gemini failed at this specific task — and what kind of tasks it is actually good at.

📄 [`esempio-ai-clinica-giacomo.Rmd`](./esempio-ai-clinica-giacomo.Rmd)

---

## How to run an example

1. Install [R](https://cran.r-project.org) and [RStudio](https://posit.co/download/rstudio-desktop/) (both free)
2. If you have never compiled a PDF from RStudio, run this once in the R console:
   ```r
   install.packages("tinytex")
   tinytex::install_tinytex()
   ```
   Then restart RStudio.
3. Open the `.Rmd` file and click **Knit → Knit to PDF**
4. All required packages are installed automatically on first run

---

## Contributing

If you have a real example of an AI tool that did not do what you expected in a clinical or biomedical data context — and you found a better way — open an issue or send a pull request. The bar is low: a dataset, a chart, and an honest description of what went wrong.

---

## License

MIT. Use freely, adapt, share. No attribution required, though appreciated.

---

*Maintained by Jonathan Montomoli — intensivist, clinical epidemiologist, occasional coder.*

---
---

# clinical-ai-snippets

**Esempi pratici e brevi su come usare gli strumenti AI in modo utile nei flussi di lavoro con dati clinici e biomedici.**

---

## ⚠️ A chi è rivolto questo repository

Questo repository **non** è per esperti di AI, data scientist o ricercatori di machine learning.

È per medici, infermieri, specializzandi e amministratori sanitari che si trovano occasionalmente a lavorare con dati — fogli Excel, schede di dimissione, report operativi, indicatori di qualità — e che sono curiosi di capire se gli strumenti AI possono aiutare, senza necessariamente saper programmare.

Gli esempi qui raccolti sono volutamente semplici. Ognuno parte da una frustrazione reale, un errore reale, o un malinteso reale, e mostra un modo possibile per fare la stessa cosa in maniera più affidabile.

---

## Cosa troverai qui

Ogni snippet è un file `.Rmd` autonomo che:

- genera un piccolo dataset sintetico (nessun dato reale di paziente, mai)
- produce una o più visualizzazioni
- installa automaticamente i pacchetti R necessari se non già presenti
- si compila in un PDF pulito da RStudio con un singolo clic

Non è necessario capire ogni riga di codice per imparare qualcosa da questi esempi. Leggere i commenti e l'output è già sufficiente.

---

## Perché R e non semplicemente l'AI?

Domanda lecita — e merita una risposta onesta.

Gli strumenti AI (Gemini, ChatGPT, Claude, e altri) sono genuinamente utili. In pochi secondi possono redigere un riassunto, spiegare un concetto statistico, tradurre una tabella, o suggerire una visualizzazione. Li usiamo anche noi.

Ma quando l'output è un grafico che informerà una decisione clinica, un report di qualità, o una presentazione alla direzione ospedaliera, hai bisogno di qualcosa di **riproducibile**: lo stesso input deve produrre sempre lo stesso output, i colori devono essere esattamente quelli che hai specificato, e l'esportazione non deve corrompere i tuoi dati in silenzio.

È quello che ti dà un breve script R. E questo è il punto chiave: **non devi scriverlo tu**. Puoi chiedere a un'AI di scriverlo per te, e poi eseguirlo in RStudio. L'AI genera il codice; il codice genera il grafico. Il grafico è sempre lo stesso.

---

## Esempio 001 — R vs Gemini su un grafico di dati chirurgici

> *Ispirato a un post LinkedIn di Giacomo, scritto tra le consegne in Terapia Intensiva alle 20:25.*

Giacomo ha chiesto a Gemini di produrre un grafico a barre percentuali da un Google Sheet che mostrava gli esiti dei pazienti per divisione chirurgica. Il primo grafico sembrava accettabile. Poi ha chiesto di cambiare i colori. Poi ha esportato in Fogli. Tre passaggi, tre risultati progressivamente peggiori.

Questo esempio ricrea lo stesso grafico in R, aggiunge due visualizzazioni alternative degli stessi dati, e spiega in linguaggio semplice perché Gemini ha fallito in questo specifico task — e per quali tipi di compiti è invece davvero utile.

📄 [`esempio-ai-clinica-giacomo.Rmd`](./esempio-ai-clinica-giacomo.Rmd)

---

## Come eseguire un esempio

1. Installa [R](https://cran.r-project.org) e [RStudio](https://posit.co/download/rstudio-desktop/) (entrambi gratuiti)
2. Se non hai mai compilato un PDF da RStudio, esegui questo una volta nella console R:
   ```r
   install.packages("tinytex")
   tinytex::install_tinytex()
   ```
   Poi riavvia RStudio.
3. Apri il file `.Rmd` e clicca **Knit → Knit to PDF**
4. Tutti i pacchetti necessari vengono installati automaticamente al primo avvio

---

## Contribuire

Se hai un esempio reale di uno strumento AI che non ha fatto quello che ti aspettavi in un contesto di dati clinici o biomedici — e hai trovato un modo migliore — apri una issue o invia una pull request. Il requisito è minimo: un dataset, un grafico, e una descrizione onesta di cosa è andato storto.

---

## Licenza

MIT. Usa liberamente, adatta, condividi. Nessuna attribuzione richiesta, anche se apprezzata.

---

*Mantenuto da Jonathan Montomoli — intensivista, epidemiologo clinico, programmatore occasionale.*
