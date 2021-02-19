# Overige informatie

## Houd een testversie bij de hand! <a id="Overigeinformatie-Houdeentestversiebijdehand!"></a>

Wanneer u klaar bent met het instellen van uw winkel op basis van uw wensen, maar voordat u deze officieel openstelt voor het publiek, raden we u **ten zeerste** aan om een lokale testversie te installeren op uw eigen computer \(met [WAMP](http://en.wikipedia.org/wiki/Comparison_of_WAMPs) voor Windows, [MAMP](http://en.wikipedia.org/wiki/MAMP) voor Mac, [LAMP](http://en.wikipedia.org/wiki/LAMP_%28software_bundle) voor Linux of [XAMPP](http://www.apachefriends.org/en/xampp.html) voor een willekeurig platform\) of op een andere locatie op uw hostingserver.

Het tweede exemplaar is handig om te gebruiken als pre-productieomgeving; hierin kunt u alle toekomstige wijzigingen doorvoeren aan uw PrestaShop-webwinkel zonder dat de liveversie hierdoor wordt beïnvloed. Als er dan een fout optreedt, is dit niet het geval voor uw livewinkel.

Wanneer u hebt gecontroleerd of de testversie goed werkt, overschrijft u de liveversie met de testversie. Dit kunt u het beste doen buiten de drukste tijdstippen en terwijl uw winkel correct en tijdelijk is uitgeschakeld via de PrestaShop-backoffice.

## Op zoek naar de GD-bibliotheek <a id="Overigeinformatie-OpzoeknaardeGD-bibliotheek"></a>

Dankzij de [GD-bibliotheek](http://www.boutell.com/gd/) kan PrestaShop afbeeldingen bewerken die u uploadt. Het belangrijkste hierbij is het wijzigen van het formaat van afbeeldingen.

Bij een standaardinstallatie van PHP moet de GD-bibliotheek zijn ingeschakeld, maar als dat niet het geval is voor uw installatie, zijn de standaardinstructies voor Windows:

1. In de hoofdmap van uw PHP-map opent u het bestand `php.ini`.
2. Verwijder de opmerking van de regel `extension=php_gd2.dll` \(ongeveer halverwege in het bestand, in het midden van een lange lijst extensies\) door de puntkomma aan het begin van de regel te verwijderen.
3. Start de PHP-services opnieuw op.

Als u geen toegang hebt tot het bestand `php.ini` \(wat vaak het geval is bij gedeelde hosting\), neemt u met uw host contact op over uw hostingbehoeften.

## PHP5 activeren <a id="Overigeinformatie-PHP5activeren"></a>

Vaak is bij eigen of gedeelde servers zoal PHP 4 als PHP 5 beschikbaar, maar alleen PHP4 wordt standaard geactiveerd.

Voor het installeren van PrestaShop moet PHP 5 worden geactiveerd. Als u PrestaShop probeert uit te voeren met PHP 4, ontvangt u meerdere foutmeldingen, waaronder dit bekende bericht:

```text
Parse error: parse error, unexpected T_STATIC, expecting T_OLD_FUNCTION or T_FUNCTION or T_VAR or '}' in [php file] on line X.
```

U kunt altijd een foutrapport plaatsen met tips voor het uitvoeren van PrestaShop via uw hostingservice. Dit kan via [Forge](http://forge.prestashop.com/) van PrestaShop \(hier hebt u een account voor nodig\). De tips worden na ontvangst ook toegevoegd aan deze gids.

Hier volgt een lijst met de procedures waar we momenteel van op de hoogte zijn...

### 1&1 IONOS <a id="Overigeinformatie-1&amp;1IONOS"></a>

Voeg deze regel toe aan het bestand `.htaccess`:

```text
AddType x-mapp-php5 .php
```

Voor het herschrijven van de URL's voegt u deze regels toe:

```text
Options +FollowSymLinks
RewriteEngine On
```

### [Free.fr](http://free.fr/) <a id="Overigeinformatie-Free.fr"></a>

Voeg deze regel toe aan het bestand `.htaccess`:

```text
php 1
```

### OVH <a id="Overigeinformatie-OVH"></a>

Voeg deze regel toe aan het bestand `.htaccess`:

```text
SetEnv PHP_VER 5
```

Algemene registers deactiveren:

```text
SetEnv REGISTER_GLOBALS 0
```

### GoDaddy <a id="Overigeinformatie-GoDaddy"></a>

Uw PHP-versie bekijken:

1. Meld u aan bij Account Manager.
2. In het gedeelte Producten klikt u op Webhosting.
3. Naast het hostingaccount dat u wilt gebruiken klikt u op Starten.

In het gedeelte Server wordt de PHP-versie weergegeven.

Uw PHP-versie wijzigen:

1. In het menu Inhoud selecteert u Programmeertalen.
2. Selecteer de PHP-versie die u wilt gebruiken en klik op Doorgaan.
3. Klik op Bijwerken.

Het kan tot 24 uur duren voor de wijzigingen zijn doorgevoerd.

### Gedeelde hosting van Lunarpages <a id="Overigeinformatie-GedeeldehostingvanLunarpages"></a>

1. Open cPanel. Deze vindt u hier: **Erreur ! La référence de lien hypertexte est incorrecte.**
2. Voer in het vak dat wordt weergegeven de gebruikersnaam en het wachtwoord in van het account.
3. Er wordt een nieuwe pagina weergegeven. Ga naar de onderste rij pictogrammen op de pagina en klik op het pictogram met de naam PHP 5 inschakelen/uitschakelen.
4. Er wordt een nieuwe pagina weergegeven. Klik op PHP 5 toevoegen aan uw account!

Uw verzoek voor het wijzigen van de taal wordt ingediend. Het kan tot 24 uur duren tot de verandering is verwerkt door de hostingserver.

