# RaiPlay Sound Feed

Questo repository genera dei feed RSS per i programmi di RaiPlay Sound, e sono generati automaticamente tramite GitHub Actions e GitHub Pages. In modo da potersi abbonare/ascoltare su qualsiasi client podcast  e non esclusivamente tramite l’app RaiPlaySound. 


## Podcast

| Programma | Feed RSS |
|----------|----------|
| America7 | https://valluanino.github.io/raiplaysound-feed/rss/programmi/america7.xml |
| Atacama, la terra dei telescopi | https://valluanino.github.io/raiplaysound-feed/rss/programmi/atacamalaterradeitelescopi.xml |
| Eta Beta | https://valluanino.github.io/raiplaysound-feed/rss/programmi/etabeta.xml |
| GR Puglia | https://valluanino.github.io/raiplaysound-feed/rss/programmi/grpuglia.xml |
| GR1 | https://valluanino.github.io/raiplaysound-feed/rss/programmi/gr1.xml |
| Lillo e Greg 610 | https://valluanino.github.io/raiplaysound-feed/rss/programmi/lilloegreg610.xml |
| Number Stations - Le radio delle spie | https://valluanino.github.io/raiplaysound-feed/rss/programmi/numberstations-leradiodellespie.xml |
| Pillole di Eta Beta | https://valluanino.github.io/raiplaysound-feed/rss/programmi/pilloledietabeta.xml |
| Prima Pagina | https://valluanino.github.io/raiplaysound-feed/rss/programmi/primapagina.xml |
| Radio3 Mondo | https://valluanino.github.io/raiplaysound-feed/rss/programmi/radio3mondo.xml |
| Radio3 Scienza | https://valluanino.github.io/raiplaysound-feed/rss/programmi/radio3scienza.xml |
| Revolution | https://valluanino.github.io/raiplaysound-feed/rss/programmi/revolution.xml |
| Tutta la città ne parla | https://valluanino.github.io/raiplaysound-feed/rss/programmi/tuttalacittaneparla.xml |
| Un giorno da pecora | https://valluanino.github.io/raiplaysound-feed/rss/programmi/ungiornodapecora.xml |

## Audiolibri

| Audiolibro | Feed RSS |
|------------|----------|
| Arancia meccanica | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/aranciameccanica.xml |
| Cuore di tenebra | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/cuoreditenebra.xml |
| Flush. Una biografia | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/flushunabiografia.xml |
| Frankenstein | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/frankenstein.xml |
| Gli indifferenti | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/gliindifferenti.xml |
| I promessi sposi | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/ipromessisposi.xml |
| I tre moschettieri | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/itremoschettieri.xml |
| Il grande Gatsby | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/ilgrandegatsby.xml |
| Mansfield Park | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/mansfieldpark.xml |
| Racconti di Italo Calvino | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/raccontidiitalocalvino.xml |
| Ventimila leghe sotto i mari | https://valluanino.github.io/raiplaysound-feed/rss/audiolibri/ventimilaleghesottoimari.xml |

## Abbonarsi o aggiungere un feed

Per abbonarsi basta copiare l'URL del feed dalla tabella nel lettore podcast.

Per aggiungere programmi o audiolibri puoi forkare il repository e aggiungere manualmente i feed, oppure aprire una Pull Request modificando [static.ts](https://github.com/giuliomagnifico/raiplaysound-feed/blob/main/src/static.ts), esempio:

```ts
{
  title: 'Radio3 Scienza',
  path: 'programmi/radio3scienza'
}
```

oppure per un audiolibro:

```ts
{
  title: 'Arancia meccanica',
  path: 'audiolibri/aranciameccanica'
}
```

> [!NOTE]
> la tabella con i feeds o audiolibri nuovi si aggiorna  automaticamente con il nuovo feed (in ordine alfabetico) quando viene eseguita la Action, non aggiungere o modificare manualmente la tabella.

## Aggiornamento ogni ora

I feed vengono aggiornati automaticamente tramite GitHub Actions ogni ora e viene controllata la validità degli URL vecchi ogni 14 giorni.

## INFO

Questo progetto è una evoluzione di un mio [precedente repository](https://github.com/giuliomagnifico/raiplay-feed),  il quale aveva il problema di non risolvere correttamente la redirect ed era quindi necessario scaricare il file prima di riprodurlo certi podcast. Adesso gli URLs vengono risolti fino alla CDN finale Rai, evitando i problemi causati dai redirect `relinkerServlet.htm` con alcuni client podcast (i.e. [PocketCasts](https://pocketcasts.com/)).


> [!TIP]
> È una versione modificata del repository [frammenti/raiplaysoundrss](https://github.com/frammenti/raiplaysoundrss) costruita per poter funzionare usando solo su GitHub, in modo da essere indipendente da un server esterno. 

