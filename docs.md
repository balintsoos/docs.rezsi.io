ELTE címer

Eötvös Loránd Tudományegyetem

Informatikai Kar

Média- és Oktatásinformatika Tanszék

Webes alkalmazás társasházak közüzemi fogyasztásainak adminisztrálására

Dr. Horváth Győző

egyetemi adjunktus

Soós Bálint

programtervező informatikus Bsc

Budapest, 2018

# Tartalomjegyzék

# Bevezetés

## Motiváció
Újépítésű társasházakban egyre jellemzőbb a központi kazán, amellyel a lakások fűtését és melegvízellátását biztosítják. Ilyen rendszer mellett a lakók fogyasztásainak adminisztrálása a közös képviselő feladata lesz, azonban ennek kivitelezése a lakóknak és a közös képviselőnek is komoly odafigyelést és terhet jelent.

Saját helyzetemből kiindulva, az én társasházamban minden hónap végén egy papírlapot függesztenek ki a lépcsőházban, amelyre minden lakónak kézzel kell beírni a hőmennyiségmérő és a vízórák állását. Ezt a papírlapot a bejelentési időszak végeztével a közös képviselő elviszi és kézzel viszi fel az adatokat egy Excel táblába, ahol kiszámolja a havi fűtés és melegítés díjat. A számlák kitöltése szintén kézzel történik, amiket ezután a postaládába dobva kézbesítenek a lakóknak. Ez a rendszer lassú, és a legtöbb lépésben ott van az emberi hibalehetőség is. Ennek a rendszernek a kiváltására szeretnék tervezni egy webes alkalmazást, amely a lépések automatizálásával kiküszöbölheti az emberi tényezőt és kényelmes felületet nyújthat a társasház lakóinak és a közös képviselőnek.

## Felhasználási igények
Az alkalmazásnak két fő felhasználási igényt kell kielégíteni. A lakók számára egy könnyen átlátható felületet kell biztosítani, ahol felölthetik a fogyasztásmérők állását, illetve megtekinthetik a kapott számlákat. A közös képviselőnek egy adminisztrációs felületet kell biztosítani, ahol láthatja a fogyasztási adatokat, és ezek alapján számlákat tud kiállítani, majd ezeket elküldeni a lakóknak.

# Felhasználói dokumentáció

## Követelmények
Az alkalmazás használatához szükség van egy JavaScript futtatására alkalmas webböngészőre, internet hozzáférésre és email címre. Az alkalmazás csak angol nyelven érhető el, így szükség van minimális angol nyelvtudásra is.

### Támogatott böngészők:
- Google Chrome (v62.x és későbbi verziók)
- Google Chrome for Android (v62.x és későbbi verziók)

## Alkalmazás használata

### Alkalmazás használata közös képviselők számára
#### Regisztráció
Az alkalmazás használatához rendelkeznünk kell egy regisztrált fiókkal, amit a Sign Up (Regisztrálás) aloldalon hozhatunk létre. Meg kell adnunk az email címünket, felhasználó nevünket és a jelszónkat. Sikeres regisztráció esetén a megadott email címre egy visszaigazoló email fog érkezni. Az emailben található gombra kattintva erősítsük meg, hogy valódi címet adtunk meg.

> Sign Up screenshot

#### Bejelentkezés
Az alkalmazásba való belépéshez navigáljunk a Login (Bejelentkezés) aloldalra és írjuk be a regisztrációkor megadott email címet és jelszót.

> Login screenshot

#### Kijelentkezés
Az alkalmazás jobb felső sarkában található menü ikonra kattintva a felugró menüben láthatjuk az aktuálisan bejelentkezett felhasználó nevét és email címét. A Sign Out gombra kattintva kijelentkezhetünk az alkalmazásból.

> Logout screenshot

#### Új csoport létrehozása
Jövőbeli felhasználóinkat (lakóinkat) saját preferenciáink szerint csoportokba oszthatjuk. A csoportosítás módja a közös képviselőre van bízva, ez lehet például épület, lépcsőház, vagy akár szint alapján. Egy felhasználó csak egy darab csoport tagja lehet. Új csoport létrehozásához a csoport nevét kell megadni.

> Groups screenshot

> Create group screenshot

#### Csoport szerkesztése és törlése
A már létező csoportok nevét átírhatjuk, vagy akár törölhetjük az egész csoportot a hozzá tartozó felhasználókkal együtt. Ebben az esetben a törölt felhasználók többé nem lesznek képesek bejelentkezni az alkalmazásba.

> Group options screenshot

> Edit group screenshot

> Delete group screenshot

#### Lakók meghívása a csoportba
Új lakók meghívásához kattintsunk az adott csoport lakóinak listájánál az Invite gombra. A megjelenő párbeszédablakban található linken keresztül tudnak regisztrálni a lakók a csoportunkba. Ez a link teljesen publikus, így fokozottan figyeljünk oda, hogy kinek küldjük el.

> Invite dialog screenshot

#### Lakó törlése
A csoportba felvett lakókat egyesével törölhetjük. A törölt lakók többé már nem lesznek képesek bejelentkenzni az alkalmazásba. Újrafelvételükhöz újra regisztrálni kell.

#### Csoportos számla kiállítása
A csoport összes tagja számára egyszerre tudunk kiállítani számlát. A csoport számláinak listájánál kattintsunk A Create bill gombra. A felugró párbeszédablakban meg kell adnunk a számlázási időszak kezdetének dátumát, a számlázási időszak végének dátumát, a pénznemet, a fűtés egységárát pénznem/kWh-ban, a melegvíz egységárát köbméter/pénznemben, és a hidegvíz egységárát köbméter/pénznemben. A számlá készítéséről minden érintett felhasználó értesítést kap.

#### Csoportos számla adatainak letöltése
A kiállított csoportos számla adatait letölthetjük CSV formátumban. Ehhez a csoport számláinak listájában a számla alatti Download as CSV gombra kell kattintani. A fájl egy sora tartalmazza a csoporthoz tartozó lakó nevét, email címét, az adott időszakban felhasznált fűtés mennyiségét kWh-ban, a fűtés egységárát pénznem/kWh-ban, fűtés összdíját az adott pénznemben, melegvíz fogyasztást köbméterben, melegvíz egységárát köbméter/pénznemben, melegvíz összdíját, hidegvíz fogyasztást köbméterben, hidegvíz egységárát köbméter/pénznemben, hidegvíz összdíját, a megadott pénznemet és a végösszeget.

#### Lakó fogyasztási adatainak és számláinak megtekintése
A csoport lakóinak listájánál ha rákkatintunk egy adott lakóra, akkor megtekinthetjük az adott lakó összes fogyasztási bejelentését és az összes kiállított számláját. A bejelentések tartalmazzák a bejelentés napjának dátumát, és a fogyasztásmérők állását: a hőmennyiséget kWh-ban és a meleg-, illetve hidegvíz mennyiségét köbméterben. A számlák tartalmazzák a kiállítás dátumát, a számlázási időszak kezdetének és végének dátumát, illetve egy táblázatban lebontva a fogyasztások díjait a végösszeggel együtt.

#### Lakó számlájának letöltése
A lakók kiállított számláit szabadon letölthetjük PDF formátumban. Ehhez kattintsunk a lakó számláinak listájában a számla alatt található Download as PDF gombra. A letöltött fájl tartalmazza a számla azonosítószámát, kiállításának dátumát, a számlázási időszak kezdetének és végének dátumát, illetve egy táblázatban lebontva a fogyasztások díjait a végösszeggel együtt.

### Alkalmazás használata lakók számára
#### Regisztráció
Az alkalmazás használatához rendelkeznünk kell egy regisztrált fiókkal, amit a közös képviselőtől kapott linken keresztül tehetünk meg. Meg kell adnunk az email címünket, felhasználó nevünket és a jelszónkat. Ajánlott a valódi nevünket használni, hiszen a közös képviselő így tud a legegyszerűbben beazonosítani minket. Sikeres regisztráció esetén a megadott email címre egy visszaigazoló email fog érkezni. Az emailben található gombra kattintva erősítsük meg, hogy valódi címet adtunk meg.

> Sign Up screenshot

#### Bejelentkezés
Az alkalmazásba való belépéshez navigáljunk a Login (Bejelentkezés) aloldalra és írjuk be a regisztrációkor megadott email címet és jelszót.

> Login screenshot

#### Kijelentkezés
Az alkalmazás jobb felső sarkában található menü ikonra kattintva a felugró menüben láthatjuk az aktuálisan bejelentkezett felhasználó nevét és email címét. A Sign Out gombra kattintva kijelentkezhetünk az alkalmazásból.

> Logout screenshot

#### Új bejelentés készítése

#### Értesítés számla kiállításáról

#### Számla letöltése
A kiállított számlákat szabadon letölthetjük PDF formátumban a számla alatt található Download as PDF gombra kattintva. A letöltött fájl tartalmazza a számla azonosítószámát, kiállításának dátumát, a számlázási időszak kezdetének és végének dátumát, illetve egy táblázatban lebontva a fogyasztások díjait a végösszeggel együtt.

# Fejlesztői dokumentáció

## Specifikáció
## Elemzés
## Tervezés

## Fejlesztőkörnyezet
### Rendszerkövetelmények
### A fejlesztőkörnyezet kialakítása

## Development Workflow
### Buildelés
### Deploy

## Continuous delivery

## Szerver oldali architektúra
### API
#### Végpontok
#### Felhasznált technológiák
##### Node.js
##### Express

### Adatbázis
#### Felhasznált technológiák
##### MongoDB
##### Mongoose

### Authentikáció
#### Felhasznált technológiák
##### Passport.js
##### JWT

### Értesítési rendszer
#### Felhasznált technológiák
##### WebSocket

## Kliens oldali architektúra

### Felhasznált technológiák
#### React
#### Redux

### Komponens hierarchia
### Kommunikáció

## Tesztelés
