# La Buca dei Diavoli — Demo

Concept website demo progettato e sviluppato da Punto Due Studio per **La Buca dei Diavoli**, Noceto (PR).

> Concept dimostrativo non commissionato · Punto Due Studio

## Creative thesis

**Sotto la superficie, il fuoco.**

Il concept deriva dal nome del locale come metafora grafica, non da una presunta storia dell'edificio. “Buca” diventa profondità, camera, discesa; “Diavoli” diventa calore, brace e fuoco. Il risultato evita sia il classico sito pizzeria rosso/nero sia un'estetica “inferno” kitsch.

La hero usa una camera astratta costruita in CSS con archi, profondità, brace e una bocca di forno simbolica. Nessuna fotografia di terzi è re-hostata.

## Standard demo — versione finale

La demo applica il quality gate più severo usato da Punto Due Studio:

- ricerca pubblica aggiornata prima del design
- separazione facts / inference / creative choices
- nessun dato commerciale inventato
- concept proprietario derivato dall'identità del business
- portfolio-distance check rispetto a Sanafollia, Sój, Vicolo Stretto, Da Sergio e Crudo & Cotto
- interaction design narrativo, non decorativo
- niente sezioni template se non necessarie
- progressive enhancement
- mobile progettato separatamente
- `prefers-reduced-motion`
- touch targets mobile adeguati
- nessun asset di review site re-hostato
- QA responsive prima del push finale quando l'ambiente lo consente

## Dati verificati utilizzati

Verifica effettuata il 15/09/2026.

- Nome: La Buca dei Diavoli
- Sede demo: Piazza Giovanni Lunardi 21, 43015 Noceto PR
- Telefono: +39 0521 627323
- Email pubblica: bucadeidiavoli@libero.it
- Instagram: @bucadeidiavoli
- Categorie ricorrenti: pizza, italiana; Tripadvisor aggiunge pesce, mediterranea, europea
- Servizi pubblicamente riportati: prenotazioni, tavoli all'aperto, asporto, parcheggio, accessibilità, servizio al tavolo
- Tripadvisor: 4,1/5, 761 recensioni al momento della verifica
- Restaurant Guru: #1 tra i ristoranti italiani a Noceto nella pagina corrente

## Presenza digitale

Restaurant Guru indica `facebook.com` come sito web e Instagram `@bucadeidiavoli`.
Tripadvisor mostra il profilo come richiesto/gestito dal locale.

La demo tratta quindi il problema non come “assenza totale dal web”, ma come **presenza frammentata senza una forte esperienza proprietaria centralizzata**.

## Cucina e menu

La demo NON presenta un menu ufficiale corrente.

Fonti recenti e menu archiviati documentano pizza e proposte stagionali, servizio su tagliere con più gusti citato in una recensione del 2026, cucina di pesce, primi e secondi di mare, carne, salumi e dessert.

I prezzi presenti nei menu online possono essere storici e non vengono quindi mostrati come prezzi attuali.

## Orari e conflitti tra fonti

Restaurant Guru, aggiornato nel 2026, riporta lunedì e mercoledì–domenica 12:00–15:00 / 19:00–00:00 e martedì chiuso.
Tripadvisor e directory aggiornate nel 2025 riportano in alcuni casi chiusure serali anticipate. La demo mostra l'orario della fonte più recente con asterisco e invito esplicito a confermare telefonicamente.

## Seconda sede

Recensioni Tripadvisor 2025 citano due sedi, **Noceto e Fidenza**. Questa demo è deliberatamente focalizzata sulla sede di Noceto e non incorpora contatti/orari della sede di Fidenza.

## Distinctive decisions

1. Hero “camera di fuoco” CSS, non fotografia food standard.
2. Profondità e archi concentrici come sistema visuale.
3. Palette carbone / carta / ember, distinta dal thermal cyan-coral di Crudo & Cotto.
4. Menu come ledger materico, non card.
5. Reputazione come segnale tipografico.
6. Digital gap formulato con cautela: presenza frammentata, non “nessuna presenza”.
7. La parola “forno” è usata solo in senso gastronomico/creativo; la demo non inventa una storia architettonica dell'edificio.

## Funzionalità

- responsive navigation
- click-to-call
- email
- Instagram
- Google Maps
- mobile action dock
- scroll progress
- subtle CSS 3D hero interaction desktop
- magnetic CTA desktop
- progressive reveal
- no-JS readable fallback
- `prefers-reduced-motion`
- keyboard focus states
- touch target mobile minimi
- Schema.org `Restaurant`
- SEO / Open Graph base
- custom 404
- Netlify config
- security headers

## QA responsive completo

QA eseguito il 15/09/2026 con Chromium headless sulla build finale inlined per evitare dipendenze di rete dell'ambiente di test.

Viewport verificati:

- 320 px
- 360 px
- 375 px
- 390 px
- 430 px
- 768 px
- 1024 px
- 1440 px

Controlli completati:

- nessun overflow orizzontale sugli 8 viewport
- nessun errore JavaScript rilevato
- menu mobile aperto correttamente sotto l'header da 320 a 768 px
- nessuna collisione brand / navigazione a 1024 e 1440 px
- mobile dock contenuto nel viewport
- nessun link o button mobile visibile sotto 44 px di altezza nel pass finale
- hero, camera di fuoco, menu ledger, sezione locale, reputazione, orari, contatti, closing e footer controllati responsive
- screenshot visuali finali controllati a 320, 768 e 1440 px

### Fix applicato durante il QA

È stato aggiunto un fail-safe ai reveal: dopo 1,6 secondi tutti i contenuti vengono comunque marcati visibili. L'IntersectionObserver resta l'esperienza primaria, ma browser lenti, automazioni o callback saltate non possono più lasciare testo invisibile.

Esito finale: **PASS** sugli 8 viewport richiesti.

## Deploy Netlify

Sito statico senza build step.

- Base directory: vuota
- Build command: vuoto
- Publish directory: `.`
- Functions directory: vuota

Dopo il deploy aggiungere canonical, `og:url`, sitemap e `og:image` definitivo.
