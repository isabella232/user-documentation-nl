# Wat u nodig hebt om aan de slag te gaan

* [Wat u nodig hebt om aan de slag te gaan](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Watunodighebtomaandeslagtegaan)
  * [Verkorte installatie-instructies](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Verkorteinstallatie-instructies)
  * [Gedetailleerde installatie-instructies](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Gedetailleerdeinstallatie-instructies)
    * [Een domeinnaam registreren](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Eendomeinnaamregistreren)
    * [Een host vinden](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Eenhostvinden)
    * [Technische vereisten](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Technischevereisten)
    * [Tools](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Tools)
    * [Een plan opstellen](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-Eenplanopstellen)
    * [PrestaShop installeren](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md#Watunodighebtomaandeslagtegaan-PrestaShopinstalleren)

## Wat u nodig hebt om aan de slag te gaan <a id="Watunodighebtomaandeslagtegaan-Watunodighebtomaandeslagtegaan"></a>

### Verkorte installatie-instructies <a id="Watunodighebtomaandeslagtegaan-Verkorteinstallatie-instructies"></a>

Hier volgt een lijst met de zaken die u nodig hebt om aan de slag te gaan met het installeren van PrestaShop 1.7. Als u het idee hebt dat de informatie te algemeen is, kunt u in de hierop volgende hoofdstukken meer gedetailleerde informatie vinden.

* Systeemvereisten:
  * PHP 5.4 of nieuwer.
    * Handige instellingen \(in het bestand `php.ini`\): 
      * `allow_url_fopen` ingesteld op On \(Aan\), 
      * `register_globals` ingesteld op Off \(Uit\)`,`
      * `upload_max_filesize` ingesteld op 16M \(of meer\).
    * Vereiste PHP-extensies \(in het bestand `php.ini`\): PDO\_MySQL, cURL, SimpleXML, mcrypt, GD, OpenSSL, DOM, SOAP, Zip, fileinfo.
    * Handige servertools: cron/crontab, Memcached.
  * MySQL 5.0 of nieuwer.
  * Beter met: 
    * Unix-/Linux-hosting.
    * Apache Web Server 2.0 of nieuwer, of nginx Web Server.
      * Apache-module-instellingen: 
        * `mod_rewrite` ingeschakeld, 
        * `mod_security` uitgeschakeld,
        * `mod_auth_basic` uitgeschakeld.
    * Ten minste 128 MB aan RAM-geheugen voor PHP. Hoe meer, hoe beter.
* Toegangscodes voor uw FTP-server en uw MySQL-database
  * Deze moeten worden aangeleverd door uw webhost als u geen lokale installatie uitvoert.
* Een tekstverwerkingsprogramma.
* Een FTP-client.
* Een moderne webbrowser \(als u Internet Explorer gebruikt, dan ten minste versie IE9\).

U moet ook weten via welke URL op uw domein u uw winkel\(s\) wilt kunnen openen.

Bekijk de pagina met officiële systeemvereisten: [http://www.prestashop.com/nl/system-requirements](http://www.prestashop.com/en/system-requirements).

Wanneer u alles hebt voorbereid, gebruikt u de [installatiehandleiding](prestashop-installeren.md).

### Gedetailleerde installatie-instructies <a id="Watunodighebtomaandeslagtegaan-Gedetailleerdeinstallatie-instructies"></a>

PrestaShop is een webtoepassing: deze moet worden geïnstalleerd op een webserver om te kunnen worden uitgevoerd en er is een domeinnaam nodig die uw bezoekers gebruiken om uw winkel te bezoeken.

#### Een domeinnaam registreren <a id="Watunodighebtomaandeslagtegaan-Eendomeinnaamregistreren"></a>

Voordat u iets downloadt of installeert, moet u een startpagina opgeven voor uw PrestaShop-webwinkel. Deze startpagina bestaat uit twee zaken: een domeinnaam en een webserver. Een domeinnaam is een online-id voor uw website, zoals [example.com](http://example.com/) of [myonlineshop.net](http://myonlineshop.net/). Dit is het visitekaartje van uw webserver en daarmee ook van uw winkel.

U moet een domeinnaam kopen voor uw winkel. Mogelijk krijgt u er een wanneer u ergens webhostingservices koopt: veel webhosts bieden een gratis domeinnaam bij elk nieuwe account. Het kan zijn dat u de domeinnaam een jaar gratis kunt gebruiken of zelfs zo lang zal als u de webhostingservices gebruikt. Op die manier is het eenvoudig om álles \(hosting + domeinnaam\) in één keer te verkrijgen.

Er kan een probleem optreden met door een host aangeboden domeinnamen: als u niet tevreden bent met de services van de host, kan het zijn dat u van host wilt wisselen. Dat betekent dat u uw bestanden, gegevens en domeinnaam naar een andere host moet verplaatsen.

De bestanden en gegevens zijn eenvoudig te verplaatsen, maar het kan lastig zijn om uw domeinnaam ook mee te nemen. Omdat de host de domeinnaam voor u heeft gekocht, is het domein technisch gezien eigendom van de host. De host kan u verbieden om de domeinnaam mee te nemen naar een andere host, of de host kan u ervoor laten betalen. Omdat de domeinnaam uw merk en visitekaartje is op internet, moet u de regels van de webhost opvolgen.

Daarom wordt het vaak aanbevolen om uw domeinnaam aan te schaffen bij een onafhankelijke domeinnaamregistrar \(zie: [http://en.wikipedia.org/wiki/Domain\_name\_registrar](http://en.wikipedia.org/wiki/Domain_name_registrar)\). Technisch gezien kunt u domeinnamen nooit kopen, maar alleen huren. Dit gaat meestal gepaard met een jaarlijks te betalen bedrag. Dit biedt u het recht om de domeinnaam te gebruiken, maar zodra u stopt met betalen, is de domeinnaam niet meer van u en kunnen anderen er gebruik van maken.

Naast het betalen voor de domeinnaamregistratie moet u ook betalen voor webhosting. U kunt dan wel te allen tijde overstappen naar een betere host, zonder aanvullende kosten: u hoeft alleen de DNS-adressen van de domeinnaam te wijzigen. De wijziging wordt binnen 24 uur wereldwijd doorgevoerd.

  
Als u liever een domeinnaam koopt bij een onafhankelijke registrar, vindt u hier enkele betrouwbare partijen:

* Gandi: [http://en.gandi.net/](http://en.gandi.net/)
* Namecheap: [http://www.namecheap.com/](http://www.namecheap.com/)
* GoDaddy: [https://www.godaddy.com/](https://www.godaddy.com/)
* 1&1 IONOS: [https://www.ionos.com](https://www.ionos.com/)

Er zijn er echter nog veel meer. Vraag uw vrienden ook naar tips!

#### Een host vinden <a id="Watunodighebtomaandeslagtegaan-Eenhostvinden"></a>

Nu u een domeinnaam hebt, moet u deze koppelen aan PrestaShop. Dit betekent dat de PrestaShop-bestanden zich moeten bevinden op een webserver. Mogelijk hebt u een eigen webserver, maar de kans is groter dat u uw winkel host bij of gaat hosten bij een internethostingservice \(zie: [http://en.wikipedia.org/wiki/Internet\_hosting\_service](http://en.wikipedia.org/wiki/Internet_hosting_service)\); deze biedt u een locatie online voor een maandelijks of jaarlijks te betalen bedrag.

Voordat u aan de slag gaat met een webwinkel, moet u een hostingprovider kiezen. Vrijwel elke webhost kan effectief omgaan met de PrestaShop-oplossing. Slechts enkele hostingproviders bieden echter geoptimaliseerde servers voor PrestaShop \(met eenvoudige installatie en een up-to-date versie\). U vindt onze lijst met hostingpartners [hier](https://www.prestashop.com/en/ecommerce-hosting).

Bij het kiezen van een host moet u rekening houden met één belangrijke vereiste: er moet ondersteuning worden geboden voor PHP 5.4 \(of nieuwer\); dit is de programmeertaal waarin PrestaShop is geschreven, en voor MySQL 5 \(of nieuwer\), het databasesysteem waarin PrestaShop alle gegevens opslaat. Er zijn nog meer vereisten. Zie daarvoor het gedeelte Technische vereisten hieronder.

#### Technische vereisten <a id="Watunodighebtomaandeslagtegaan-Technischevereisten"></a>

PrestaShop is een toepassing die wordt uitgevoerd op een webserver en is geschreven op basis van de PHP-programmeertaal. De gegevens worden in een MySQL-server opgeslagen.

PHP is een open-source programmeertaal die voornamelijk wordt gebruikt voor webtoepassingen. De taal is bedacht in 1995 en is nu de taal die het meest wordt gebruikt door webontwikkelaars. Voor de taal wordt een C-achtige syntaxis gebruikt waardoor ontwikkelaars de taal eenvoudig kunnen leren.

MySQL is een open-source databasemanagementsysteem. Dit systeem is ook in 1995 ontwikkeld en het is tegenwoordig het meest gebruikte databasesysteem van webontwikkelaars. Het systeem is gebaseerd op de SQL-taal, de meest bekende databasetaal.

Voor welke hostingservice u ook kiest, de volgend onderdelen worden op uw webserver geïnstalleerd:

* **Systeem**: Unix, Linux of Windows. Unix wordt ten zeerste aanbevolen.
* **Webserver**: Apache Web Server 2.0 of nieuwer.
* **PHP 5.4 of nieuwer**. Mogelijk moet u PHP 5 activeren \(doe hiervoor navraag bij uw hostingprovider\).
* **MySQL 5.0 of nieuwer**.
* Ten minste 128 MB aan RAM-geheugen op uw server.

PrestaShop kan ook werken met de IIS-webserver 6.0 of nieuwer van Microsoft en nginx 1.0 of nieuwer.

Er is in de [Handleiding voor systeembeheerders](wat-u-nodig-hebt-om-aan-de-slag-te-gaan.md) meer informatie beschikbaar voor systeembeheerders. Lees deze!

#### Tools <a id="Watunodighebtomaandeslagtegaan-Tools"></a>

U hebt twee tools nodig: een tekstverwerkingsprogramma om tekstbestanden te bewerken en een FTP-client om bestanden van uw apparaat te verplaatsen naar uw server en andersom.

**Tekstverwerkingsprogramma**

Dit zijn enkele bekende tekstverwerkingsprogramma's:

* Windows en OS X:
  * Sublime Text: [http://www.sublimetext.com/](http://www.sublimetext.com/)
  * Atom: [https://atom.io/](https://atom.io/)
* Unix/Linux:
  * Vim: [http://www.vim.org/](http://www.vim.org/)
  * Emacs: [http://www.gnu.org/software/emacs/](http://www.gnu.org/software/emacs/)  

Gebruik GEEN regulier tekstverwerkingsprogramma voor het bewerken van tekstbestanden, zoals Microsoft Word of Write van [OpenOffice.org](http://openoffice.org/).

FTP-client

FTP staat voor File Transfer Protocol: de standaardmanier voor het overbrengen van bestanden van een computer naar een webhost.

In deze gids wordt FileZilla gebruikt: een uitstekende en gratis FTP-client voor Windows, Mac OS X en Linux. Het programma is te downloaden via [http://filezilla-project.org/](http://filezilla-project.org/). Start vervolgens het installatieprogramma. Download niet de FileZilla-server, maar alleen de FileZilla-client!

Wanneer FileZilla is geïnstalleerd, moet u deze configureren met de verbindingsparameters van uw webserver. Deze moeten door uw host naar u zijn verzonden. Als de host dat niet heeft gedaan, vraagt u ernaar bij de host of kijkt u in de map Spam.

De benodigde parameters zijn:

* **een hostnaam** of **een IP-adres**: de locatie van de FTP-server van uw hostingruimte.
* **een gebruikersnaam**: uw hostingaccount-id, die uniek is voor u.
* **een wachtwoord**: een verplichte beveiligingsmaatregel.

Open FileZilla en open de Site Manager-tool. U kunt dit op drie verschillende manieren doen:

* Druk op CTRL + S.
* Klik op het pictogram Site Manager openen in de linkerbovenhoek,
* Open het menu Bestand en selecteer de optie Site Manager...

Er wordt een venster geopend.

Uw hostingruimte toevoegen aan Site Manager:

1. Klik op de knop Nieuwe site. Er wordt een nieuwe vermelding aangemaakt in de sitelijst. Geef deze een herkenbare naam.
2. Aan de rechterkant, op het tabblad Algemeen, voert u de parameters in die uw host heeft opgegeven: host, gebruikersnaam en wachtwoord. U hoeft de overige standaardparameters niet te wijzigen, tenzij dit door de host wordt aangegeven.
3. Wanneer alle velden juist zijn ingevuld, klikt u op de knop Verbinden. Hiermee slaat u uw site op in de lijst en meldt u zich aan bij uw account. U kunt dan controleren of alles goed werkt.

Als FileZilla u niet bevalt, kunt u een van de andere bekende FTP-clients gebruiken:

* Windows:
  * CoreFTP: [http://www.coreftp.com/](http://www.coreftp.com/)
  * WinSCP: [http://winscp.net/](http://winscp.net/)
  * SmartFTP: [http://www.smartftp.com/](http://www.smartftp.com/)
* Mac OS X:
  * Cyberduck: [http://cyberduck.ch/](http://cyberduck.ch/)
  * Transmit: [http://www.panic.com/transmit/](http://www.panic.com/transmit/)
  * Fetch: [http://fetchsoftworks.com/fetch/](http://fetchsoftworks.com/fetch/)
* Unix/Linux:
  * gFTP: [http://gftp.seul.org/](http://gftp.seul.org/)
  * kasablanca: [http://kasablanca.berlios.de/](http://kasablanca.berlios.de/)
  * NcFTP: [http://www.ncftp.com/ncftp/](http://www.ncftp.com/ncftp/)

#### Een plan opstellen <a id="Watunodighebtomaandeslagtegaan-Eenplanopstellen"></a>

U moet direct beslissen waar u PrestaShop wilt hosten. Er zijn vier mogelijkheden ten aanzien van uw domeinnaam:

* In de hoofdmap van het domein: [http://www.voorbeeld.com/](http://www.example.com/)
* In een map: [http://www.voorbeeld.com/shop/](http://www.example.com/shop/)
* In een subdomein: [http://store.voorbeeld.com/](http://store.example.com/)
* In een map van een subdomein: [http://kleding.voorbeeld.com/boutique/](http://clothes.example.com/boutique/)

Dankzij de functie voor meerdere winkels kunt u zo veel winkels als nodig is opstarten met één installatie van PrestaShop 1.7. Indien nodig kunt u voor elke winkel een eigen domeinnaam gebruiken. Houd hier rekening mee tijdens het besluiten waar u wat gaat opslaan.  
 Wat u ook van plan bent: de standaardopslagplaats bevindt zich altijd op dezelfde locatie als PrestaShop.

#### PrestaShop installeren <a id="Watunodighebtomaandeslagtegaan-PrestaShopinstalleren"></a>

Nu u aan alle vereisten voldoet, kunt u de [installatiehandleiding gebruiken](prestashop-installeren.md).

