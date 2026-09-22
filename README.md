# FICSIT Live

Een live dashboard, een fabriekskaart en een productieplanner voor **Satisfactory 1.2**. Alles komt rechtstreeks uit je draaiende game en verschijnt in je browser en als overlay over de game.

## Wat je nodig hebt

1. **Satisfactory 1.2** op Windows.
2. **De mod FicsIt Remote Monitoring**, te installeren via de [Satisfactory Mod Manager](https://smm.ficsit.app/). Zet in de modinstellingen **Web Autostart** aan, zodat de webserver met de game meestart. Je kunt hem ook zelf starten door in de chat `/frm http start` te typen. Hij luistert op poort 8080.
3. **Borderless Fullscreen** (Randloos volledig scherm) als weergavemodus, anders kan de overlay niet over de game heen.

## Installeren

1. **Download [FICSIT-Live-Setup.exe](https://github.com/Eyonator/FicsitLive/releases/latest/download/FICSIT-Live-Setup.exe)** (ongeveer 100 MB).
   - Vraagt je browser of je het bestand wilt behouden, kies dan **Behouden**. In Edge zit dat onder de drie puntjes naast de download: **Behouden → Meer weergeven → Toch behouden**.
2. **Dubbelklik op het bestand.**
   - Windows toont de eerste keer een blauw venster, *"Windows heeft uw pc beschermd"*. Klik op **Meer info** en dan op **Toch uitvoeren**. Dat komt doordat het programma geen betaald certificaat heeft; het gebeurt alleen bij deze eerste installatie.
3. **Klaar.** FICSIT Live installeert zich zonder verdere vragen, en daarna opent het dashboard in je browser.

Je hebt geen beheerdersrechten nodig. Er staat een snelkoppeling op je bureaublad en in het Startmenu.

## Gebruiken

- **FICSIT Live start vanzelf als je inlogt** en wacht stil in het systeemvak (rechtsonder, bij de klok).
- **Start je Satisfactory**, dan verschijnt de overlay vanzelf. Met **F9** toon en verberg je hem, en met **Shift+F9** klik je erdoorheen naar de game.
- **Het dashboard** open je met de snelkoppeling op je bureaublad, of via het icoon in het systeemvak → **Dashboard openen**. Het adres is <http://localhost:8420/>.

## Bijwerken

Dat gaat vanzelf. FICSIT Live haalt een nieuwe versie op de achtergrond binnen en installeert die pas als de game dicht is, dus nooit tijdens het spelen. Zolang er een versie klaarstaat, zie je dat in het menu van het systeemvak-icoon. Je projecten en instellingen blijven staan. Bij updates komt er geen waarschuwing van Windows.

## Instellingen

Je instellingen staan in `%APPDATA%\FICSIT Live`. Die map open je door dat pad in de adresbalk van Verkenner te plakken.

- **De overlay** (sneltoetsen, grootte, kant, taal) stel je in in `overlay.config.json`. Wijzigingen werken meteen.
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
