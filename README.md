# Wari

[![Versione](https://img.shields.io/badge/versione-1.0-blue)](#versioni)
[![Licenza: AGPL v3](https://img.shields.io/badge/licenza-AGPL--3.0-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-222?logo=github)](#pubblicazione-su-github-pages)
[![HTML5](https://img.shields.io/badge/HTML5-single%20file-E34F26?logo=html5&logoColor=white)](index.html)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES2020-F7DF1E?logo=javascript&logoColor=black)](index.html)
[![Lingua](https://img.shields.io/badge/lingua-italiano-green)](#)

Versione per browser del wari (oware, awalé, warri), il più diffuso dei mancala. È una singola pagina HTML, senza build, senza dipendenze e senza installazione. Condivide l'architettura del Gioco Reale di Ur e del Senet: motore di gioco separato dall'interfaccia, animazioni, audio sintetizzato, storia e regole illustrate. Il wari non ha elementi casuali, quindi non ci sono dadi.

## Caratteristiche

- **Regole abapa**, quelle delle competizioni internazionali, con la variante dei Caraibi per il grand slam selezionabile.
- **Avversario**: computer a tre livelli (principiante, intermedio, esperto) o due giocatori sullo stesso schermo. Il computer usa una ricerca alfa-beta; la valutazione considera semi catturati, mosse in mano (come nel testo di Chamberlin) e case vulnerabili.
- **Tavoliere** in legno con case incavate e semi, con o senza granai (senza granai i semi catturati vanno su un tappetino «in mano»).
- **Semina animata** seme per seme, con catture che confluiscono nel granaio; anteprima della semina e di ciò che si cattura (disattivabile); suggerimento del computer.
- **Audio** sintetizzato con Web Audio: effetti sonori (attivi di default; le note della semina seguono una scala pentatonica) e colonna sonora di ispirazione africana (disattivata di default): mbira a due voci incrociate, balafon, djembe, campana e shekere in metro 12/8, con frasi in botta e risposta. La scelta è salvata nel browser.
- **Regole illustrate**: 15 passi animati, dalla semina alla strategia (mosse in mano, casa grande, apertura).
- **Storia**: sequenza a titoli cinematografici sulla famiglia dei mancala e sul wari. Durante la storia lo schermo del cellulare resta acceso.
- Tema chiaro e scuro automatico, layout adattabile a schermi piccoli. Con «riduci movimento» attivo nel sistema operativo le animazioni sono disattivate.

## Regole in breve

Dodici case, 48 semi, 4 per casa. Si prende il contenuto di una propria casa e lo si semina in senso antiorario, uno per casa, saltando la casa di partenza. Se l'ultimo seme cade in una casa avversaria che arriva a 2 o 3 semi, la si cattura, insieme alle case precedenti contigue che hanno 2 o 3 semi. Vince chi cattura 25 semi; con 24 a 24 è pareggio. Se l'avversario non ha semi, si deve giocare una semina che glieli dia; se non è possibile, si prendono i semi rimasti e la partita finisce. Il grand slam non cattura nulla (abapa).

Il dettaglio è nel pannello «Regole, strategia, interpretazioni e fonti» della pagina.

## Interpretazioni e limiti

- **Grand slam**: nell'abapa (Wikipedia) la mossa è valida ma non cattura; nel testo di Chamberlin (Caraibi) cattura tutto e chi ha catturato deve poi dare da mangiare. Entrambe sono selezionabili; il default è l'abapa.
- **Stallo**: il gioco da tavolo lo risolve con un accordo tra i giocatori. Qui la partita termina alla terza ripetizione della stessa posizione con lo stesso giocatore di turno, o dopo 400 mosse, e ciascuno prende i semi della propria fila.
- **Computer**: il livello Esperto è limitato a circa 0,4 secondi per mossa, quindi non è un giocatore perfetto. L'ordine di forza dei livelli è stato verificato con partite simulate (esperto contro intermedio e intermedio contro principiante, tutte vinte dal livello superiore su 6 partite per coppia, con inizio alternato); non è una misura di forza assoluta.
- **Audio**: i suoni sono generati proceduralmente e non sono stati ascoltati dall'autore del codice; il giudizio sul risultato musicale è lasciato all'ascolto.

Il motore è stato verificato con 800 partite casuali complete (conservazione dei 48 semi, terminazione, mosse sempre disponibili) e con scenari ripresi dal testo di Chamberlin (dodicesima buca, cattura, catena, dar da mangiare, grand slam, stallo).

## Avvio

Apri `index.html` in un browser moderno. La pagina carica da Google Fonts, se raggiungibile, i caratteri; senza, usa quelli di sistema.

## Pubblicazione su GitHub Pages

1. Copia `index.html` nella radice del repository.
2. In *Settings → Pages* scegli il branch (ad esempio `main`) e la cartella `/ (root)`.
3. La pagina sarà all'indirizzo `https://<utente>.github.io/<repository>/`.

## Versioni

| Versione | Contenuto |
|---|---|
| 1.0 | Gioco completo con regole abapa e variante dei Caraibi, computer a tre livelli, animazioni, audio, storia e regole illustrate. |

## Fonti

- Voce «Wari», Wikipedia in italiano, e voce «Oware», Wikipedia in inglese (regole dell'abapa).
- Voci «Mancala», Wikipedia in italiano e in inglese (storia e famiglia dei mancala).
- David Chamberlin, *How to play warri* (regole dei Caraibi e strategia).

## Licenza

Copyright © 2026 Alessandro Valli.

Questo programma è software libero: puoi ridistribuirlo e modificarlo secondo i termini della GNU Affero General Public License, versione 3 o successiva. Se fornisci una versione modificata come servizio in rete, devi renderne disponibile il codice sorgente agli utenti. Il programma è distribuito senza alcuna garanzia. Testo completo: [LICENSE](LICENSE) e <https://www.gnu.org/licenses/agpl-3.0.html>.
