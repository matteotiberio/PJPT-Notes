# Passive 

Prima di effetivamente ad andare a toccare la macchina andiamo a fare una ricerca con degli strumenti di tutto ciò che ci può essere utile, per questo ricognizione passiva

**Physical/Social:**

Andare fisicamente a captare informazioni utili (cancelli, badge...) oppure usare satelliti (Google Maps...).
Capire anche chi sono le persone che lavorano lì guardando sui social eventuali foto.


**Web/Host:**

-*Target Validation*: WHOIS, nslookup, dnsrecon - serve per capire se il target fornito è giusto.

-*Finding Subdomains*: Google Fu, dig, nmap, sublist3r, bluto, curl, crt.sh... 

-*Fingerprinting*: nmap, wappalyzer, whatweb, builtwith, netcat... 

-*Data Breaches*: haveibeenpwned, breach-parse, weleakinfo


# Identifying our Targets

Abbiamo usato **Bugcrowd** che è un sito per Bug Bounty per fare information gathering verso dei target in-scope.

# Discovering Email Addresses

Usare tools come **hunter.io** permette di scoprire i domini delle email dei target.

Un altro tool utile è **phonebook.cz**

Un modo per validare le email è direttamente su gmail o outlook, immettendo l'email nel campo di login e vedere se esiste.

Oppure con tool come **email checker** ed **email hippo**

# Hunting Breached Credentials 

Ci sono vari modi per trovare delle credenziali breachate, si può usare una lista come **BreachCompilation** e usare qualche tool che ti legga la lista.

Oppure siti come **DeHashed**

# Hunting Subdomains

Quando mettiamo * prima di un dominio, come *.esempio.com, il simbolo “*” rappresenta una *wildcard*, che ricerca tutti  subdomain disponibili per quel dominio.

Un tool utile per cercare i subdomain è **sublist3r** oppure **theHarvester**
Un sito invece è **crt.sh**

**OWASP Amass** é un tool molto utile, ma che richiede un tempo di caricamento molto lungo.

# Identifying Websites

Sapere con cosa é costruito un sito é molto utile. Un tool come BuiltWith puó essere molto utile, un esempio: 

![alt text](/Images/IW.png)

Ci dice tutti i tool usati in un sito specifico, utili per capire delle informazioni in piú.

Un altro tool sottoforma di estensione é **Wappalyzer**. 

É molto utile capire con cosa é costruito un sito, specialmente il suo framework, perché ci puó essere utile per ottenere delle vulnerabilitá specifiche su linguaggi di programmazione, webservers etc...

Un altro tool per fare Informatrion Gathering su un sito é **WhatWeb**

# Information Gathering with Burp Suite

Un tool molto utile per fare information gathering a livello di web é **Burp Suite**.

Burp Suite fa da *proxy*, quindi intercetta le connessioni fra te e un sito.

## Setup Burp Suite:

Per setuppare Burp Suite basta andare nelle impostazioni del browser>proxy>settare 127.0.0.1  (sia per HTTP che per HTTPS).

Andare poi su https://burp e scaricare il certificato cliccanto su CA Certificate.  Andare nelle impostazioni del browser>privacy & security>certificates; ed esportare il certificato precedentemente scaricato.


## Intercettare il traffico con Burp Suite

Burp Suite é molto utile per fare information gathering su un sito perché ti permette di acquisire molte informazioni tramite l'intercettazione delle richieste API.
Si puó anche interagire con le richieste API.