---
title: Staking come servizio
description: Una panoramica di come iniziare con lo staking in pool di ETH
lang: it
template: staking
emoji: ":money_with_wings:"
image: ../../../../../assets/staking/leslie-saas.png
alt: Leslie il rinoceronte che fluttua tra le nuvole.
sidebarDepth: 2
summaryPoints:
  - Gli operatori di nodi di terze parti gestiscono l'operazione del tuo client del validatore
  - Ottima opzione per chiunque abbia 32 ETH e non si senta a proprio agio nell'affrontare la complessità tecnica dell'esecuzione di un nodo
  - Riduce la fiducia e mantiene la custodia delle tue chiavi di prelievo
---

## Cos'è lo staking come un servizio? {#what-is-staking-as-a-service}

Lo staking come un servizio ("SaaS") rappresenta una categoria di servizi di staking in cui depositi i tuoi 32 ETH per un validatore, ma deleghi le operazioni del nodo a un operatore di terze parti. Solitamente questo processo coinvolge la guida alla configurazione iniziale, inclusa la generazione della chiave e il deposito e il successivo caricamento delle tue chiavi di firma all'operatore. Questo consente al servizio di operare il tuo validatore per tuo conto, solitamente per una commissione mensile.

## Perché mettere in staking con un servizio? {#why-stake-with-a-service}

Il protocollo di Ethereum non supporta nativamente la delegazione dello staking, quindi questi servizi sono stati creati per soddisfare questa domanda. Se hai 32 ETH da mettere in staking, ma non hai dimestichezza con l'hardware, i servizi di SaaS ti consentono di delegare la parte hardware e ottenere le ricompense del blocco nativo.

<CardGrid>
  <Card title="Il tuo validatore" emoji=":desktop_computer:" description="Deposit your own 32 ETH to activate your own set of signing keys that will participate in Ethereum consensus. Monitor your progress with dashboards to watch those ETH rewards accumulate." />    
  <Card title="Facile iniziare" emoji="🏁" description="Forget about hardware specs, setup, node maintenance and upgrades. SaaS providers let you to outsource the hard part by uploading your own signing credentials, allowing them to run a validator on your behalf, for a small cost." />
  <Card title="Limita i tuoi rischi" emoji=":shield:" description="In many cases users do not have to give up access to the keys that enable withdrawing or transferring staked funds. These are different than the signing keys, and can be stored separately to limit (but not eliminate) your risk as a staker." />
</CardGrid>

<StakingComparison page="saas" />

## Cosa considerare {#what-to-consider}

Esiste un numero crescente di fornitori di SaaS, per aiutarti a mettere i tuoi ETH in staking, ma ognuno presenta diversi benefici e rischi. Dovresti considerare che tutte le opzioni di SaaS richiedono ipotesi di fiducia aggiuntive, rispetto allo staking domestico. Le opzioni di SaaS potrebbero contenere del codice aggiuntivo, avvolto dai client di Ethereum, che non è aperto o verificabile. I SaaS hanno inoltre un effetto negativo sulla decentralizzazione della rete. A seconda della configurazione, potresti non controllare il tuo validatore; l'operatore potrebbe agire in modo disonesto, utilizzando i tuoi ETH.

Gli indicatori d'attributo sono usati di seguito per segnalare notevoli punti di forza o debolezze che un fornitore di SaaS elencato potrebbe avere. Usa questa sezione come un riferimento per come definiamo questi attributi mentre stai scegliendo un servizio per aiutarti con il tuo percorso di staking.

<StakingConsiderations page="saas" />

## Esplora i fornitori del servizio di staking {#saas-providers}

Di seguito alcuni fornitori di SaaS disponibili. Usa i suddetti indicatori per orientarti tra questi servizi

<InfoBanner emoji="⚠️" isWarning>
Ricorda l'importanza di supportare la <a href="/developers/docs/nodes-and-clients/client-diversity/">diversità del client</a> poiché migliora la sicurezza della rete e limita i tuoi rischi. I servizi per i quali è dimostrato che limitino l'uso del client di maggioranza sono contrassegnati come <em style="text-transform: uppercase;">"client diversi."</em>
</InfoBanner>

#### Fornitori di SaaS

<StakingProductsCardGrid category="saas" />

#### Generatori di chiavi

<StakingProductsCardGrid category="keyGen" />

Hai un suggerimento per un fornitore di staking come servizio che abbiamo dimenticato? Dai un'occhiata alla nostra [politica di elenco dei prodotti](/contributing/adding-staking-products/) per vedere se sarebbe adatto e sottoporcelo.

## Domande frequenti {#faq}

<ExpandableCard title="Chi detiene le mie chiavi?" eventCategory="SaasStaking" eventName="clicked who holds my keys">
  Le disposizioni differiranno da fornitore a fornitore, ma in genere, sarai guidato alla configurazione di qualsiasi chiave di firma necessaria (una per 32 ETH) e al loro caricamento al tuo fornitore per consentirgli di validare per conto tuo. Le sole chiavi di firma non danno alcuna possibilità di prelevare, trasferire o spendere i tuoi fondi. Tuttavia, forniscono la possibilità di trasmettere voti a favore di un consenso, il che, se non fatto propriamente, può risultare in sanzioni offline o tagli.
</ExpandableCard>

<ExpandableCard title="Quindi esistono due serie di chiavi?" eventCategory="SaasStaking" eventName="clicked so there are two sets of keys">
Sì. Ogni conto si compone sia di chiavi di <em>firma</em> che di chiavi di <em>prelievo</em> BLS. Affinché un validatore possa attestare allo stato della catena, partecipare ai comitati di sincronizzazione e proporre blocchi, le chiavi di firma devono essere prontamente accessibili dal client di un validatore. Queste devono esser connesse a Internet in qualche modo e sono dunque intrinsecamente considerate chiavi "calde". Questo è un requisito affinché il tuo validatore possa attestare e, dunque, le chiavi usate per trasferire o prelevare i fondi sono separate per motivi di sicurezza.

Le chiavi di prelievo BLS sono utilizzate per firmare un messaggio una tantum che dichiara a chi dovrebbero andare le ricompense di staking del conto del livello d'esecuzione e i fondi prelevati. Una volta trasmesso questo messaggio, le chiavi di <em>prelievo BLS</em> non saranno più necessarie. Invece, il controllo dei fondi prelevati è permanentemente delegato all'indirizzo fornito. Ciò consente di impostare un indirizzo di prelievo protetto tramite l'archiviazione a freddo, minimizzando il rischio per i tuoi fondi del validatore, anche se qualcun altro controlla le chiavi di firma del tuo validatore.

Aggiornare le credenziali di prelievo è un passaggio necessario per abilitare i prelievi con l'aggiornamento Shanghai. Questo processo comporta la generazione delle chiavi di prelievo, utilizzando la tua frase di seed mnemonica. <em>Assicurati di eseguire il backup di questa frase di seed in sicurezza o non potrai generare le tue chiavi di prelievo quando arriverà il momento.</em>

Gli staker che lo hanno già fornito con il deposito iniziale, non dovranno impostare un indirizzo di prelievo. Confrontati con il tuo fornitore SaaS per ricevere assistenza con la preparazione del validatore.
</ExpandableCard>

<ExpandableCard title="Quando posso prelevare?" eventCategory="SaasStaking" eventName="clicked when can I withdraw">
Quando metti 32 ETH in stake con un fornitore di SaaS, quegli ETH sono ancora depositati al contratto di deposito di staking ufficiale. Come tali, gli staker di SaaS sono limitati dalle stesse limitazioni di prelievo degli staker in solo e i prelievi non saranno abilitati fino all'aggiornamento Shanghai.

I prelievi di staking saranno implementati nel prossimo aggiornamento Shanghai, previsto tra il primo e il secondo trimestre del 2023. Dopodiché, gli staker dovranno fornire un indirizzo di prelievo (se non è fornito sul deposito iniziale) e i pagamenti delle ricompense inizieranno a essere distribuiti automaticamente su base periodica ogni pochi giorni.

Ciò consentirà anche di sbloccare i fondi usciti. I validatori possono uscire completamente da tale ruolo e riceveranno il loro saldo per intero all'indirizzo di prelievo fornito.

<ButtonLink to="/staking/withdrawals/">Di più sulle ricompense di staking</ButtonLink>
</ExpandableCard>

<ExpandableCard title="Cosa succede se vengo tagliato?" eventCategory="SaasStaking" eventName="clicked what happens if I get slashed">
Usando un fornitore di Saas, affidi l'operazione del tuo nodo a qualcun altro. Questo comporta il rischio delle scarse prestazioni del nodo, che non dipendono da te. Nell'evento in cui il tuo validatore sia tagliato, il saldo del tuo validatore sarà sanzionato e forzatamente rimosso dal pool dei validatori. Questi fondi saranno bloccati finché i prelievi non saranno abilitati a livello del protocollo.

L'imminente aggiornamento Shanghai introduce la funzionalità di prelievo, che ai fini dell'attivazione richiede di fornire un indirizzo di prelievo. Questo potrebbe essere stato fornito al deposito iniziale. Altrimenti, le chiavi di firma del validatore dovranno essere utilizzate per firmare un messaggio che dichiari un indirizzo di prelievo, al momento dell'aggiornamento.

Contatta il singolo fornitore di SaaS per ulteriori dettagli su qualsiasi opzione di garanzia o assicurazione e per le istruzioni su come fornire un indirizzo di prelievo. Se preferisci avere il pieno controllo della configurazione del tuo validatore, <a href="/staking/solo/">scopri di più su come fare staking in solo dei tuoi ETH</a>.
</ExpandableCard>

## Approfondimenti {#further-reading}

- [Valutare i servizi di Staking](https://www.attestant.io/posts/evaluating-staking-services/) - _Jim McDonald 2020_
