# OWASP Top 10 for LLM Applications – Übersicht

Referenz: [owasp.org/www-project-top-10-for-large-language-model-applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

## Die 10 größten Sicherheitsrisiken für LLM-Anwendungen

### LLM01: Prompt Injection
**Was ist das?** Angreifer schleusen Anweisungen in die Eingabe ein, die das Modell dazu bringen, seine eigentlichen Regeln zu ignorieren.
**Direkte Injection:** User gibt manipulierte Prompts direkt ein.
**Indirekte Injection:** Schädliche Anweisungen werden über externe Datenquellen eingeschleust (z.B. Webseiten, Dokumente die das Modell liest).
**Eigene Tests:** [Finding 003 - Cross-Lingual Injection](../findings/003-cross-lingual-injection.md)

### LLM02: Sensitive Information Disclosure
**Was ist das?** Das Modell gibt vertrauliche Informationen preis – aus Trainingsdaten, System-Prompts oder Kontext-Dokumenten.
**Risiko:** PII (persönliche Daten), Geschäftsgeheimnisse, API-Keys, interne Prozesse.

### LLM03: Supply Chain Vulnerabilities
**Was ist das?** Angriffe über kompromittierte Komponenten: vortrainierte Modelle, Plugins, Trainingsdaten, Bibliotheken.
**Risiko:** Backdoors in Open-Source-Modellen, vergiftete Datensätze, unsichere Plugins.

### LLM04: Data and Model Poisoning
**Was ist das?** Manipulation der Trainingsdaten oder des Modells selbst, um falsche oder schädliche Ergebnisse zu erzeugen.
**Risiko:** Bias-Einführung, gezielte Fehlinformation, versteckte Trigger im Modell.

### LLM05: Improper Output Handling
**Was ist das?** Die Ausgaben des Modells werden ohne Prüfung an andere Systeme weitergeleitet.
**Risiko:** Code Injection, XSS, SQL Injection – wenn LLM-Output direkt als Code ausgeführt wird.

### LLM06: Excessive Agency
**Was ist das?** Das Modell hat zu viele Berechtigungen und kann eigenständig kritische Aktionen ausführen.
**Risiko:** Unbeabsichtigtes Löschen, Senden, Kaufen – alles was das Modell "im Namen des Users" tun kann.

### LLM07: System Prompt Leakage
**Was ist das?** Der versteckte System-Prompt wird durch geschickte Fragen extrahiert.
**Risiko:** Angreifer sehen interne Regeln, Geschäftslogik, vertrauliche Anweisungen.
**Eigene Tests:** [Finding 001](../findings/001-system-prompt-leakage.md), [Finding 002](../findings/002-creative-bypass-gedicht.md)

### LLM08: Vector and Embedding Weaknesses
**Was ist das?** Schwachstellen in RAG-Systemen (Retrieval Augmented Generation), wo externe Daten in den Kontext eingespeist werden.
**Risiko:** Manipulierte Dokumente in der Wissensdatenbank, vergiftete Embeddings.

### LLM09: Misinformation
**Was ist das?** Das Modell generiert überzeugend klingende aber falsche Informationen (Halluzinationen).
**Risiko:** Besonders gefährlich in medizinischen, rechtlichen oder sicherheitskritischen Kontexten.

### LLM10: Unbounded Consumption
**Was ist das?** Das Modell wird so manipuliert, dass es übermäßig Ressourcen verbraucht.
**Risiko:** Denial of Service, explodierende API-Kosten, Systemüberlastung.

## Status meiner Tests

| OWASP Nr. | Kategorie | Getestet? | Findings |
|---|---|---|---|
| LLM01 | Prompt Injection | ✅ | Finding 003 |
| LLM02 | Sensitive Information Disclosure | ⬜ | – |
| LLM03 | Supply Chain | ⬜ | – |
| LLM04 | Data/Model Poisoning | ⬜ | – |
| LLM05 | Improper Output Handling | ⬜ | – |
| LLM06 | Excessive Agency | ⬜ | – |
| LLM07 | System Prompt Leakage | ✅ | Finding 001, 002 |
| LLM08 | Vector/Embedding Weaknesses | ⬜ | – |
| LLM09 | Misinformation | ⬜ | – |
| LLM10 | Unbounded Consumption | ⬜ | – |
