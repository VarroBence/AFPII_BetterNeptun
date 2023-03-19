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

Az alkalmazás egy olyan webes felületen készült, amely Laravel keretrendszeren fut, nincsenek megvásárol komponenseink.

Fejlesztői eszközök: Visual Studio Code, XAMMP, PHP myadmin.

## Architekturális terv

Front-end: BootStrap Studio

Back-end:

- A back-end fejlesztéséhez szükséges egy adatbázis szerver, amit MySQL-lel valósítuttuk meg.
- Laravel framework a szabványos fájlkezelés és összetettebb fejlesztési lehetőségek végett.
- PHP

## Implementációs terv

A webes felület főként Php nyelven íródott minimális JavaScript alkalmazásával és Laravel keretrendszerrel. Ezeket a technológiákat amennyire csak lehet külön fájlokba
írva készítjük, és úgy fogjuk egymáshoz csatolni a jobb átláthatóság, könnyebb változtathatóság, és könnyebb bővítés érdekében. Az oldalakat és azokat vezérlő fájlokat
a keretrendszer által biztosított lehetőségekkel különítettük el.

## Adatbázis terv

![Rendszerterv - adatb  terv](https://user-images.githubusercontent.com/78543866/226215510-19d4a8e9-58a2-409e-ae96-7257268231e6.png)

## Teszt terv

Tesztelendő Windows rendszerek: Windows 10, vagy újabbak.

Tesztelendő kijelző méretek: 1280x720 (minimum), 1366x768, 1920x1080.

A tesztelés időtartama egy hét.

### Tesztelendő funkciók

Hallgató:

- QR kód beolvasásával igazolni tudja jelenlétét.
- Fel tudja tölteni a hiányzását igazoló dokumentumot.
- Ki tudja számítani az átlagát jegyeinek megadásával.

Admin:

- Képes tárgyakat törölni.

## Telepítési terv

A weboldal megnyitásához szükséges lesz telepíteni a Xampp nevű programot, és annak a kezelőfelületén elindítani a szerver hostolását helyi hálozatra. Az Apache és
MySQL melett elhelyezkedő start gombok megnyomásával.

![image](https://user-images.githubusercontent.com/103049058/206261590-1126c99f-b09e-4af3-9c64-2d2d059fecc3.png)

Ez után szükség lesz a Composer nevezető programra, amit letöltés után telepíteni kell.
Telepítést követően a windows parancssorban az xampp/htdocs mappába kell navigálni, és ott lefuttatni egy új projekt létrehozásához szükséges parancssort.

![image](https://user-images.githubusercontent.com/103049058/206265273-a6191284-cb68-4b8b-aac9-44482d3d41af.png)

A myapp nevezetű mappában felül kell írni mindent a mi github felületenünkön lévő projekt fájljaival.

A felülírás elvégézése után ismét a parancssorra lesz szükség, mivel itt elkell most navigálni a myapp nevezetű könyvtárba és futtatni a következő parancsot:

![image](https://user-images.githubusercontent.com/103049058/206265655-0c5c4cd5-4e9a-4c8d-ae21-36c7b9665388.png)

Az itt kapott címet kimásolva és beillesztve a böngészőbe megjeleníthetjük a weboldalt.

![image](https://user-images.githubusercontent.com/103049058/206265860-431d3de4-fe0c-4adb-9efe-92ed78f8ecb7.png)

## Karbantartási terv
