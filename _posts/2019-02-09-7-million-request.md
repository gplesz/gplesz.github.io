---
layout: post
title: Hogy _teljesít_ az ASP.NET Core?
categories: cikkajánló 
---

Hát jól. Nagyon jól. Nagyon-nagyon-nagyon jól. Ahogy az írás végén hivatkozott cikk írja, az **ASP.NET Core 2.2** (0,046%-al elmaradva a legelső helyezettől) **a 3. leggyorsabb webszerver** jelenleg, ami a tesztben részt vett. Másodpercenként több, mint 7.000.000 (hétmillió) kérés kiszolgálásával.

---
>Itt tegyünk egy rövid kitérőt, mi is ez a teszt? A [Techempower](https://www.techempower.com/) 2013 óta [foglalkozik különböző webes környezetek összehasonlítható módon való tesztelésével](https://www.techempower.com/blog/2013/03/28/frameworks-round-1/). Ehhez [egy nyílt forráskódú környezetet](https://github.com/TechEmpower/FrameworkBenchmarks) alakított ki, környezet alatt értve [nagyon sok mindent](https://www.techempower.com/benchmarks/#section=motivation), ami a teszthez kell.
>
>A tesztek ökoszisztémájáról azt gondolom, hogy érdemes majd sokkal hosszabban beszélni, tervezek is ezzel foglalkozni. Ezekből a kódokból, cikkekből és eredményekből rengeteget lehet tanulni nemcsak egy tesztelőnek hanem *minden fejlesztőnek*, aki a webes kiszolgálással kapcsolatba kerül. Ez napjainkban gyakorlatilag elkerülhetetlen.
>
>A rövid kitérőnket zárjuk most le azzal, hogy ez egy nagyon komoly teszt, transzparens, a végeredményében megbízható adatokat szállító, több éves múlttal rendelkező, egy szóval *tiszta forrás*.
>
---

Nézzük a teszt legújabb eredményeit ASP.NET Core 2.2 szemszögből.

- Első eredményként sima szöveges (plaintext) kiszolgálásban (ami a legkevesebb erőforrást igénylő, tehát leggyorsabban megoldható feladat) a már írt harmadik helyezett, 3212 kéréssel (ami az összes kérés 0,046%-a) lemaradva az első helyezettől. A szereplők ebben a tesztben fejlesztőkörnyezetek. Itt érdemes megnézni a listát, az első helyezett az **[actix-raw](https://actix.rs/)**. A link az ACTIX oldalára visz, egyelőre nem tudom pontosan, hogy a "*-raw" mit jelent, [talán egy beállítás, ha jól látom](https://github.com/TechEmpower/FrameworkBenchmarks/pull/3767). A második pedig a **[wizzardo-http](https://github.com/wizzardo/http)**. Bevallom férfiasan, egyiket sem ismertem korábban, már csak erre is jó, hogy megnéztem a teszteredményeket.

- Második eredményként kiemelhető, hogy a **webszerverek** között *a leggyorsabb*. Több, mint *másfélszer gyorsabb*, mint az **nginx**, majdnem *kétszer gyorsabb*, mint a **Java servlet**, több, mint *hétszer gyorsabb*, mint a **Golang net/http** csomag, és több, mint *nyolcszor* gyorsabb, mint a **node.js**. Mivel a node.js egyszálú végrehajtási modellt használ, így 28 párhuzamos folyamatot használtak a node.js tesztben.

Fontos figyelnünk arra, hogy *nem lehet **egy** objektív tesztet futtatni*. Milyen *adatbázist* használunk? Milyen *operációs rendszert*? Használunk valamilyen *ORM*-et a perzisztens adatok felé? Mi van a *cache* mechanizmussal? És így tovább, a sort nagyon hosszan lehetne folytatni.

Ezért is végeznek rengeteg permutációval és beállítással [rengeteg tesztet](https://github.com/TechEmpower/FrameworkBenchmarks/issues/133). Dotnet fejlesztőként én most -talán nem teljesen elitélhető módon- a szívemnek legszebb eredményeket emeltem ki, de érdemes böngészni minden adatot.

- Utolsó fontos megjegyzésként kénytelen mindenki észrevenni, hogy ezek az eredmények **Linux** környezetben jönnek. Aki tehát a teljesítményt ki akarja csavarni az utolsó cseppig, annak ezzel a gondolattal barátkozni kell. Szerencsére [az ASP.NET fejlesztés multiplatform eredményt is hozhat](https://app.netacademia.hu/Tanfolyam/2018csharpalapok-c-alapok-2018-a-multiplatform-c), így egy windows fejlesztő számára is abszolút elérhető közelségbe kerül ez a lehetőség.

Ajánlom tehát az eredeti cikket, és a teszteket, rengeteg érdekesség vár még felfedezésre.

[ASP.NET Core: Saturating 10GbE at 7+ million request/s](https://www.ageofascent.com/2019/02/04/asp-net-core-saturating-10gbe-at-7-million-requests-per-second/)