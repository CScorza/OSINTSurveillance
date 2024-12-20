![Immagine1](https://github.com/CScorza/OSINTSurveillance/assets/98583912/8a4d4fe5-114d-436b-90d1-4e128db5f2f9)

# *Strumenti utili per la ricerca di WebCam, Canali d'Informazione e Wifi di pubblico accesso per la raccolta di informazioni utili all'attività di Analisi.*

*Useful tools for searching for webcams, information channels, and public access Wi-Fi for gathering information relevant to analysis activities.*

![Telecamere](https://github.com/CScorza/OSINTSurveillance/assets/98583912/33a5859d-6d5f-4e1b-ac5f-98ee20e8e31e)


|**INDICE**|**AIUTI ALL'INVESTIGAZIONE**||
| :--- | :--- | :--- |
|[**CCTV - WEBCAMS - Social Video Live**](https://github.com/CScorza/OSINTSurveillance/tree/main#cctv---webcams---social-video-live)|[**OPEN WIFI**](https://github.com/CScorza/OSINTSurveillance/tree/main#open-wifi)|[**OSINT IP**](https://github.com/CScorza/OSINTSurveillance/tree/osint-ip)|

```
Gli analisti OSINT possono utilizzare le telecamere pubbliche per raccogliere informazioni su una varietà di argomenti
Ciò può essere utile per le autorità per la sicurezza pubblica per garantire
la sicurezza dei cittadini e per i giornalisti per informare il pubblico. 
Telecamere pubbliche
Posizione e movimenti delle persone: Le telecamere pubbliche possono fornire agli analisti OSINT informazioni
sulla posizione delle persone, sui loro movimenti e sulle loro interazioni. 
```
```
OSINT analysts can use public cameras to gather information on a variety of topics.
This can be useful for public safety authorities to ensure the security of citizens and for journalists to inform the public.

Public Cameras
Location and movements of people: Public cameras can provide OSINT analysts with information about people's locations, movements, and interactions.
```

# CCTV - WEBCAMS - Social Video Live
![World Cam](https://user-images.githubusercontent.com/98583912/202259674-34a165d5-98af-44e7-aae0-4a108b15de49.gif)

[**Shodan**](https://www.shodan.io/)
🇮🇹
```
Shodan è un motore di ricerca che permette di trovare dispositivi connessi a Internet, 
tra cui webcam, router, NAS e altri dispositivi remoti.
È uno strumento potente che può essere utilizzato per scopi legittimi, 
come la ricerca di vulnerabilità di sicurezza, ma può anche essere utilizzato per scopi, come la sorveglianza.

Per utilizzare Shodan per trovare telecamere online, 
è necessario prima registrarsi per un account gratuito. Una volta registrato, 
è possibile accedere al sito Web di Shodan e iniziare a cercare.

Ecco alcuni esempi di query che è possibile utilizzare per trovare telecamere online:

- "webcam" - 
Questa query restituirà tutti i dispositivi che hanno la parola "webcam" nel loro nome o nei metadati.
- "country:IT" - 
Questa query restituirà tutti i dispositivi che si trovano in Italia.
- "port:8080" - 
Questa query restituirà tutti i dispositivi che sono in ascolto sulla porta 8080, che è una porta comunemente utilizzata dalle telecamere IP.

È inoltre possibile utilizzare operatori booleani per restringere i risultati della ricerca. 
Ad esempio, la seguente query restituirà solo le telecamere IP che si trovano in Italia e sono in ascolto sulla porta 8080:

"webcam" AND "country:IT" AND "port:8080"
```
🇬🇧
```
Shodan is a search engine that allows you to find devices connected to the Internet, including webcams, routers, NAS devices, and other remote devices. It is a powerful tool that can be used for legitimate purposes, such as security vulnerability research, but it can also be used for purposes like surveillance.

To use Shodan to find online cameras, you first need to sign up for a free account. Once registered, you can access the Shodan website and start searching.

Here are some examples of queries you can use to find online cameras:

"webcam" -
This query will return all devices that have the word "webcam" in their name or metadata.
"country:IT" -
This query will return all devices located in Italy.
"port:8080" -
This query will return all devices listening on port 8080, which is a port commonly used by IP cameras.
You can also use Boolean operators to narrow your search results. For example, the following query will return only IP cameras located in Italy and listening on port 8080:

"webcam" AND "country:IT" AND "port:8080"
```

# Shodan Query Guide
## Basic Queries

| Syntax          | Example                      | Description                                  | Descrizione Italiana                                |
|------------------|------------------------------|----------------------------------------------|----------------------------------------------------|
| `ip`            | `ip:"192.168.1.1"`          | Search for a specific IPv4 address.          | Cerca un indirizzo IPv4 specifico.                 |
| `port`          | `port:80`                   | Find devices running on a specific port.     | Trova dispositivi che utilizzano una porta specifica. |
| `hostname`      | `hostname:"example.com"`   | Query devices by hostname.                   | Cerca dispositivi tramite hostname.                |
| `country`       | `country:"US"`             | Search devices located in a specific country.| Cerca dispositivi in un determinato paese.         |
| `city`          | `city:"San Francisco"`     | Search devices in a specific city.           | Cerca dispositivi in una città specifica.          |

## Intermediate Queries
| Syntax          | Example                      | Description                                  | Descrizione Italiana                                |
|------------------|------------------------------|----------------------------------------------|----------------------------------------------------|
| `org`           | `org:"Google"`             | Find devices belonging to a specific organization. | Trova dispositivi appartenenti a un'organizzazione specifica. |
| `asn`           | `asn:"AS12345"`            | Query devices by Autonomous System Number (ASN). | Cerca dispositivi tramite numero ASN.              |
| `os`            | `os:"Windows"`            | Search for devices running a specific operating system. | Cerca dispositivi con un determinato sistema operativo. |
| `before`        | `before:"2023-01-01"`      | Filter results updated before a specific date. | Filtra i risultati aggiornati prima di una certa data. |
| `after`         | `after:"2022-12-31"`       | Filter results updated after a specific date. | Filtra i risultati aggiornati dopo una certa data.  |

## Complex Queries
| Syntax          | Example                      | Description                                  | Descrizione Italiana                                |
|------------------|------------------------------|----------------------------------------------|----------------------------------------------------|
| `product`       | `product:"Apache httpd"`   | Search for specific software or products on devices. | Cerca software o prodotti specifici sui dispositivi. |
| `ssl`           | `ssl:"Let's Encrypt"`      | Find devices using a specific SSL certificate. | Trova dispositivi che utilizzano un certificato SSL specifico. |
| `http.title`    | `http.title:"Login"`       | Query devices by the title of their HTTP pages. | Cerca dispositivi in base al titolo delle loro pagine HTTP. |
| `vuln`          | `vuln:"CVE-2023-XXXX"`     | Search for devices with a specific vulnerability. | Trova dispositivi con una vulnerabilità specifica. |
| `net`           | `net:"192.168.0.0/16"`     | Filter results by a network range in CIDR format. | Filtra i risultati per intervallo di rete in formato CIDR. |

## Advanced Filters and Search Combinations
| Syntax          | Example                      | Description                                  | Descrizione Italiana                                |
|------------------|------------------------------|----------------------------------------------|----------------------------------------------------|
| `http.html`     | `http.html:"admin"`        | Search for keywords in the HTML body of HTTP pages. | Cerca parole chiave nel corpo HTML delle pagine HTTP. |
| `has_screenshot`| `has_screenshot:true`        | Filter results to show devices with screenshots. | Filtra i risultati per dispositivi con screenshot. |
| `device`        | `device:"router"`          | Find specific device types (e.g., router, webcam). | Trova tipi specifici di dispositivi (es. router, webcam). |
| `tags`          | `tags:"industrial-control"`| Filter results by tags assigned to devices. | Filtra i risultati tramite tag assegnati ai dispositivi. |
| `geo`           | `geo:37.7749,-122.4194`     | Search devices by specific geographic coordinates. | Cerca dispositivi tramite coordinate geografiche specifiche. |

## Industrial Control Systems (ICS)
| Syntax          | Example                      | Description                                  | Descrizione Italiana                                |
|------------------|------------------------------|----------------------------------------------|----------------------------------------------------|
| `ics.vendor`    | `ics.vendor:"Siemens"`     | Query ICS devices by vendor.                 | Cerca dispositivi ICS per fornitore.               |
| `ics.product`   | `ics.product:"SCADA"`      | Search for specific ICS products or software.| Cerca prodotti o software ICS specifici.          |
| `ics.version`   | `ics.version:"2.1.0"`      | Find ICS devices running a specific version. | Trova dispositivi ICS con una versione specifica.  |
| `modbus.function`| `modbus.function:"03"`    | Query devices by Modbus function codes.      | Cerca dispositivi tramite codici funzione Modbus.  |
| `bacnet.device` | `bacnet.device:"HVAC"`     | Find devices using BACnet protocols for HVAC systems. | Trova dispositivi che usano BACnet per sistemi HVAC. |

## IoT-Specific Queries
| Syntax          | Example                      | Description                                  | Descrizione Italiana                                |
|------------------|------------------------------|----------------------------------------------|----------------------------------------------------|
| `iot`           | `iot:"smart-camera"`       | Search for Internet of Things (IoT) devices by type. | Cerca dispositivi IoT per tipo.                    |
| `manufacturer`  | `manufacturer:"Philips"`   | Query IoT devices by manufacturer.           | Cerca dispositivi IoT per produttore.              |
| `firmware`      | `firmware:"1.0.2"`         | Find IoT devices by firmware version.        | Trova dispositivi IoT per versione firmware.       |
| `is_public`     | `is_public:true`            | Filter devices with public IPs.              | Filtra dispositivi con IP pubblici.                |
| `is_upnp`       | `is_upnp:true`              | Filter devices using Universal Plug and Play (UPnP). | Filtra dispositivi che utilizzano UPnP.            |

## Useful Shodan Tags
| Tag             | Description                                  | Descrizione Italiana                                |
|------------------|----------------------------------------------|----------------------------------------------------|
| `ics`           | Devices related to industrial control systems. | Dispositivi relativi a sistemi di controllo industriale. |
| `vulnerable`    | Devices with known vulnerabilities.           | Dispositivi con vulnerabilità conosciute.           |
| `webcam`        | Publicly accessible webcams.                  | Webcam accessibili pubblicamente.                 |
| `database`      | Exposed databases like MongoDB or Elasticsearch. | Database esposti come MongoDB o Elasticsearch.    |
| `honeypot`      | Devices identified as honeypots.              | Dispositivi identificati come honeypot.           |


## **Surveillance under Surveillance** - *Dove si trovano le telecamere nel mondo*

![Screenshot 2024-09-18 122411](https://github.com/user-attachments/assets/7afa9742-1fd7-4fa9-877e-58dee24f549b)
| :--- |
[**Sunders Uber Space**](https://sunders.uber.space/)


[**Camhacker**](https://www.camhacker.com/)|[**openstreetcam**](https://openstreetcam.org/map/)|[**Airport Web Cams**](https://airportwebcams.net)|
| :--- | :--- | :--- |
[**The Webcam Network**](http://www.the-webcam-network.com/)|[**Whatsup Cams**](https://www.whatsupcams.com/en/) |[**Goakamai**](http://goakamai.org/home)|
[**Thingful**](http://www.thingful.net/)|[**Honolulu.gov**](http://www2.honolulu.gov/honolulumyway/?trafficcam)|[**Gobefore**](http://gobefore.me/cams/)|
[**Worldcam**](https://worldcam.eu/)|[**Live World Web Cam**](http://liveworldwebcam.net/)|[**Ukraine-Live  Cams**](https://nagix.github.io/ukraine-livecams/)|
[**Surveillance under Surveillance**](https://sunders.uber.space)|[**Arcgis**](https://www.arcgis.com/apps/webappviewer/index.html?id=0f7aa08cc4b74fc6a0c4308d4eace6b3)|
[**Earthcam**](https://www.earthcam.com/)|[**Web Cams Abroad**](https://www.webcamsabroad.com/)|[**OpenTopia**](http://www.opentopia.com/)|[**WebCams**](https://www.webcams.travel/)|
[**Pictimo**](https://www.pictimo.com/)|[**Insecam**](http://insecam.org/)|[**the-webcam-network**](http://www.the-webcam-network.com/)|
[**windy**](https://www.windy.com/-Webcams/webcams)|[**Wrld Web Cams nsspot.net**](http://world-webcams.nsspot.net/)|[**Sky Line Web Cams**](https://www.skylinewebcams.com/en/webcm)|
[**Kroooz-cams**](https://www.kroooz-cams.com/)|[**Tfljam Cams**](https://www.tfljamcams.net/)|[**archive.tfljamcam**](https://archive.tfljamcams.net/)|
[**Fisgonia**](http://www.fisgonia.com/)|[**Calculator**](https://calculator.ipvm.com/)|[**camvista**](http://www.camvista.com/)| 
[**Grmchairresearch**](https://otc.armchairresearch.org/map)|[**Dries Depoorter**](https://driesdepoorter.be/thefollower/)|[**Mass Pirates**](https://cctv.masspirates.org/)|
[**CSE.Google.**](https://cse.google.com/cse?cx=013991603413798772546:gjcdtyiytey#gsc.tab=0)|[**Web Cam Taxi**](https://www.webcamtaxi.com/en/)|[**Watching the World**](https://webcamaze.engineering.zhaw.ch/watchingtheworld/)|

🇮🇹
```
I canali dove vengono pubblicati video possono essere utilizzati come fonti di informazioni per l'OSINT. 
Questi canali possono includere siti di condivisione video come i Social Network.
```
🇬🇧
```
Channels where videos are published can be used as sources of information for OSINT.
These channels can include video-sharing sites and social networks.
```

**Live**

![download](https://github.com/CScorza/OSINTSurveillance/assets/98583912/b0c31e97-164d-4d36-9cb9-44e90b3dda8c)

|[**Facebook Live**](https://www.facebook.com/watch/live/)|
| :--- |
|[**Localteamtv - Facebook**](https://www.facebook.com/localteamtv)|
|[**TikTok - Live**](https://www.tiktok.com/live)|
|[**YouTube - Live**](https://www.youtube.com/channel/UC4R8DWoMoI7CAwX8_LjQHig)|

**News**

![istockphoto-1205528986-612x612](https://github.com/CScorza/OSINTSurveillance/assets/98583912/2578c4b3-b74a-4272-a1cc-694db9eee583)

|[**Telegiornali - Internazionali**](https://photocall.tv/)|
| :--- |
|[**TeleVideo**](https://www.televideo.rai.it/televideo/pub/index.jsp)|
|[**ABC News**](http://abcnews.go.com/)|
|[**CNN**](http://cnn.com)|
|[**NY Times**](http://nytimes.com)|
|[**AlJazeera**](https://www.aljazeera.com/live)|
|[**BBC - Liuve**](https://www.bbc.co.uk/iplayer/live/bbcone)|


### **Video Condivis sui Social**

*Videos shared on social media*

![video-social](https://github.com/CScorza/OSINTSurveillance/assets/98583912/7fbad402-2dbc-41ca-a62f-c1ab42bf9dde)

|[**Welcome to Favelas - Telegram**](https://t.me/joinchat/x629Xz5ZNy80NWM0)|
| :--- |
[**Riotlibro - Telegram**](https://t.me/riotlibro)


# OPEN WIFI

![wifi](https://github.com/CScorza/OSINTSurveillance/assets/98583912/8bbcbac6-776a-43b2-bfe3-5535bad021e1)

🇮🇹
```
Ecco alcuni consigli su cosa non fare con le reti Wi-Fi pubbliche:
Non connetterti a reti Wi-Fi sconosciute o non protette.
Non utilizzare le reti Wi-Fi pubbliche per accedere a informazioni sensibili, come dati finanziari o dati sanitari.
Non utilizzare le reti Wi-Fi pubbliche per effettuare transazioni online, come acquisti o pagamenti.
Non utilizzare le reti Wi-Fi pubbliche per scaricare file o software. 

Suggerimento
Utilizza una VPN. 
```
🇬🇧
```
Here are some tips on what not to do with public Wi-Fi networks:

Do not connect to unknown or unsecured Wi-Fi networks.
Do not use public Wi-Fi networks to access sensitive information, such as financial or health data.
Do not use public Wi-Fi networks for online transactions, such as shopping or payments.
Do not use public Wi-Fi networks to download files or software.
Suggestion:
Use a VPN.
```

|[**WIGLE**](https://wigle.net/)|[**openwifi**](https://openwifi.su/)|[**Radio Cells**](https://radiocells.org/)|
| :--- | :--- | :--- |
|[**Mylnikov**](https://www.mylnikov.org/)|[**3wifi**](https://3wifi.stascorp.com/)|[**Open Wifi Map**](https://openwifimap.net/)
|[**Wiman**](https://www.wiman.me/)|[**wifimap**](https://www.wifimap.io/)|[**Btwifi**](https://www.btwifi.com/)|[**Open wWifi Spots**](http://openwifispots.com/)|

# OSINT IP

![360_F_633201203_N9gn1Iu5Atll2wDZD46GTQsHyGtyQ2dV](https://github.com/CScorza/OSINTSurveillance/assets/98583912/51c51604-a82c-494c-ada2-7fd977183fba)

[**Whois - domaintools**](https://whois.domaintools.com/)
| :--- | 
[**LOPSEG.com.br/OSINT**](https://www.lopseg.com.br/osint)
[**IPQualityScore**](https://www.ipqualityscore.com/)
