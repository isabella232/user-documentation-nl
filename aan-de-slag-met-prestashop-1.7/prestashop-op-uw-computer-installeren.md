# PrestaShop op uw computer installeren

Mogelijk wilt u PrestaShop op uw lokale apparaat installeren, ofwel om deze te testen voordat u geld investeert in een server en domeinnaam, ofwel om uw winkel lokaal aan te passen voordat u de wijzigingen naar de PrestaShop-installatie pusht die mogelijk al online staat.

Als u een webtoepassing lokaal installeert, moet u eerst de juiste omgeving installeren, namelijk de Apache-webserver, de PHP-taalinterpreter, de MySQL-databaseserver en idealiter ook de phpMyAdmin-tool. Dit heet ook wel een AMP: Apache+MySQL+PHP. Deze bestaat voor vele besturingssystemen. Voor elk besturingssysteem wordt een andere letter toegevoegd aan het acroniem: WAMP \(Windows+Apache+MySQL+PHP\), MAMP \(Mac OS X+...\) en LAMP \(Linux+...\).

## Een AMP-pakket kiezen <a id="PrestaShopopuwcomputerinstalleren-EenAMP-pakketkiezen"></a>

Hiervoor moet u beschikken over technische kennis. Gelukkig zijn er veel vooraf samengestelde pakketten die eenvoudig te installeren zijn. Dit wil niet zeggen dat u hier en daar toch technische handelingen moet verrichten, maar de pakketten bieden wel veel hulp. Omdat alle items uit de pakketten open-source zijn, zijn de installatieprogramma's meestal gratis te verkrijgen. Hieronder vindt u een reeks gratis AMP-installatieprogramma's:

* EasyPHP: [http://www.easyphp.org/](http://www.easyphp.org/) \(Windows\)
* MAMP: [http://www.mamp.info/](http://www.mamp.info/) \(Mac OS X\)
* WampServer: [http://www.wampserver.com/en/](http://www.wampserver.com/en/) \(Windows\)
* XAMPP: [http://www.apachefriends.org/en/xampp.html](http://www.apachefriends.org/en/xampp.html) \(Windows, Mac OS X, Linux, Solaris\)

Kies het pakket dat u het fijnst vindt en open het.

## Controleren of alles werkt <a id="PrestaShopopuwcomputerinstalleren-Controlerenofalleswerkt"></a>

Voordat u doorgaat met deze installatiezelfstudie van PrestaShop controleert u of alle onderdelen van uw AMP-pakket werken:

* **De webserver moet actief zijn**. U zou deze moeten kunnen openen via uw browser door 127.0.0.1 in te voeren in de adresbalk.

[http://127.0.0.1](http://127.0.0.1/) is de localhost \(uw computer\): dit is een loopbackadres dat de browser doorverwijst naar uw lokale webserver.  
[http://127.0.0.1](http://127.0.0.1/) en [http://localhost](http://localhost/) zijn daarom dus hetzelfde: u kunt ze beide gebruiken om naar de hoofdmap van uw lokale webserver te gaan.

Sommige webservers kunnen mogelijk niet starten omdat de verbindingspoorten \(meestal poort 80\) al worden gebruikt door andere toepassingen.

Dit gebeurt vaak wanneer Skype wordt gebruikt. Als u ervoor wilt zorgen dat Skype niet voorkomt dat de lokale webserver wordt uitgevoerd, gaat u naar de geavanceerde instellingen van Skype \(Tools &gt; Opties &gt; Geavanceerd &gt; Verbindingen\) en schakelt u het selectievakje bij Poort 80 en 443 als alternatieven gebruiken uit. Start Skype opnieuw op en start uw lokale webserver opnieuw op.

* **De databaseserver moet actief zijn**. In MySQL worden alle PrestaShop-gegevens opgeslagen. Het AMP-pakket moet u een duidelijke indicatie bieden van of MySQL wel of niet actief is.
* **De phpMyAdmin-tool moet toegankelijk zijn**. Dit is de webtoepassing waarmee u de gegevens kunt verwerken die zijn opgeslagen in MySQL. De locatie hangt af van welk AMP-pakket u hebt gekozen: u vindt deze op [http://127.0.0.1/phpmyadmin](http://127.0.0.1/phpmyadmin) \(XAMPP, WampServer, MAMP\) of [http://127.0.0.1/mysql](http://127.0.0.1/mysql) \(EasyPHP\), of mogelijk zelfs op een andere locatie. Lees de documentatie bij het pakket. Mogelijk staat hierin een phpMyAdmin-knop waarmee de juiste URL wordt geopend in uw browser.

## De hoofdmap van de lokale webserver zoeken <a id="PrestaShopopuwcomputerinstalleren-Dehoofdmapvandelokalewebserverzoeken"></a>

Wanneer u hebt gecontroleerd of het pakket correct is geïnstalleerd en of alle onderdelen actief zijn, moet u de hoofdmap van uw lokale webserver zoeken.

Dat is de lokale map waarin u alle toepassingsbestanden plaatst. Deze map is vergelijkbaar met de hoofdmap van uw onlineserver. De inhoud kan worden geopend via [http://127.0.0.1](http://127.0.0.1/).

De daadwerkelijke lokale locatie van de map is in grote mate afhankelijk van het AMP-pakket en kan worden gewijzigd:

* EasyPHP: `C:\easyphp\www`
* MAMP: `/Applications/MAMP/htdocs/`
* WampServer: `C:\wamp\www`
* XAMPP: `C:\xampp\htdocs` of `/Applications/xampp/htdocs`

## De MySQL-gebruikersinformatie zoeken <a id="PrestaShopopuwcomputerinstalleren-DeMySQL-gebruikersinformatiezoeken"></a>

Tot slot moet u beschikken over de hoofdgebruikersnaam en het hoofdwachtwoord voor MySQL om PrestaShop te kunnen installeren.

**In de meeste pakketten wordt de gebruikersnaam ‘root’ gebruikt met een leeg wachtwoord**, zoals bij EasyPHP, MAMP, WampServer en XAMPP.

Lees de documentatie bij uw pakket.

## Laatste opmerking vóór de installatiezelfstudie <a id="PrestaShopopuwcomputerinstalleren-Laatsteopmerkingv&#xF3;&#xF3;rdeinstallatiezelfstudie"></a>

Nu alles duidelijk is, kunt u de rest van deze gids doornemen en beginnen met het installeren van PrestaShop.

Wanneer u PrestaShop lokaal installeert, denkt u aan het volgende:

* Bestanden mogen niet worden geüpload via FTP-software \(zoals FileZilla\) naar een webserver: verplaats ze naar de juiste lokale map, zoals hierboven wordt aangegeven.
* Je hoeft geen lokale domeinnaam te maken: PrestaShop is beschikbaar via het loopbackadres dat hierboven is opgegeven. Dat is [http://localhost](http://localhost/) of [http://127.0.0.1](http://127.0.0.1/). PrestaShop zelf is beschikbaar via dit adres door de mapnaam toe te voegen: bijvoorbeeld [http://localhost/prestashop](http://localhost/prestashop) of [http://127.0.0.1/prestashop](http://127.0.0.1/prestashop) als PrestaShop zich in de submap `/prestashop/` bevindt van de lokale hoofdmap. Wanneer u dit adres voor het eerst opent, wordt u automatisch doorgestuurd naar de PrestaShop-installatie, ofwel via [http://localhost/prestashop/install](http://localhost/prestashop/install) ofwel via [http://127.0.0.1/prestashop/install](http://127.0.0.1/prestashop/install).

  
Hebt u alles gelezen? Volg nu de reguliere installatiegids. Begin bij het gedeelte Een database maken voor uw winkel: [PrestaShop installeren](prestashop-op-uw-computer-installeren.md).

