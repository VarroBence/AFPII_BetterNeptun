## BetterNeptun funkcionális specifikáció

## A jelenlegi helyzet leírása

Az egyetemi hallgatók közül sokan tudják, hogy a Neptun nem éppen a leggyorsabb és legstabilabb naplózási rendszer.
Nagy terhelés esetén, pl. a tárgyfelvételi időszak első napján lefagy, lassú, elavult a felülete, hiányzik belőle rengeteg funkció, stb.
Idegesítő 15 perces bejelenkezési limit van rajta, ami már személyesen is megkeserítette az életemet, a mobilos applikáció pedig nem
volt elérhető Eszerházy-s diákoknak, egészen a 2022/23-as tanév 2. félévéig, ami mobilon nehezen kezelhetővé tette a felületet
(ezt csak iOS-en tudom megerősíteni, a régi androidos telefonomra még nem töltöttem le az alkalmazást).
Ezen kellemetlenségek miatt határoztuk el, hogy teljesítsük ezen megrendelést és elkészítsük a BetterNeptun-t: egy teljes újraírást,
mely gyorsabb és megbízhatóbb lesz, szebb kezelőfelülettel és a közösség által legjobban igényelt funkciókkal, melyeknél fontos a tanárok és
hallgatók véleménye ahhoz, hogy leimplementáljuk őket.

## Vágyálomrendszer

Célunk az, hogy a lehető legjobb alternatívát nyújtsuk egyetemi tanároknak és hallgatóknak egyaránt. Maximális odafigyeléssel és többszörös
optimalizáció segítségével a lehető leggyorsabb és legstabilabb egyetemi naplórendzsert kívánjuk létrehozni, mely komoly konkurenciája lenne
az SDA Informatika Zrt. megoldásainak. Ehhez többrétegű Unit-tesztelést végeznénk; egyetlen komoly, a használatot hátráltató hiba sem lehet
a programban!

A stabilitás a szíve-lelke csapatunk filozófiájának.

A kezelőfelület letisztult lenne, mely a mai lapos/féllapos dizájnok elveit követné, hogy a lehető legközérthetőbb legyen mindenki számára a felület.

## Jelenlegi üzleti folyamatok modellje

A Neptun rendszere túlságosan is ingatag nagy terhelés esetén, legfőképpen tárgyfelvételi időszakban. Számos hallgató nem tudja megfelelően rendezni így az órarendjét
és többszörös óraütközések jelennek meg az órarendekben. Ennek következtében a hallgatók kénytelenek kihagyni előadásokat, vagy rosszabb esetben, leadni gyakorlatokat,
mert nem tudják átszervezni másik csoportba magukat.

## Igényelt üzleti folyamatok modellje

Azért, hogy zökkenőmentesebbé és egyszerűbbé tegyük a hallagatók tanulmányait, újradolgozzuk a jelenlegi Neptun rendszert, hogy ne okozzon senkinek sem problémát az
egyetemi tanulmányaiban a tárgyfelvétel. A hallgatóknak nem kell amiatt aggódniuk majd, hogy nem engedi be őket a rendszer, vagy esetleg a tárgyfelvétel közepén kidobja őket és kezdhetnek mindent előlről.

## Követelménylista

![Funk  spec  Követelménylista](https://user-images.githubusercontent.com/78543866/224713674-b377c95e-afb1-44a5-9a1e-57e84daa199f.PNG)

## Használati esetek

Hallgató: Bejelentkezés után megtekintheti az átlagát, órarendjét. Megváltoztathatja a jelszavát, valamint felvehet tárgyakat.

Tanár: Jegyeket tud beírni a hallgatóknak.

## Használati eset - követelmény megfeleltetés

Bejelentkezés (J1): A felhasználó bejelentkezés után a jogosultságának megfelelő funkciókat éri el. Hallgatóknál ez a tárgyfelvétel, órarend valamint átlag megtekintése. Tanároknál jegy beírás adott diáknak.

Jogosultsági szintek(J2): A bejelentkezésnél megadott adatokat leellenőrzive a jogosultságának megfelelő funkciókat ér el a felhasználó.

Jelenlét vezetés - QR kód (J3): A hallgató bejelentkezés után QR kód beolvasása után igazolni tudja a jelenlétét.

Hiányzás követés (J4): A hallgató fel tudja tölteni a hiányzását igazoló dokumentumot a rendszerbe, valamint követni tudja a hiányzásait.

Jegyvezetés (J5): A hallgató meg tudja tekinteni a jegyeit.

Átlagszámítás (J6): A hallgató ki tudja számítani az átlagát a rendszerben meglévő jegyek alapján.

Jelszó módosítása (M1): A felhasználó módosítani tudja a jelszavát bejelentkezés után.

Tárgy felvétel (F1): Bejelentkezés után a hallgató jogkörrel rendelkező felhaszanálók fel tudják venni a tárgyakat.

## Képernyőtervek

## Forgatókönyvek

## Funkció - követelmény megfeleltetés

|	Azonosító	|	Követelmény    |                                                                                   Funkció                                                                                |
|:-------------:|:----------------:|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      BN1      |     Larawell     |Egyszerű Laravel szintaxis, ami megkíméli a back-end programozót a PHP szintaxis rémálmaitól, ezáltal megkímélve mentális és (a megspórolt órák által) fizikai egészségét.|
|      BN2      |   QuickConnect   |Többszörösen optimalizált MySQL-hívások, hogy a naplózás extrém gyors legyen. A filozófiáját a Gentoo Linux operációs rendszer ihlette.                                   |
|      BN3      |      SilkUI      |Lapos dizájn, maximális közérthetőség. A BetterNeptun felületének a lehető elérhetőbbnek kell lennie, még az informatikában laikusok között is.                           |
|      BN4      |    LoginButler   |Az oldal bejelentkezés-kezelője. Segít bejelentkezni és a felhasználó profilját CRUD-műveletekkel kezelni.                                                                |
|      BN5      |   WhereIsWaldo   |A jelenlétet vezeti QR-kód beolvasásával és követi a hiányzásokat, igazolásokat.                                                                                          |
|      BN6      |   AngellicPupil  |Ez a funkció vezeti a jegyeket a naplóba, mely kommunikál a QuickConnect-el és rajta keresztül kezeli a jegyek információját.                                             |
|      BN7      |    MathMerlin    |Gyors matematikai (aritmetikai) logika, amely a (súlyozott) átlagokra és a (korrigált) kreditindexekre lett a végletekig optimalizálva.                                   |
|      BN8      | AestheticCalendar|Jól kinéző és erőteljes naptár az órarend megtekintéséhez és kezeléséhez.                                                                                                 |

## Fogalomszótár
