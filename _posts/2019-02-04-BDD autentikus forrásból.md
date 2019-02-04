---
layout: post
title: A viselkedésalapú fejlesztés - Behaviour Driven Development (BDD) - tiszta forrásból
categories: cikkek, security, bdd, specflow
---

Honnan is kezdjem? Talán onnan, amivel sokszor egy lapon említik: viszonylag ismert fogalom a TDD, magyarul talán tesztek által vezérelt fejlesztési megközelítésnek mondanám. Azt jelenti, hogy egy új funkció -vagy felmerülő hiba kijavítása- esetén _először_ megírjuk a teszteket. Ezek lesznek a _teljesítendő követelmények_. Majd _a tesztek alapján_ következik az "igazi" fejlesztőmunka: addig igazítjuk a kódunkat, amíg a tesztek hiba nélkül lefutnak. 

Előnyök? A fejlesztésünk eredménye pontosan teljesíti a követelményeket. A későbbiekben pedig már "nem tudjuk" észrevétlenül elrontani, ugyanis, ha baj van, és a teszteket futtatjuk, azonnal kiderül. Így bátrabban mehet a módosítás vagy a refactoring, és a végeredmény is garantáltabban ad jobb minőséget. 

A kihívás ebben a jó tesztek meghatározása és megírása, tesztelhető megoldás készítése valamint a változásokkal párhuzamosan a tesztek naprakészen tartása.

Ez konyhanyelven a TDD leírása.

A [BDD megközelítésről](https://en.wikipedia.org/wiki/Behavior-driven_development) már [kevesebben hallottunk](https://hup.hu/szavazasok/20171006/tudod_mi_az_a_bdd_behavior_driven_development). 

Fontos megjegyezni, hogy bár a BDD és a TDD kifejezések eléggé hasonlatosnak tűnnek (mindegyiknek a vége DD, azaz _driven development_) [nem ikertestvérek](https://www.glowtouch.com/test-driven-development-vs-behavior-driven-development/), sőt. Legalább annyi különbség van a kettő között, mint amennyire hasonló a két fogalom.

A [BDD](https://www.scaledagileframework.com/behavior-driven-development) -szintén konyhanyelven- arról szól, hogy az elkészítendő feladat _viselkedési mintáit_ rögzítjük, mint teljesítendő követelményeket. Majd a TDD-hez hasonlóan (ezért * _driven development_ ugye) ezekből a mintákból valahogy megoldást fejlesztünk, amiknek ezeket a rögzített viselkedési mintákat ellenőrizhető módon teljesítenie kell.

A csavar ott van a dologban, hogy a viselkedési mintákat **jellemzőkbe** (feature) csoportosítjuk, majd ezekhez a jellemzőkhöz **forgatókönyveket** (scenario) írunk. Végül ezekből a forgatókönyvekből aztán tesztek lesznek, amit már hagyományos fejlesztői eszközökkel írunk meg.

De. És ez a legnagyobb de. Nem valamilyen programnyelven írjuk a **forgatókönyveket** és a **jellemzőket**, hanem ezek egy üzleti felhasználó által is megérthető (un. [Business Readable Domain Specific Language - BR.DSL](http://docs.behat.org/en/v2.5/guides/1.gherkin.html)) nyelven készülnek.

Vagyis duplagondol-duplacsavar-duplafenék, és így leírva elég macerásnak is tűnik, **viszont ez nem feltétlenül igaz**. Ha _**jó**_ eszközünk van, akkor kézbentartható a feladat, és ölünkbe hullik tengernyi előny.

Ezért _is_ írtam ezt a pár sort. 

De leginkább azért, mert szerintem nem kap elég figyelmet, hogy [**magyar fejlesztőé**](http://gasparnagy.com/) a BDD egyik autentikus és a világban [széles körben elterjedt](https://www.softwaretestinghelp.com/behavior-driven-development-bdd-tools/) C#/dotnet/dotnetcore alapú megoldása, a [SpecFlow](https://specflow.org/). 
[Nyílt forráskódú](https://github.com/techtalk/SpecFlow), sokféle tesztelési környezetet [támogat](https://specflow.org/documentation/Unit-Test-Providers/), a bdd fejlesztők legelterjedtebb eszközének ([cucumber](https://cucumber.io/)) a ([gherkin](http://docs.behat.org/en/v2.5/guides/1.gherkin.html)) BR.DSL nyelvét  használja. Vagyis mondhatni, a világban már kialakult és kiválóan használható művészetet terjeszti ki a dotnet fejlesztők számára is elérhetővé.

És azért tiszta forrásból, mert február 21-én [a szerző ingyenes webinar-t tart a BDD-ről](https://smartbear.com/resources/webinars/is-bdd-for-me/), érdemes részt venni rajta.