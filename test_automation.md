# Tesztautomatizálási kérdések

## Tesztelési alapok (ISTQB-hez kapcsolódó)
<img src="https://www.mindsmapped.com/wp-content/uploads/2016/06/ISTQB.jpg" alt="image" width="300" height="220">

## A tesztelés alapjai:
#### Mi a tesztelés célja? Mi nem az?
A tesztelés célja az, hogy a fejlesztés során létrejövő hibákat minél korábban felfedezze, és ezzel csökkentse azok kijavításának költségeit. Nem teszteléshez tartozik a folyamat mikor maga a program részeit építik össze. 
https://hu.wikipedia.org/wiki/Szoftvertesztel%C3%A9s
#### Mi a kapcsolat a tesztelés és a hibamegelőzés között?
A fejlesztésnek minél korábbi szakaszában derül fény egy hibára, annál olcsóbb annak korrigálása.
https://hu.wikipedia.org/wiki/Szoftvertesztel%C3%A9s
#### Miért fontos, hogy a tesztelők függetlenek legyenek a fejlesztőktől?
Két különböző szakirány, különböző ismeretekkel. A tesztelőknek ismernie kell az üzleti oldalát is átfogóan a projektnek, ezáltal nem alakíthatják az eredményeket a fejlesztők igényei szerint.
https://www.jtechlog.hu/2022/08/20/fejlesztok-es-tesztelok.html
#### Mi a veszélye annak, ha a fejlesztő maga teszteli a saját kódját?
A fejlesztő belülről látja a saját programját, projektjét így nincs egy független fél, aki úgy tud hibákat észre venni mint akár egy új felhasználó. Nem is beszélve arról hogy a fejlesztő nem feltétlenül jártas a helyes tesztelési módszerekben.
https://www.jtechlog.hu/2022/08/20/fejlesztok-es-tesztelok.html
#### Mik a tesztelési alapelvek?
A tesztelés hibák jelenlétét jelzi, Nem lehetséges kimerítő teszt, Korai teszt, Hibák csoportosulása, A féregirtó paradoxon, A tesztelés függ a körülményektől, A hibátlan rendszer téveszméje
https://teveli.info/index.php/teszteles/01-alapok/05-szoftvertesztelesi-alapelvek
#### Mit jelent az „alapvető tesztelési elv”, hogy „a kimerítő tesztelés lehetetlen”?
Minden bemeneti kombinációt nem lehet letesztelni (csak egy 10 hosszú karakterláncnak 256^10 lehetséges értéke van) és nem is érdemes. Általában csak a magas kockázatú és magas prioritású részeket teszteljük.
https://teveli.info/index.php/teszteles/01-alapok/05-szoftvertesztelesi-alapelvek
#### Mit jelent az „alapvető tesztelési elv”, hogy „a hibák halmozódnak”?
A tesztelésre csak véges időnk van, ezért a tesztelést azokra a modulokra kell koncentrálni, ahol a hibák a legvalószínűbbek, illetve azokra a bemenetekre kell tesztelnünk, amelyre valószínűleg hibás a szoftver (pl. szélsőértékek).
https://teveli.info/index.php/teszteles/01-alapok/05-szoftvertesztelesi-alapelvek
#### Mit jelent az „alapvető tesztelési elv”, hogy „a tesztelés a kontextustól függ”?
Másképp tesztelünk egy atomerőműnek szánt programot és egy beadandót. Másképp tesztelünk, ha a tesztre 10 napunk vagy csak egy éjszakánk van.
https://teveli.info/index.php/teszteles/01-alapok/05-szoftvertesztelesi-alapelvek


## 2. Tesztelés a szoftverfejlesztés életciklusán át
#### Mik a tesztszintek, és mi a különbség köztük?
Unit teszt, a fejlesztés alatt álló alkalmazás egységeinek tesztelése zajlik itt. Célja, hogy biztonságos alapot nyújtson a felépítmény létrehozásához. Modul (integrációs) teszt, az alkalmazás egyes részei modul készenléti állapotba kerül(het)nek, amikor is a tesztelő feladata, hogy a modullá integrált kódelemeket tesztelje. Rendszerteszt, az alkalmazáson (ha van, akkor) már megjelent a GUI, részben elérhető funkciókkal. A tesztelők megfelelő dokumentációs forrás felhasználásával teszteseteket írnak, ütemeznek, majd futtatnak. A tesztelési szint célja: a feltételezett, jobb esetben leírt specifikációnak megfelelő működés vizsgálata. Elfogadási teszt, a szint célja, hogy a végfelhasználót támogassa az új (általunk) szállított termék elfogadásában. Megírása és elfogadása optimális esetben közös, megrendelői – szállítói feladat.
https://tesztelesagyakorlatban.hu/a-tesztelesi-szintek/
#### Miért nem érdemes mindig ugyanazokat a teszteseteket futtatni (regressziós torzítás)?
Ha állandóan ugyanazokat a teszteseteket használjuk, előfordulhat, hogy az új hibák rejtve maradnak, mivel ezek a tesztek nem fedik le a frissítések vagy módosítások minden lehetséges hatását. Így a tesztelés nem lesz elég hatékony az új problémák feltárásában.
https://tesztelesagyakorlatban.hu/hogyan-javitsd-a-regresszios-teszteleseid-eredmenyesseget-30-kal/
#### Mi az egységtesztelés (unit testing)? Ki felelős az egységtesztek írásáért?
Az egységtesztelés során a program egy-egy kisebb, önálló részét – például függvényeket vagy osztályokat – teszteljük külön-külön. Ezeket a teszteket általában a fejlesztők készítik, hogy biztosítsák az adott egységek helyes működését.
https://learn.microsoft.com/hu-hu/dotnet/architecture/maui/unit-testing
#### Mi a különbség a verifikáció és a validáció között?
A verifikáció és validáció olyan folyamatok, amelyekkel értékeljük és ellenőrizzük egy MI modell megbízhatóságát és teljesítményét különböző környezetekben vagy adathalmazokon. Verifikáció, annak ellenőrzése, hogy a modell fejlesztése és működése megfelel-e a technikai elvárásoknak és specifikációknak. Validáció, annak vizsgálata, hogy a modell valóban azt nyújtja-e, amire a felhasználóknak szükségük van, és a céljainak megfelelően működik-e. 
https://siteland.hu/2023/07/11/verifikacio-es-validacio/
#### Mik a tesztelési típusok, és mi a különbség köztük?
Funkcionális tesztelés: A szoftver funkcióinak helyes működését ellenőrzi. Nem-funkcionális tesztelés: Olyan jellemzőket vizsgál, mint a teljesítmény, biztonság, skálázhatóság vagy a használhatóság.
https://www.guru99.com/types-of-software-testing.html 
#### Mi a különbség a fehér doboz, szürke doboz és fekete doboz tesztelés között?
Fehér dobozos tesztelés: A tesztelő ismeri a kód belső működését, és ennek alapján készíti a teszteseteket. Ez a módszer főként a program logikai felépítésének ellenőrzésére szolgál. Fekete dobozos tesztelés: A tesztelő nem rendelkezik információval a program belső szerkezetéről, kizárólag a bemenetekre és kimenetekre koncentrál. Ez segíti az elfogulatlan hibakeresést. Szürke dobozos tesztelés: A tesztelő részben ismeri a rendszer belső működését, de nem teljes mértékben. Ez a megközelítés ötvözi a fehér és fekete dobozos módszerek előnyeit, lehetővé téve a mélyebb hibák hatékonyabb feltárását.
https://hu.wikipedia.org/wiki/Feh%C3%A9rdobozos_tesztel%C3%A9s
https://www.zaptest.com/hu/szurke-doboz-teszteles-mely-merules-a-mi-ez-tipusok-folyamat-megkozelitesek-eszkozok-es-tobb
https://www.zaptest.com/hu/fekete-doboz-teszteles-mi-az-tipusok-folyamat-megkozelitesek-eszkozok-es-meg-sok-mas
#### Mi a különbség a felhasználói elfogadási teszt (UAT) és a rendszerteszt között?
Rendszertesztelés: A teljes rendszer működését vizsgálja, beleértve az összes modul integrációját és azok közös működését. A cél, hogy meggyőződjünk arról, hogy a rendszer megfelel a technikai elvárásoknak Felhasználói elfogadási teszt (UAT): A végfelhasználók vagy ügyfelek által végzett tesztelés, amely azt ellenőrzi, hogy a szoftver valóban megfelel-e az üzleti igényeknek és elvárásoknak a kiadás előtt.
https://www.zaptest.com/hu/uat-teszteles-mely-merules-a-felhasznaloi-elfogadas-jelentesebe-tipusok-folyamatok-megkozelitesek-eszkozok-es-meg-sok-mas
https://www.zaptest.com/hu/mi-az-a-rendszerteszteles-melyre-merules-a-megkozelitesek-tipusok-eszkozok-tippek-es-trukkok-es-meg-sok-mas
#### Mi a különbség a statikus és dinamikus tesztelés között?
A statikus tesztelés a forráskód vagy dokumentáció vizsgálatára összpontosít, anélkül, hogy a programot futtatnák, míg a dinamikus tesztelés a program futtatásával és az eredmények elemzésével ellenőrzi a szoftver viselkedését
https://www.guru99.com/hu/static-dynamic-testing.html