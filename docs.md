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

----

Tartalomjegyzék

----

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

### Regisztráció
Az alkalmazás használatához rendelkeznünk kell egy regisztrált fiókkal, amit a Sign Up (Regisztrálás) aloldalon hozhatunk létre. Meg kell adnunk az email címünket, felhasználó nevünket (Ajánlott a valódi nevünket használni, hiszen a közös képviselő így tud a legegyszerűbben beazonosítani.) és a jelszónkat. Sikeres regisztráció esetén a megadott email címre egy visszaigazoló email fog érkezni. Az emailben található gomra kattintva megerősíthetjük, hogy valódi címet adtunk meg.

> Sign Up screenshot

### Bejelentkezés

> Login screenshot

# Fejlesztői dokumentáció

## Specifikáció
## Elemzés
## Tervezés

## Fejlesztői környezet
### A fejlesztőkörnyezet kialakítása

## Szerver oldali architektúra

### Felhasznált technológiák
#### Node.js
#### MongoDB
#### JWT
#### WebSocket

### API
### Adatbázis
### Authentikáció

## Kliens oldali architektúra

### Felhasznált technológiák
#### React
#### Redux

### Komponens hierarchia
### Kommunikáció

## Tesztelés
