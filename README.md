# FICSIT Live

Een live dashboard, een fabriekskaart en een productieplanner voor **Satisfactory 1.2**. Alles komt rechtstreeks uit je draaiende game en verschijnt in je browser en als overlay over de game.

## Wat je nodig hebt

1. **Satisfactory 1.2** op Windows.
2. **De mod FicsIt Remote Monitoring**, te installeren via de [Satisfactory Mod Manager](https://smm.ficsit.app/). Zet in de modinstellingen **Web Autostart** aan, zodat de webserver met de game meestart. Je kunt hem ook zelf starten door in de chat `/frm http start` te typen. Hij luistert op poort 8080.

## Installeren

1. **Download [FICSIT-Live-Setup.exe](https://github.com/Eyonator/FicsitLive/releases/latest/download/FICSIT-Live-Setup.exe)** (ongeveer 100 MB).
   - Vraagt je browser of je het bestand wilt behouden, kies dan **Behouden**. In Edge zit dat onder de drie puntjes naast de download: **Behouden → Meer weergeven → Toch behouden**.
2. **Dubbelklik op het bestand.**
   - Windows toont de eerste keer een blauw venster, *"Windows heeft uw pc beschermd"*. Klik op **Meer info** en dan op **Toch uitvoeren**. Dat komt doordat het programma geen betaald certificaat heeft; het gebeurt alleen bij deze eerste installatie.
3. **Klaar.** FICSIT Live installeert zich zonder verdere vragen, en daarna opent het dashboard in je browser.

Je hebt geen beheerdersrechten nodig. Er staat een snelkoppeling op je bureaublad en in het Startmenu.

## Het dashboard: http://localhost:8420

FICSIT Live is een pagina in je eigen browser, op **<http://localhost:8420/>**. Dat adres werkt alleen op de pc waar FICSIT Live draait. Het is geen website op internet.

Je opent het dashboard op drie manieren:
- dubbelklik op **FICSIT Live** op je bureaublad of in het Startmenu;
- klik met rechts op het icoon in het systeemvak (rechtsonder, bij de klok) en kies **Dashboard openen**;
- typ `localhost:8420` in de adresbalk van je browser. Zet het gerust bij je favorieten.

Hier staan de energie, de machines, de kaart van je fabriek en de planner.

## De overlay in de game

- **FICSIT Live start vanzelf als je inlogt** en wacht stil in het systeemvak.
- **Start je Satisfactory**, dan verschijnt de overlay vanzelf over de game. Dat werkt in *Volledig scherm* en in *Randloos venster*.
- Met **F9** toon en verberg je hem, en met **Shift+F9** klik je erdoorheen naar de game.
- Met de knop **In browser openen** bovenin de overlay open je hetzelfde dashboard groot in je browser.

## Bijwerken

FICSIT Live kijkt elk half uur of er een nieuwe versie is en haalt die op de achtergrond binnen.

- Staat er een klaar, dan zie je bovenin het dashboard en in de overlay een knop **Update**. Een klik vertelt wat er verandert en hoe het bijwerken gaat.
- Pas als jij op **Nu bijwerken** klikt, wordt hij geïnstalleerd. Dat kan ook via het icoon in het systeemvak.
- De game mag gewoon blijven draaien. FICSIT Live is ongeveer een halve minuut weg, start daarna vanzelf opnieuw, en de pagina laadt zichzelf opnieuw.
- Je projecten en instellingen blijven staan. Bij updates komt er geen waarschuwing van Windows.

## Instellingen

Je instellingen staan in `%APPDATA%\FICSIT Live`. Die map open je door dat pad in de adresbalk van Verkenner te plakken.

- **De overlay** (sneltoetsen, breedte, kant, taal) stel je in in `overlay.config.json`. `"width": 0.95` betekent 95% van de schermbreedte. Wijzigingen werken meteen.
- **Het dashboard op een tablet:** zet in `settings.json` de waarde `bridgeHost` op `"0.0.0.0"` en herstart FICSIT Live (systeemvak → **Afsluiten**, daarna de snelkoppeling). Windows vraagt dan één keer of het de firewall mag openen. Op de tablet ga je naar `http://<ip-van-je-pc>:8420/`.
- **Niet automatisch bijwerken:** zet `checkForUpdates` op `false`. **Niet starten bij inloggen:** zet `openAtLogin` op `false`.

## Verwijderen

Via **Windows-instellingen → Apps → Geïnstalleerde apps → FICSIT Live → Verwijderen**. Je projecten blijven in `%APPDATA%\FICSIT Live` staan, tot je die map zelf weggooit.

## Werkt er iets niet?

Kijk in `%APPDATA%\FICSIT Live`:
- `app.log` zegt wat de app doet;
- `bridge.log` zegt wat de verbinding met de game doet;
- `updater.log` zegt wat de updates doen.

Stuur die drie bestanden mee met je vraag of opmerking.

## Wat hier staat

In de releases staan het setup-bestand en de wijzigingen per versie. De broncode staat niet in deze repository.
