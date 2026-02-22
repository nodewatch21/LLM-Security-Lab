# 🔓 LLM Security Lab

**Praktische Sicherheitsforschung an Large Language Models (LLMs)**

Dieses Repository dokumentiert meine praktischen Experimente und Erkenntnisse im Bereich KI-Sicherheit. Alle Tests werden lokal mit Open-Source-Modellen durchgeführt – verantwortungsvoll und zu Lernzwecken.

## 🎯 Ziel

Verstehen, wie LLMs angegriffen werden können, um sie besser absichern zu können. Grundlage ist die [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/).

## 🛠️ Lab-Setup

| Komponente | Details |
|---|---|
| **Plattform** | Windows + Ollama |
| **Modell** | DeepSeek (lokal) |
| **Zweck** | Offensive LLM Security Testing |

## 📁 Struktur

```
LLM-Security-Lab/
├── README.md
├── findings/
│   ├── 001-system-prompt-leakage.md
│   ├── 002-creative-bypass-gedicht.md
│   └── 003-cross-lingual-injection.md
├── owasp-llm-top10/
│   └── uebersicht.md
├── tools/
│   └── nuetzliche-tools.md
└── ressourcen/
    └── lernmaterial.md
```

## 📋 Findings

| Nr. | Titel | OWASP Kategorie | Schweregrad |
|---|---|---|---|
| 001 | [System Prompt Leakage via Zusammenfassung](findings/001-system-prompt-leakage.md) | LLM07 - System Prompt Leakage | Hoch |
| 002 | [Kreative Umgehung via Gedicht](findings/002-creative-bypass-gedicht.md) | LLM07 - System Prompt Leakage | Hoch |
| 003 | [Cross-Lingual Prompt Injection (Französisch)](findings/003-cross-lingual-injection.md) | LLM01 - Prompt Injection | Kritisch |

## 🔬 OWASP Top 10 for LLM Applications

Übersicht und eigene Notizen: [owasp-llm-top10/uebersicht.md](owasp-llm-top10/uebersicht.md)

## 🧰 Tools

Nützliche Tools für LLM Security Testing: [tools/nuetzliche-tools.md](tools/nuetzliche-tools.md)

## 📚 Ressourcen

Lernmaterial und weiterführende Links: [ressourcen/lernmaterial.md](ressourcen/lernmaterial.md)

## ⚠️ Disclaimer

Alle Experimente werden **lokal** und **verantwortungsvoll** durchgeführt. Dieses Repository dient ausschließlich Bildungs- und Forschungszwecken. Die dokumentierten Techniken sollen helfen, KI-Systeme sicherer zu machen – nicht sie zu missbrauchen.

## 👤 Über mich

Angehender Fachinformatiker Systemintegration mit Fokus auf Cloud Security und KI-Sicherheit. Aktuell in Umschulung (2026-2028) mit dem Ziel, als Cloud Security Engineer / AI Security Engineer zu arbeiten.

---

*Dieses Repository wird fortlaufend mit neuen Findings und Experimenten aktualisiert.*
