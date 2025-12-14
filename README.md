# 📈 Flusso Automatico: Reporting e Analisi AI da Zendesk

Un workflow di **Business Intelligence e Generazione Report**, costruito con **n8n**, che trasforma dati grezzi di Customer Service (da Zendesk) in un report di sintesi professionale, generato e analizzato dall'Intelligenza Artificiale (Gemini).

## Caratteristiche & Funzionalità

* **Data Sourcing Critico:** 📥 Recupera automaticamente tutti i ticket da Zendesk (o da un altro sistema di ticketing), permettendo l'analisi dei volumi, dei tempi di risposta e dei trend.
* **AI Business Analysis:** 🧠 Il nodo **AI Agent** (Gemini) è istruito per analizzare la lista dei ticket (dati non strutturati), riassumere le metriche chiave (es. numero di ticket, problemi più comuni) e generare un report di sintesi in formato Markdown.
* **Generazione File Automatica:** 📝 Il report generato dall'AI viene formattato come un file Markdown e salvato in una cartella designata su **Google Drive**.
* **Notifica di Distribuzione:** 📧 Una volta che il report è salvato, il flusso invia un messaggio su **Slack** contenente il link di condivisione al file di Google Drive.

## Struttura del Flusso

Questo flusso è una pipeline dati completa, dall'acquisizione alla distribuzione:

* **Schedule Trigger:** 🕒 Avvia il flusso automaticamente (es. ogni giorno alle 23:59).
* **Get many tickets (Zendesk):** Acquisizione dei dati di ticketing.
* **Serializza:** 🧹 Prepara il formato dei dati rendendolo ottimale e compresso per l'input di Gemini.
* **AI Agent:** 💡 Esegue l'analisi e la generazione del report di sintesi in Markdown.
* **Format Report (Code):** 🛠️ Formatta l'output Markdown dell'AI come un file binario.
* **Upload file (Google Drive):** 💾 Salva il report su Google Drive.
* **Share file (Slack):** Invia la notifica di disponibilità del report su Slack.

## Video di Spiegazione

Per una spiegazione dettagliata del funzionamento del Sourcing da Zendesk e della configurazione dell'AI Agent per l'analisi dei dati di Business Intelligence, guarda il video qui sotto:

[Spiegazione dettagliata del Flusso Reporting AI su YouTube](https://youtu.be/ZLX-nVJRQrs)

## Requisiti

Per utilizzare questo flusso, è necessario configurare le credenziali per i seguenti servizi:

* **Zendesk API Account**
* **Google Gemini (PaLM) API Account**
* **Google Drive Account**
* **Slack Account**

---

