# Stångloggen

En träningslogg för styrketräning med skivstång enligt Starting Strength-upplägget (pass A/B, 3×5, marklyft 1×5).
Appen räknar ut nästa pass, uppvärmningsset och vilka viktskivor som ska på stången. Den fungerar utan nät.

## Installera på telefonen (gratis, cirka 10 minuter)

Appen behöver ligga på en webbadress en gång, sedan installeras den på telefonen. Enklast är GitHub Pages.
Gör stegen på en dator, det är lättast så.

1. Skapa ett **privat** konto på <https://github.com/signup> (använd inte jobbkontot).
2. Klicka på **+** uppe till höger och välj **New repository**.
   - Namn: `stangloggen`
   - Välj **Public** (koden blir synlig, men den innehåller inga uppgifter om dig. Dina pass sparas bara i telefonen.)
   - Klicka på **Create repository**.
3. Klicka på länken **uploading an existing file**. Dra in alla filer från zip-filen:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`.
   Klicka på **Commit changes**.
4. Gå till **Settings → Pages**. Under *Build and deployment* väljer du **Deploy from a branch**, branch **main** och mapp **/ (root)**. Klicka på **Save**.
5. Vänta en till två minuter. Adressen blir `https://DITT-ANVÄNDARNAMN.github.io/stangloggen/`.
6. Öppna adressen i **Chrome** på telefonen. Tryck på menyn **⋮** och välj **Installera app** (ibland heter det **Lägg till på startskärmen**).

Nu ligger Stångloggen bland dina appar och startar utan adressfält.

## Backup till Google Drive

- Efter varje pass får du frågan om du vill spara en backup. Tryck på **Spara backup till Drive** och välj **Spara på Drive** i menyn som öppnas.
- Du kan också göra det under **Inställningar → Backup till Google Drive**.
- På startsidan ser du om det finns pass som inte har backup.
- **Exportera till kalkylark (CSV)** ger en fil som går att öppna i Google Kalkylark eller Excel.

## Byta telefon

1. Installera appen på den nya telefonen enligt steg 6 ovan.
2. Välj **Återställ från backup** på startskärmen, eller under Inställningar.
3. Välj den senaste backupfilen från Google Drive (`stangloggen-backup-ÅÅÅÅ-MM-DD.txt`).

## Så räknar appen

- Pass A: knäböj 3×5, stående press 3×5, marklyft 1×5.
- Pass B: knäböj 3×5, bänkpress 3×5, marklyft 1×5.
- Klarar du alla reps höjs vikten nästa gång: +2,5 kg för knäböj, press och bänk, +5 kg för marklyft. Det går att ändra.
- Missar du en rep blir det samma vikt nästa gång. Efter tre missade pass i rad på samma vikt sänks vikten med 10 %.
- Ändrar du vikten under passet räknas nästa pass från vikten du faktiskt körde.
- Uppvärmning: tom stång 2×5, sedan ett till tre set med stigande vikt och färre reps.

## Uppdatera appen

Ladda upp den nya `index.html` (och övriga ändrade filer) till samma repository.
Telefonen hämtar uppdateringen i bakgrunden och visar den nästa gång appen startas.
