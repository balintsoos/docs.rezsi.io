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
- Google Chrome (v62.x)
- Google Chrome for Android (v62.x)

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

#### Lakó törlése
A csoportba felvett lakókat egyesével törölhetjük. A törölt lakók többé már nem lesznek képesek bejelentkenzni az alkalmazásba. Újrafelvételükhöz újra regisztrálni kell.

#### Csoportos számla kiállítása

#### Csoportos számla adatainak letöltése

#### Lakó fogyasztási adatainak és számláinak megtekintése

#### Lakó számlájának letöltése

### Alkalmazás használata lakók számára
#### Regisztráció
Az alkalmazás használatához rendelkeznünk kell egy regisztrált fiókkal, amit a közös képviselőtől kapott linken keresztül tehetünk meg. Meg kell adnunk az email címünket, felhasználó nevünket és a jelszónkat. Ajánlott a valódi nevünket használni, hiszen a közös képviselő így tud a legegyszerűbben beazonosítani minket. Sikeres regisztráció esetén a megadott email címre egy visszaigazoló email fog érkezni. Az emailben található gombra kattintva erősítsük meg, hogy valódi címet adtunk meg.

> Sign Up screenshot

#### Bejelentkezés
Az alkalmazásba való belépéshez navigáljunk a Login (Bejelentkezés) aloldalra és írjuk be a regisztrációkor megadott email címet és jelszót.

> Login screenshot

# Fejlesztői dokumentáció

## Specifikáció
## Elemzés
## Tervezés

## Fejlesztői környezet
### A fejlesztőkörnyezet kialakítása

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
