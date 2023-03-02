# Filius-Router

Documentare il problema risolto da questo esercizio, sul Diario di Bordo allegato a questo compito descrivendo:

- A cosa serve il serve DHCP
- Perchè inizialmente i PC delle due reti non si raggiungevano con ping
- Quale protocollo viene utilizzato dal comando ping

1)Il DHCP è un servizio all'interno di un server che assegna un indirizzo IP ad ogni dipsositivo che si collega la rete senza per forza di configuararlo manualemte.

2)Inizialmente i PC delle due reti non si raggiungevano con ping perchè gli Indirizzi IP era tutti uguali e anche perchè non era stato inserito il gateway nè nel router nè nei computer, e quindi se si voleva pingare il pc della'altra rete non si riusciva

3)Il protocollo che viene utilizzato dal comando ping è quello di ARP (Address Resolution Protocol). Il "compito" di questo protocollo e quello di recuperare il MAC per inviare un messaggio ad unaltro computer che non è salvato nella MAC Table, una tabella che contiene tutti i MAC dei vari computer che sono stati pingati in precedenza. I passi per il recupero del MAC sono questi:
Prima di tutto il computer che vuole pingare un altro computer ma non ha il MAC del computer che vuole contattare, manda un messaggio di Broadcast dove nella sezione dell' IP c'è appunto IP del destinatario da trovare e invece nella sezione del MAC c'è scritto "ff:ff:ff:ff:ff:ff". Tutti i computer connessi alla rete ricevono questo messaggio e controllano se è il loro IP. Quando arriva al computer interessato al posto delle "ff:ff:ff:ff:ff:ff" ci sostituisce il su MAC e rimanda il messagio indietro. Il primo computer riceve il messaggio con il MAC aggiornato e finalmente può mandare il messaggio iniziale salvando il MAC del computer pingato nella MAC Table.

                                                              ┍————————————✧/ᐠ-ꞈ-ᐟ\✧———————————┑
                                                  ·͙*̩̩͙✧˚̩̥̩̥*̩̩̥͙·̩̩̥͙*̩̩̥͙☆˚̩̥̩̥*̩̩͙‧♩|     Grazie per l'attenzione    |*:･ﾟ⋄✧☆·͙*̩̩͙˚̩̥̩̥☆*̩̩̥͙·̩̩̥͙*̩̩̥͙˚̩̥̩̥*̩̩͙‧
                                                              ┕————————————(ฅ)(ฅ) ∫∫———————————┙
