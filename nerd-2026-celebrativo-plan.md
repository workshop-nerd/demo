# Piano: Sito Celebrativo Premiazione Nazionale Progetto NERD 2026

## Panoramica

Sostituire l'attuale pagina placeholder in `docs/index.html` con un sito celebrativo completo, in italiano, per la **Premiazione Nazionale Progetto NERD 2026**. Il sito sarà un singolo file HTML/CSS/JS (`docs/index.html`) servito tramite **GitHub Pages** (già configurato per la cartella `docs/` sul ramo `main` del repository `workshop-nerd/demo`).

**Design system:** Colori IBM ufficiali (Blue #0F62FE, Navy #001141, White #FFFFFF) con accenti oro (#C9A84C). Font IBM Plex Sans (Google Fonts). Responsive via CSS Flexbox/Grid.

---

## Sub-Task 1 — Struttura HTML e layout responsive

**Intent:** Definire lo scheletro semantico del sito con tutte le sezioni necessarie e il layout responsive tramite CSS Grid/Flexbox.

**Expected Outcomes:**
- Pagina con header IBM-branded, 4 sezioni principali, footer
- Layout a colonne su desktop, stacked su mobile
- Font IBM Plex Sans caricato da Google Fonts

**Todo List:**
1. Sostituire interamente `docs/index.html` con la nuova struttura
2. Aggiungere `<head>` con meta responsive, link Google Fonts (IBM Plex Sans), titolo in italiano
3. Creare sezioni: `#hero`, `#countdown`, `#vincitrici`, `#galleria`, `#footer`
4. Aggiungere CSS reset, variabili CSS per i colori IBM + oro, stili base responsive

**Relevant Context:**
- File target: `docs/index.html` (attualmente 34 righe, placeholder)
- Repository GitHub Pages usa la cartella `docs/` su `main`

**Status:** [ ] pending

---

## Sub-Task 2 — Hero section e header IBM-branded

**Intent:** Creare una hero section di impatto visivo che comunichi l'evento con colori IBM e accenti oro.

**Expected Outcomes:**
- Header con logo testuale "Progetto NERD" in stile IBM
- Titolo principale: "Premiazione Nazionale Progetto NERD 2026"
- Sottotitolo in italiano
- Sfondo gradiente IBM Blue to IBM Navy
- Testo oro per elementi di enfasi

**Todo List:**
1. Aggiungere markup hero con titolo, sottotitolo, badge evento
2. Stilare con sfondo `linear-gradient(135deg, #001141, #0F62FE)`
3. Titolo principale in bianco, accenti in oro `#C9A84C`
4. Aggiungere decorazione geometrica IBM-style (bordi, linee)

**Relevant Context:**
- Sezione `#hero` definita in Sub-Task 1
- Colori: `--ibm-blue: #0F62FE`, `--ibm-navy: #001141`, `--gold: #C9A84C`, `--white: #FFFFFF`

**Status:** [ ] pending

---

## Sub-Task 3 — Countdown interattivo JavaScript

**Intent:** Aggiungere un countdown visivo e interattivo impostato sulla data dell'evento (es. 15 maggio 2026).

**Expected Outcomes:**
- 4 card animate: Giorni, Ore, Minuti, Secondi
- Aggiornamento ogni secondo via `setInterval`
- Gestione stato "evento iniziato" quando il countdown raggiunge zero
- Design coerente con palette IBM + oro

**Todo List:**
1. Aggiungere markup sezione `#countdown` con 4 blocchi numerici
2. Scrivere funzione JS `startCountdown(targetDate)` con `setInterval(1000)`
3. Calcolare differenza temporale e aggiornare DOM
4. Aggiungere stile card con bordo oro, numeri grandi in IBM Blue su sfondo bianco
5. Mostrare messaggio "L'evento e' iniziato!" quando countdown = 0

**Relevant Context:**
- Data target suggerita: `2026-05-15T10:00:00` (modificabile)
- Tutto JS inline nel file HTML (nessun file esterno)

**Status:** [ ] pending

---

## Sub-Task 4 — Sezione "Le Vincitrici" con card eleganti

**Intent:** Presentare le vincitrici dell'edizione 2026 con card visivamente curate e dati placeholder realistici.

**Expected Outcomes:**
- Grid responsive di card (3 colonne desktop, 1 mobile)
- Ogni card: avatar/iniziali, nome, citta, categoria premio, citazione
- Card con bordo superiore oro, ombra morbida, hover effect
- 6 card placeholder con nomi e categorie italiane realistiche

**Todo List:**
1. Aggiungere markup `#vincitrici` con titolo sezione e grid di card
2. Creare 6 card placeholder: nome, citta, categoria (AI, Sostenibilita, Social Impact, ecc.), citazione breve
3. Stilare card con `border-top: 4px solid var(--gold)`, box-shadow, transizione hover
4. Avatar con iniziali su cerchio colorato IBM Blue
5. Badge categoria con colore differenziato per tipo

**Relevant Context:**
- Nomi placeholder: italiani femminili (coerenti col tema "Progetto NERD")
- Categorie: AI & Machine Learning, Sostenibilita, Social Impact, Digital Innovation

**Status:** [ ] pending

---

## Sub-Task 5 — Galleria progetti innovativi

**Intent:** Mostrare i progetti finalisti organizzati per categoria tematica con card visive.

**Expected Outcomes:**
- 3 categorie: AI & Machine Learning, Sostenibilita, Social Impact
- 2-3 card per categoria con titolo progetto, descrizione breve, tag tecnologie
- Filtro/tab per categoria (click per mostrare/nascondere, JS vanilla)
- Icone emoji o SVG semplici per rappresentare le categorie

**Todo List:**
1. Aggiungere markup `#galleria` con tab-bar categorie e griglia progetti
2. Creare 9 card progetto placeholder (3 per categoria) con titolo, descrizione, tech tags
3. Stilare tab-bar con indicatore attivo in oro
4. Implementare JS per filtraggio: click su tab mostra/nascondi card per categoria
5. Aggiungere transizione CSS per il cambio categoria

**Relevant Context:**
- Stessa palette e grid del Sub-Task 4
- JS vanilla inline, nessuna dipendenza esterna

**Status:** [ ] pending

---

## Sub-Task 6 — Footer e publish su GitHub Pages

**Intent:** Completare il sito con un footer branded e fare il push del file finale sul repository GitHub per la pubblicazione tramite GitHub Pages.

**Expected Outcomes:**
- Footer con logo testuale, copyright, nota "Powered by IBM Bob"
- File `docs/index.html` committato e pushato su `main`
- Sito accessibile su `https://workshop-nerd.github.io/demo/`

**Todo List:**
1. Aggiungere markup footer con nome evento, anno, nota "Powered by IBM Bob"
2. Stilare footer con sfondo IBM Navy, testo bianco/oro
3. Eseguire `git add docs/index.html`, `git commit`, `git push origin main`
4. Verificare che GitHub Pages sia configurato per servire da `docs/` su `main`

**Relevant Context:**
- Remote: `https://github.com/workshop-nerd/demo.git`
- GitHub Pages URL attesa: `https://workshop-nerd.github.io/demo/`
- Nessun workflow CI/CD necessario: GitHub Pages serve direttamente `docs/`

**Status:** [ ] pending
