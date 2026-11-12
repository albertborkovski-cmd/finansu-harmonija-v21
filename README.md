# Finansų harmonija V21

2026-11-12 užfiksuota testavimo versija iš naujausios V20 darbinės kopijos. V21 nebetobulinama: tolesnis darbas vyksta atskiroje V22 kopijoje.

Testavimas: https://albertborkovski-cmd.github.io/finansu-harmonija-v21/

## Paleidimas

```bash
npm ci
npm run dev
```

Vietinis V21 adresas: http://127.0.0.1:5202/.
V22 tobulinimo adresas: http://127.0.0.1:5203/.

## Leidimo turinys

Įtraukta visa dabartinė V20 programos versija: dokumentai ir sąskaitų kūrimas, OCR Workspace / My tasks / Document issues, finansinės atskaitomybės straipsniai, banko operacijų peržiūra ir kūrimas, mokėjimų juodraščiai, banko DK priskyrimas ir prijungimo būsenos.

GitHub saugykloje publikuojama sukompiliuota svetainė ir tikslus `source-v21.zip` archyvas, `source-manifest.json` bei `release.json` su SHA-256 ir patikrų rezultatais. Vietinė šaltinių Git istorija nepakeičia GitHub artefaktų istorijos. V20 ir ankstesnės publikacijos nekeičiamos.

## Demonstracinis prisijungimas

- Vidinis administratorius: `albertborkvski@gmail.com`.
- Išorinis naudotojas: `aurika.z@meso.lt`.
- Slaptažodžio laukas prototipe tikrina formatą: bent 6 simboliai, didžioji raidė ir specialus simbolis. Naudokite išgalvotą testinę reikšmę, ne tikrą slaptažodį.

Tai demonstracinis prototipas, ne produkcinė apskaitos sistema. GitHub Pages neturi saugaus serverinio autentifikavimo, bendros duomenų bazės, tikro OCR, banko, apskaitos sistemos ar el. laiškų siuntimo API. Mokėjimai išsaugomi kaip juodraščiai, ne siunčiami į banką. Connect bank išsaugo teikėjo pasirinkimą, tačiau nepradeda banko autorizacijos ir nepakeičia būsenos į Connected. Demonstracinės prijungimo būsenos nėra tikras banko ryšys.

Vietiniai `.env`, `.meso-shared-data.json`, `node_modules` ir kiti privatūs darbo failai nepublikuojami. Nenaudokite konfidencialių dokumentų ar tikrų slaptažodžių. To paties GitHub Pages domeno leidimai gali dalytis naršyklės saugykla; izoliuotam testavimui naudokite atskirą naršyklės profilį.

## Patikros

TypeScript patikra, leidimo kompiliavimas ir tiksliniai banko / mokėjimų / DK priskyrimo testai tikrinami prieš publikavimą. Pilno testų rinkinio rezultatai ir žinomi senesnių testinių pakaitalų neatitikimai dokumentuojami `release.json`; nesėkmingi testai nelaikomi praėjusiais.
