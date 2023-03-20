# BetterNeptun - Amilyennek a Neptunnak kellett volna lennie

## Áttekintés

A mi projektünk a Neptun teljes körű újraírásáról szól, melyet legálisan, az SDA Informatika Zrt. forráskódja nélkül készítünk el.
A weboldalt többféle programozási technológia felhasználásával készítjük el:

- Adatbázis és kezelése: MySQL
- Back-end: Laravel (a háttérben a PHP dolgozza fel a Laravel-szintaxist)
- Front-end: HTML, CSS, JavaScript
- Unit-tesztelés: Cypress 

## A jelenlegi helyzet leírása

Az egyetemi hallgatók közül sokan tudják, hogy a Neptun nem éppen a leggyorsabb és legstabilabb naplózási rendszer.
Nagy terhelés esetén, pl. a tárgyfelvételi időszak első napján lefagy, lassú, elavult a felülete, hiányzik belőle rengeteg funkció, stb.
Idegesítő 15 perces bejelenkezési limit van rajta, ami már személyesen is megkeserítette az életemet, a mobilos applikáció pedig nem
volt elérhető Eszerházy-s diákoknak, egészen a 2022/23-as tanév 2. félévéig, ami mobilon nehezen kezelhetővé tette a felületet.
Ezen kellemetlenségek miatt határoztuk el, hogy teljesítsük ezen megrendelést és elkészítsük a BetterNeptun-t: egy teljes újraírást,
mely gyorsabb és megbízhatóbb lesz.

## Vágyálomrendszer

Célunk az, hogy a lehető legjobb alternatívát nyújtsuk egyetemi tanároknak és hallgatóknak egyaránt. Maximális odafigyeléssel és többszörös
optimalizáció segítségével a lehető leggyorsabb és legstabilabb egyetemi naplórendszert kívánjuk létrehozni, mely komoly konkurenciája lenne
az SDA Informatika Zrt. megoldásainak. Ehhez többrétegű Unit-tesztelést végeznénk; egyetlen komoly, a használatot hátráltató hiba sem lehet
a programban! A stabilitás a szíve-lelke csapatunk filozófiájának.

## Jelenlegi üzleti folyamatok modellje

A jelenlegi Neptun rendszer túlságosan is használhatatlan nagy terhelés esetén. Rengeteg hallgató nem tudja számára megfelelően felvenni a tárgyakat a tárgyfelvételi
időszakban, hosszas várakozás után egy hibaüzenetet kapnak és próbálkozhatnak újra a bejelentkezéssel. Ha sikerül bejelentkezniük az sem garantálja, hogy fel tudják
venni a tárgyakat, hiszen bármelyik pillanatban kidobhatja őket a rendszer. 15 perc után a hallgatót automatikusan kijelentkezteti a rendszer, amely egyáltalán nem
praktikus. Ezek mellett maga a felület kissé elavult, rengeteg hasznos funkcióval lehet bővíteni a már meglévő rendszert, hogy megkönnyítsük a felhasználók dolgát és
egyszerűbbé, átláthatóbbá tegyük az oldalt.

## Igényelt üzleti folyamatok modellje
![Igényelt üzl  foly  mod](https://user-images.githubusercontent.com/78543866/226204795-c97ec319-8de0-4bc5-ade3-f46e49bb8886.png)

## Követelménylista

Funkcionális követelmények: - tanár -> kurzusok böngészése, kurzus létrehozása/módodítása, tanulók értékelése, email küldése a kurzus résztvevőinek. vizsgák kiírása, 
hallgató adatainak megtekintése
 - diák -> kurzusok böngészése, kurzusok felvétele, haladás megtekintése, bejelentkezés,
félév aktiválás - passziválás, szakkal kapcsolatos információk megtekintése
	
Nem-funkcionális követelmények: 2msp-nél rövidebb bejelentkezési idő, 2mspnél rövidebb tárgy listázás, biztonságos adattárolás,
backup, adatvesztés megelőzése

Felhasználói követelmények: sötét mód, angol nyelv, mobil-kompatibilitás

## Fogalomtár

MySQL: SQL alapú relációs adatbázis-kezelő szerver.

Back-end: A programoknak, weboldalaknak a hátsó, a felhasználó elől rejtett, a tényleges számításokat végző része. Feladata a front‑end (a felhasználóval kapcsolatban
lévő rész) felől érkező adatok feldolgozása, és az eredményeknek a front‑end felé történő visszajuttatása.

Front-end: A programoknak, weboldalaknak az a része, amelyik a felhasználóval közvetlenül kapcsolatban van. Feladata az adatok megjelenése, befogadása a felhasználó
(vagy ritkábban egy másik rendszer) felől.

Laravel: Ingyenes és nyílt forráskódú PHP webes keretrendszer.

PHP: Általános szerveroldali szkriptnyelv dinamikus weblapok készítésére.

HTML: Egy leíró nyelv, melyet weboldalak készítéséhez fejlesztettek ki, és mára már internetes szabvánnyá vált a W3C támogatásával.

W3C: A World Wide Web Consortium egy konzorcium, mely nyílt szoftver szabványokat alkot a világhálóra.

CSS: A Cascading Style Sheets egy stíluslapnyelv, amelyet egy jelölőnyelven, például HTML-en vagy XML-en írt dokumentumok megjelenítésének leírására használnak. A CSS
a World Wide Web egyik sarokköve a HTML és a JavaScript mellett.

XML: Az XML a W3C által ajánlott általános célú leíró nyelv, speciális célú leíró nyelvek létrehozására.

JavaScript: A JavaScript programozási nyelv egy objektumorientált, prototípus-alapú szkriptnyelv, amelyet weboldalakon elterjedten használnak.

Unit-teszt: A legalacsonyabb szintű tesztelés. A részegységeket egyesével tesztelik le.

Cypress: Egy előtérbeli tesztelőeszköz webes alkalmazásokhoz.
