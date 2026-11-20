# Stångloggen

En träningslogg för styrketräning med skivstång enligt Starting Strength-upplägget (pass A/B, 3×5, marklyft 1×5).
Appen räknar ut nästa pass, uppvärmningsset och vilka viktskivor som ska på stången. Den fungerar utan nät.

**Adress:** <https://mrlundvik.github.io/stangloggen/>

## Installera på telefonen

1. Öppna adressen ovan i **Chrome** på telefonen.
2. Tryck på menyn **⋮** och välj **Installera app** (ibland heter det **Lägg till på startskärmen**).

Nu ligger Stångloggen bland dina appar och startar utan adressfält. Efter första starten fungerar den utan nät.
Dina pass sparas bara i telefonen, inte på webbplatsen.

## Backup till Google Drive

- Efter varje pass får du frågan om du vill spara en backup. Tryck på **Spara backup till Drive** och välj **Spara på Drive** i menyn som öppnas.
- Du kan också göra det under **Inställningar → Backup till Google Drive**.
- På startsidan ser du om det finns pass som inte har backup.
- **Exportera till kalkylark (CSV)** ger en fil som går att öppna i Google Kalkylark eller Excel.

## Byta telefon

1. Installera appen på den nya telefonen enligt *Installera på telefonen* ovan.
2. Välj **Återställ från backup** på startskärmen, eller under Inställningar.
3. Välj den senaste backupfilen från Google Drive (`stangloggen-backup-ÅÅÅÅ-MM-DD.txt`).

## Så räknar appen

- Pass A: knäböj 3×5, stående press 3×5, marklyft 1×5.
- Pass B: knäböj 3×5, bänkpress 3×5, marklyft 1×5.
- Klarar du alla reps höjs vikten nästa gång: +2,5 kg för knäböj, press och bänk, +5 kg för marklyft. Det går att ändra.
- Missar du en rep blir det samma vikt nästa gång. Efter tre missade pass i rad på samma vikt sänks vikten med 10 %.
- Ändrar du vikten under passet räknas nästa pass från vikten du faktiskt körde.
- Uppvärmning: tom stång 2×5, sedan ett till tre set med stigande vikt och färre reps.
- Vilotimern startar när du trycker på ett set: 3 min efter ett lyckat arbetsset, 5 min efter en miss och 1 min efter ett uppvärmningsset. Tiderna går att ändra under Inställningar.

## Uppdatera appen

Appen publiceras med GitHub Pages från grenen `main`, mappen `/` (root).

- Ändringar som pushas till `main` ligger ute efter en till två minuter.
- Telefonen hämtar uppdateringen i bakgrunden och visar den nästa gång appen startas.
- Lägger du till eller byter namn på en fil som ska fungera utan nät, för in den i `ASSETS` i `sw.js` och räkna upp `CACHE` (till exempel `stangloggen-v4`).

## Filer

| Fil | Innehåll |
|---|---|
| `index.html` | Hela appen: gränssnitt, logik och lagring i telefonen (`localStorage`) |
| `sw.js` | Service worker som gör att appen fungerar utan nät |
| `manifest.webmanifest` | Namn, färger och ikoner för installationen |
| `icon-*.png` | Appikoner (192 och 512 px, plus en maskable-variant för Android) |
