# BetterNeptun - Amilyennek a Neptunnak kellett volna lennie

## Áttekintés

A mi projektünk a Neptun teljes körű újraírásáról szól, melyet legálisan, az SDA Informatika Zrt. forráskódja nélkül készítünk el.
A weboldalt többféle programozási technológia felhasználásával készítjük el:

- Adatbázis és kezelése: MySQL
- Back-end: Laravel (a háttérben a PHP dolgozza fel a Laravel-szintaxist)
- Front-end: HTML, CSS, JavaScriptű
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
optimalizáció segítségével a lehető leggyorsabb és legstabilabb egyetemi naplórendzsert kívánjuk létrehozni, mely komoly konkurenciája lenne
az SDA Informatika Zrt. megoldásainak. Ehhez többrétegű Unit-tesztelést végeznénk; egyetlen komoly, a használatot hátráltató hiba sem lehet
a programban! A stabilitás a szíve-lelke csapatunk filozófiájának.

## Követelménylista

Funkcionális követelmények: tanár -> kurzusok böngészése, kurzus létrehozása/módodítása, tanulók értékelése, email küldése a kurzus résztvevőinek. vizsgák kiírása, 
hallgató adatainak megtekintése
diák -> kurzusok böngészése, kurzusok felvétele, haladás megtekintése, bejelentkezés,
félév aktiválás - passziválás, szakkal kapcsolatos információk megtekintése
	
Nem-funkcionális követelmények: 2msp-nél rövidebb bejelentkezési idő, 2mspnél rövidebb tárgy listázás, biztonságos adattárolás,
backup, adatvesztés megelőzése

Felhasználói követelmények: sötét mód, angol nyelv, mobil-kompatibilitás
