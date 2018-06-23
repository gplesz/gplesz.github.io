---
layout: post
title: önkéntes IT angyal kerestetik :)
categories: hírek
---

A [NetAcademia blog-on](http://netacademia.blog.hu/) az elmúlt hónapokban [folytatásokban lefordítottuk](http://netacademia.blog.hu/tags/12FactorApp) a következő cikkgyűjteményt: The Twelve-Factor App. Ez egy kikristályosodott szabályrendszer arról, hogyan érdemes alkalmazást fejleszteni és üzemeltetni a 21. században. Azért lehet érdekes, mert a szerzők a [Heroku-nál](https://12factor.net/) több százezer alkalmazás üzemeltetésében és több száz alkalmazás fejlesztésében vettek részt, így komoly tapasztalattal rendelkeznek.

Tapasztalatuk rengeteg féle alkalmazás hosszú éveken át történő fejlesztéséből, telepítéséből és üzemeltetéséből származik. Meglátásom szerint **minden szava aranyat ér**.

Ír például a [szoftver-pusztulás](https://en.wikipedia.org/wiki/Software_rot) fogalmáról, ami konyhanyelven szólva annyit jelent, hogy egy változatlan alkalmazás az idő múlásával a szükségszerűen változó környzetben (új OS kiadások, patch-ek, új hardverre költözés, új könyvtárba költöztetés, stb. stb.) évek vagy évtizedek alatt, egy idő után korszerűtlen, majd elavult, majd működésképtelen lesz. Mivel ez elkerülhetetlen, ezért az egy fontos kérdés, hogy lehet-e, és ha igen, akkor mit lehet tenni már a fejlesztés előtt/alatt, hogy ez a hatás lehetőleg minél hosszabb idő alatt alakuljon ki? **Nagyon nem mindegy, hogy évekről vagy évtizedekről beszélünk ugyanis**.

Ez csak egy példa volt, hogy ez a 12 szempont milyen meghatározó lehet egy alkalmazás életciklusában. Sok-sok nemtriviális gondolat van benne, és egy jól járható irányt jelentenek a jövőre nézve. Tekinthetünk rá szabványként is: az így felépített alkalmazás a teljes életciklusa során jól meghatározott jellemzőkkel rendelkezik; olyan egyértelműen pozitív tulajdonságokkal, amikre aztán számítani is lehet ez alatt az életciklus alatt.

A szempontok fontosságát a fordításban a **tényező** kifejezés meghagyásával is szerettem volna hangsúlyozni: a szempontok **egyenként is fontosak, de** a végeredményt tekintve szorzótényezőként viselkedve **egymás hatását is sokszorozzák**. Vagy akár lenullázzák.

Ezért a pontos megértésük elengedhetetlen, és persze az is, hogy terjesszük az igét. Én magam nem vagyok natív angol, ezért aztán lefordítottam az anyanyelvemre, hogy **tényleg pontosan értsem a gondolatokat**.

És hogy miért írom most ezt itt? Máris mondom.

[A fordítást elküldtem a szerzőknek](https://github.com/heroku/12factor/pull/180), hogy nekik is meglegyen a magyar fordítás. Ha valaki esetleg nem a NetAcademia blogon fut bele, hanem az eredetit nézi, talán könnyebbséget jelent, ha ott van magyar fordítás.

Ahhoz, viszont, hogy a fordítás kikerüljön a **[12factor.net](12factor.net)** oldalra, kell még legalább egy független szerkesztő/ellenőrző/áttekintő személy, aki a fordításom ellenőrzi, sajnálatos módon natív magyar kolléga náluk ebben a csoportban nem dolgozik.

Tehát. Aki a github-on eligazodik, tud angolul és van kedve önkéntes munkával a magyar nyelvű IT közösséget szolgálni, kérem nézzen rá a [pull request-emre](https://github.com/heroku/12factor/pull/180), és csináljon egy review-t. Bármilyen visszajelzésnek örülök!