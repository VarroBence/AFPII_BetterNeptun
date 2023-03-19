# BetterNeptun rendszerterv

## A rendszer célja

A rendszer célja, hogy egy modernebb, gyorsabb szintre hozza a jelenlegi Neptun rendszert. A hallgatók a letisztult kinézettel felújított felületen tisztán tudnak
navigálni. A rendszer nem dobja ki őket akkor sem, amikor rengetegen próbálnak egyszerre például tárgyakat felvenni. Nincsen bejelentkezési időkörlát, így nem kell
sietve elvégezni a dolgokat az oldalon. Egyszerűen kiszámítható a hallgató átlaga egy külön, erre a célra szánt oldalon. Az órarendjét tisztán átlátja a hallgató,
hiányzásait igazoló papírokat egyszerűen fel tudja tölteni, ezzel igazolva távollétének okát. Ezek mellett a gyakorlaton való jelenlét rögzítése egy egyszerű QR kód
beolvasásával történik.

## Projektterv

### Projektszerepkörök, felelősségek

Product owner: Bagoly Gábor

Scrum master: Molnár László

### Projektmunkások és felelősségek

Design: Göröcs Lajos Zsolt, Varró Bence

Developer: Göröcs Lajos Zsolt, Varró Bence

Tesztelő: Göröcs Lajos Zsolt, Varró Bence

### Ütemterv

![Ütemterv](https://user-images.githubusercontent.com/78543866/226213791-68d31345-75af-4e81-a3e6-b3e412c5e458.PNG)

## Üzleti folyamatok modellje

![Rendszert  - Üzl  foly  mod](https://user-images.githubusercontent.com/78543866/226214150-f9f85efe-f5b9-4390-9ed4-5e384eeccce9.PNG)

## Követelmények

### Funkcionális követelmények

- Felhasználók adatainak tárolása
- Jelenlét igazolása QR beolvasásával
- Hiányzás igazolás
- Órarend
- Jegyvezetés
- Átlagszámítás

### Nem funkcionális követelmények

- A felhasználók nem férhetnek hozzá egymás órarendjéhez/jegyeihez/igazolásaihoz

## Funkcionális terv

### Rendszerszereplők

Hallgató, Admin

### Rendszerhasználati esetek és lefutásaik

Admin:

- Beléphet bármilyen szereplőként teljes hozzáférése van a rendszerhez
- Tárgyak törlése/módosítása

Hallgató:

- Meg tekintheti az órarendjét
- Ki tudja számítani az átlagát
- QR kód beolvasásával igazolni tudja hogy jelen volt az órán
- Hiányzását igazolni tudja az igazoló dokumentum feltöltésével

### Menühierarchiák

Main page:

- Órarend megjelenítése
- Átlag kiszámítása gomb
- Jelenlét gomb
- Hiányzás igazolása gomb

Átlag kiszámítása page:

- Input mezők az átlag kiszámításához szükséges jegyeknek
- Main page gomb
- Jelenlét gomb
- Hiányzás igazolása gomb

Jelenlét page:

- Beolvasandó QR kód megjelenítése

Hiányzás igazolása page:

- Input mező a hiányzást igazoló dokumentum feltöltéséhez

## Fizikai környezet

## Architekturális terv

## Implementációs terv

## Adatbázis terv

## Teszt terv

## Telepítési terv

## Karbantartási terv
