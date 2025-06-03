# IP Addresses 

## IPv4 e IPv6

IPv4 (Internet Protocol versione 4) e IPv6 (Internet Protocol versione 6) sono due versioni del Protocollo Internet, il protocollo di base che permette la comunicazione su internet. Vengono usati per identificare e localizzare i dispositivi su una rete.

## IPv4

Gli indirizzi IPv4 sono indirizzi numerici a 32 bit rappresentati in formato decimale puntato, come ad esempio "192.168.0.1".
 Ogni sezione, o ottetto, dell’indirizzo è composta da 8 bit e può variare da 0 a 255. Questo permette un totale di circa 4,3 miliardi di indirizzi unici.
 Tuttavia, a causa della crescita rapida di internet, il numero di indirizzi IPv4 disponibili è diventato limitato, portando allo sviluppo di IPv6.

Classi di indirizzi IPv4
Gli indirizzi IPv4 sono divisi in classi, che definiscono la dimensione della rete e dell’host, e aiutano a identificare l’uso previsto degli indirizzi. Le principali classi sono:

| Classe | Intervallo indirizzi | Uso principale | Bit di rete / host |
| A | 0.0.0.0 – 127.255.255.255 | Reti molto grandi | 8 bit rete / 24 bit host |
| B | 128.0.0.0 – 191.255.255.255 | Reti di dimensione media | 16 bit rete / 16 bit host |
| C | 192.0.0.0 – 223.255.255.255 | Reti piccole | 24 bit rete / 8 bit host |
| D | 224.0.0.0 – 239.255.255.255 | Multicast | Non applicabile |
| E | 240.0.0.0 – 255.255.255.255 | Uso futuro o sperimentale | Non applicabile |



• Classe A: destinata a reti molto grandi (es. grandi organizzazioni). Il primo ottetto identifica la rete, i restanti tre sono per gli host.

• Classe B: usata per reti di medie dimensioni. I primi due ottetti identificano la rete, gli ultimi due gli host.

• Classe C: per reti più piccole, come le piccole aziende o reti domestiche.

• Classe D: riservata per indirizzi multicast, usati per trasmissioni a gruppi di destinatari.

• Classe E: riservata per usi futuri o sperimentali, non usata nella rete pubblica.



## IPv6

Gli indirizzi IPv6 sono indirizzi a 128 bit rappresentati in formato esadecimale, come ad esempio "2001:0db8:85a3:0000:0000:8a2e:0370:7334".
 La lunghezza maggiore degli indirizzi IPv6 permette di avere un numero molto più grande di indirizzi unici, circa 3,4×10^38.
 Gli indirizzi IPv6 sono divisi in otto gruppi di quattro cifre esadecimali, separati da due punti (:).
 Gli zeri iniziali di un gruppo possono essere omessi e gruppi consecutivi di zeri possono essere abbreviati con una doppia due punti (::) per semplificare la scrittura.

## Transizione da IPv4 a IPv6

La transizione da IPv4 a IPv6 è necessaria per via dell’esaurimento degli indirizzi IPv4 disponibili.
 IPv6 offre una soluzione al problema della scarsità di indirizzi, introducendo anche miglioramenti in termini di sicurezza, configurazione automatica e altre funzionalità.
 Tuttavia, IPv4 e IPv6 non sono direttamente compatibili tra loro, quindi sono stati sviluppati meccanismi e tecnologie di transizione per permettere la comunicazione tra i due protocolli.

*In sintesi:*

IPv4 e IPv6 sono versioni del Protocollo Internet che forniscono indirizzi unici ai dispositivi su una rete.
 Gli indirizzi IPv4 sono a 32 bit, mentre quelli IPv6 sono a 128 bit.
 IPv6 offre uno spazio di indirizzamento molto più ampio e caratteristiche aggiuntive rispetto a IPv4.


# MAC Addresses

Le prime 3 coppie di un MAC sono identificativi del produttore.

Possiamo usare dei tool come MAC Address and OUI Lookup per determinare i vendor specifici:

![alt text](/Images/MAC.png)

In questo caso 52:54:00 corrisponde all'identificativo della RealtekU


# TCP, UDP and THree-Way Handshake

TCP = Transimission Control Protocol - Connection Oriented Protocol - High reliability (http, https, ssh...)
UDP = User Datagram Protocol - Connection Less Protocol - (dns, voip...)

SYN - SYNCRONIZE
SYN ACK - SYNCRONIZE ACKNOWEGMENT
ACK - ACKNOWEGMENT

Manda un pacchetto SYN ad una porta o servizio specifico, la porta risponde con SYN ACK per dire che la porta è disponibieile e poi risponde con un ACK :


![alt text](/Images/TWH.png)


**Pacchetto 280:**  IP 192.169.57.139 manda un pacchetto SYN all'ip 74.125.21.155 dalla porta 52610 alla 443

**Pacchetto 284:** L'ip 74.125.21.155 risponde con un SYN ACK dalla porta 443 alla 52610

**Pacchetto 285:** Connessione effettuata

# Common Ports and Protocols

Ecco alcune porte comunemente usate e i protocolli associati nel networking:

• **FTP** (File Transfer Protocol): Porta 21 (TCP)

• **SSH** (Secure Shell): Porta 22 (TCP)

• **Telnet** Porta 23 (TCP)

• **SMTP** (Simple Mail Transfer Protocol): Porta 25 (TCP)

• **DNS** (Domain Name System): Porta 53 (TCP e UDP)

• **HTTP** (Hypertext Transfer Protocol): Porta 80 (TCP)

• **HTTPS** (Hypertext Transfer Protocol Secure): Porta 443 (TCP)

• **DHCP** (Dynamic Host Configuration Protocol): Porta 67 (UDP) e 68 (UDP)

• **POP3** (Post Office Protocol version 3): Porta 110 (TCP)

• **IMAP** (Internet Message Access Protocol): Porta 143 (TCP)

• **SNMP** (Simple Network Management Protocol): Porta 161 (UDP)

• **RDP** (Remote Desktop Protocol): Porta 3389 (TCP)

• **NTP** (Network Time Protocol): Porta 123 (UDP)

• **SMB** (Server Message Block): Porta 445 (TCP)

• **FTPS** (FTP over SSL/TLS): Porta 990 (TCP)

• **TFTP** (Trivial File Transfer Protocol): Porta 69 (UDP)

• **LDAP** (Lightweight Directory Access Protocol): Porta 389 (TCP e UDP)

• **MySQL** Porta 3306 (TCP)



*Nota:*
Alcuni protocolli usano sia TCP che UDP, a seconda della funzionalit√† specifica. Inoltre, queste assegnazioni di porte non sono esaustive: molte altre applicazioni e servizi possono usare porte diverse o personalizzate.

# The OSI Model

Il **modello OSI** (Open Systems Interconnection) è un quadro concettuale che standardizza le funzioni di un sistema di comunicazione in sette livelli distinti. Ogni livello ha responsabilità specifiche e interagisce con i livelli sopra e sotto di esso. Il modello OSI fornisce un approccio strutturato per comprendere e progettare protocolli di rete e sistemi di comunicazione. Ecco una breve panoramica di ogni livello:

• **Livello fisico (Physical Layer):**
 Il livello fisico è responsabile della trasmissione e ricezione di bit di dati grezzi e non strutturati su un mezzo fisico. Definisce le caratteristiche elettriche, meccaniche e funzionali dell’interfaccia fisica tra i dispositivi.

• **Livello data link (Data Link Layer):**
 Il livello data link gestisce la trasmissione affidabile di frame dati tra nodi direttamente connessi su un collegamento fisico. Fornisce rilevazione e correzione degli errori, controllo del flusso e gestisce l’accesso al mezzo fisico. Ethernet, Wi-Fi e PPP (Point-to-Point Protocol) sono esempi di protocolli di questo livello.

• **Livello rete (Network Layer):**
 Il livello rete permette il routing dei pacchetti dati attraverso diverse reti. Si occupa dell’indirizzamento logico e determina il percorso migliore per la consegna dei dati basandosi sulle condizioni di rete e sui protocolli di routing. L’IP (Internet Protocol) è un protocollo chiave di questo livello.

• **Livello trasporto (Transport Layer):**
 Il livello trasporto garantisce la consegna affidabile e ordinata dei dati tra sistemi finali. Suddivide i dati in segmenti più piccoli, gestisce la comunicazione end-to-end e fornisce il recupero dagli errori, il controllo del flusso e della congestione. TCP (Transmission Control Protocol) e UDP (User Datagram Protocol) operano a questo livello.

• **Livello sessione (Session Layer):**
 Il livello sessione stabilisce, gestisce e termina le sessioni di comunicazione tra applicazioni. Fornisce meccanismi di sincronizzazione e controllo del dialogo per abilitare una comunicazione fluida tra dispositivi. Gestisce anche il checkpointing e il recupero delle sessioni.

• **Livello presentazione (Presentation Layer):**
 Il livello presentazione è responsabile della rappresentazione dei dati, della crittografia, compressione e formattazione. Garantisce che i dati inviati dal livello applicazione di un sistema siano comprensibili dal livello applicazione di un altro sistema. Si occupa della sintassi e della semantica dei dati.

• **Livello applicazione (Application Layer):**
 Il livello applicazione è il livello più vicino all’utente finale e fornisce servizi direttamente alle applicazioni utente. Include protocolli per vari servizi di livello applicativo come trasferimento file, email, navigazione web e accesso remoto. Esempi di protocolli a questo livello sono HTTP, SMTP, FTP e DNS.



C'è un sistema mnemonico utile per ricordarsi i vari Layter:

-*Please* : Physical (Data,  Cavi, Cat6...)

-*Do*: Data (Switching, MAC Address)

-*Not*: Network (IP Addresses, routing*...)

-*Throw*: Transport (TCP/UDP)

-*Sausage*: Session (Session Management)

-*Pizza*: Presentation (WMV, JPEG, MOV...)

-*Away*: Application (HTTP, SMTP...)


*routing* = instradare i dati all'interno di una rete o tra reti diverse, cioè decidere il percorso migliore che un pacchetto di dati deve seguire per arrivare dalla sua origine alla destinazione:
quando invii un messaggio o un file via internet o in una rete, i dati non viaggiano direttamente da te al destinatario.
I dati passano attraverso diversi dispositivi di rete chiamati router.
Il router legge l'indirizzo di destinazione del pacchetto dati e decide su quale strada inviarlo, basandosi su una tabella di instradamento e regole specifiche.
Questo processo di scelta del percorso e inoltro dei pacchetti si chiama routing.
Permette di collegare reti diverse tra loro (es. la tua rete domestica con internet).
Ottimizza il traffico dati, evitando percorsi sovraccarichi o guasti.
Consente la comunicazione globale tra milioni di dispositivi.

# Subnetting 



*Risorse:*

-Seven Second Subnetting: https://www.youtube.com/watch?v=ZxAwQB8TZsM
-Subnet Guide: https://drive.google.com/file/d/1ETKH31-E7G-7ntEOlWGZcDZWuukmeHFe/view









