---
layout: post
title: Mondom is, miért C#
categories: cikkek
---

Tehát, szóval. **Miért is érdemes C#-ban programozni?**

Csak nagyon röviden: mert szinte minden területen, kis belépési kültséggel, azonnal működő prototípust tudunk építeni, és a határ majdnem a csillagos ég. Ráadásul a tudáshoz való hozzáférés gyakorlatilag korlátlan.

Persze, hogy mindjárt mondok példákat is, de előbb megismétlem az eddigieket kicsit hosszabban:

Tegyük fel, hogy programozni szeretnél, és azt a nyelvet keresed, amin

a.) Windows-ra, 
b.) Linuxra, 
c.) iOS-re, 
d.) Androidra, 
e.) OSX-re

1. ) szerver 
2. ) desktop 
3. ) kliens 
4. ) mobil
5. ) 2D/3D játék

alkalmazásokat írhatsz akár évtizedekig egy irányba haladva, nagy törések nélkül. Majd miután beletanultál [dolgozni is szeretnél](https://www.google.hu/search?q=c%23+programoz%C3%B3+%C3%A1ll%C3%A1s&rlz=1C1GCEA_enHU763HU763&oq=c%23+programoz%C3%B3) vele.

Akkor az a helyzet, hogy egyről beszélünk, hát ezért [CSharp](https://hu.wikipedia.org/wiki/C_Sharp).

A nyelvet 2000-ben mutatták be, eleve úgy indult, hogy a Java-hoz hasonlóan mindenhol fog majd futni, de az MS Windows környzeten kívül nagyon lassan haladt a fejlődése, mivel a Microsoft a Windows-ra koncentrálta erőit. Óriási áttörés történt viszont ebben az elmúlt években, a [Xamarin megvásárlásával](https://blogs.microsoft.com/blog/2016/02/24/microsoft-to-acquire-xamarin-and-empower-more-developers-to-build-apps-on-any-device/) és a házon belüli ASP.NET "lázadással" a nyílt forráskód irányába. Immár a felsorolt esetekben teljes értékű, első osztályú polgára a fejlesztési világnak.

Tényleg, mielőtt belevágunk: ***mi van a teljesítménnyel?***

Tudod, Microsoft..., meg a Windows... Hát, hogy is mondjam.

Ebből a legújabb [TechEmpower Framework Benchmarkból](https://twitter.com/TFBenchmarks/status/997137835361628160) egyértelműen kiderül, **az ASP.NET Core** környezet, amivel a szerveroldalon dolgozunk, **másodpercenként majdnem 7 millió kérést szolgált ki** a *plain text* versenyben, a verseny szabvány futtatókörnyezetében. Erre mondják, hogy a teljesítménymérések alfájában.

Ezzel a leggyorsabb versenyző 98.1%-os teljesítményét hozta. Vegyük észre, hogy **előtte az eredménylistán hiába keressük a nagy frameworköket**. Tényleg, aki a listán *hallott* ebben a kategóriában az ASP.NET Core előtt végző versenyzőkről, és *látott* már valamelyik használatával rendes fejlesztést, ***NetAcademia bögrét kap***.

A teljesítmény tehát köszöni szépen, alakul, alakulgat.

Akkor nézzük ezt a sok környezetet, mondjuk manapság egy kikerülhetetlen dolog az IoT, és ennek egyik kiváló csillaga, a Raspberry PI. Jó. Akkor mondjuk ezzel mi van?

Az van, hogy az elmúlt napokban kétszer is belefutottam, egyszer [Hanselmann írt egy szívhezszóló cikket](https://www.hanselman.com/blog/BuildingRunningAndTestingNETCoreAndASPNETCore21InDockerOnARaspberryPiARM32.aspx 
arról, hogy is lehet Docker segítségével Raspberry PI (ARM) architektúrán C# huszárkodni.

Aztán pedig jelezte, hogy [most lesz nemsokára (azóta már volt)](https://www.facebook.com/shanselman/posts/10155066568741618) a Twitch-en egy [9 órás igyenes demonstráció/kódolási maraton/bemutató workshop](https://www.twitch.tv/videos/262711576), ahol egyebek mellett Docker segítségével C# nyelven Raspberry PI-t ***is*** programoznak.

Na, ugye.

De miért mondtam mindezt itt el?

Mert az a helyzet, hogy mi itt Magyarországon olyan nagyon nem vagyunk lemaradva.

Mivel ezek *előtt*, 2018. április 23-án 15:00-18:00 között az [előző NetAcademia meetup-on](https://app.netacademia.hu/Tanfolyam/2018csharp-lenyugozo-c-programozas) ki nem találnád, 
de C# nyelven Docker segítségével a Raspberry PI ledjét villogtattuk. Az [eseményről készített videók](https://app.netacademia.hu/Videok/2018csharp-lenyugozo-c-programozas) ingyenesen elérhetőek mindenkinek, regisztráció után.

A jegyzőkönyv kedvéért:

- A következő alkalom 2018. június 04-én lesz, amikoris a saját gépünkön futó csevegőrobotból fogjuk ezt a kódot használni.
- Aztán pedig 2018. június 25-én kitesszük az egészet az Internetre, és akár Facebook Messengerből vagy Skype-ból is élvezhetjük munkánk gyümölcsét.
Azt pedig már el sem mondom, hogy a hónap elején elindult [NetAcademia Certified Junior C# fejlesztő útvonal](https://app.netacademia.hu/junior-csharp-developer), ha valaki hivatásszerűen szeretné megismerni a C# világát.

Régebbi C# motorosoknak pedig a szintén most indult [NetAcademia Certified Unity Developer 
útvonalról](https://app.netacademia.hu/unity-developer) nem beszélek bővebben, ami akár az előző után is elvégezhető mivel a tanfolyamokról szokásosan visszanézhető videó készül, a könnyebb elmélyülés érdekében.

Szóval tényleg csak elhatározás kérdése most rendes C# programozóvá válni:)

Azzal szeretném megköszönni, hogy idáig olvastál, hogy ha van valami ötleted, hogy mit lenne jó megvalósítani a következő NetAcademia meetup-on/meetup sorozaton, akkor vagy kommentben, vagy e-mail-en ([plesz.gabor@netacademia.hu](http://mailto:plesz.gabor@netacademia.hu)) küldd el nekem.

Ajándékként azt tudom felajánlani, hogy ha nyersz, akkor -egy bögre mellett- a soron következő meetup-on -akár együtt is, ha van hozzá kedved- megcsináljuk.