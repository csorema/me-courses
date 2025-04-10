2. Grafikus kimeneti- és bemeneti eszközök
==========================================

A grafikus megjelenítő rendszerek fontos részei a ki- és bemeneti eszközök. A következőkben azt láthatjuk majd, hogy milyen változatos megoldások születtek, mi a működési elvük, milyen előnyökkel és hátrányokkal rendelkeznek.

Alapfogalmak
------------

Raszteres megjelenítés
~~~~~~~~~~~~~~~~~~~~~~

* A színeknek egy skalár vagy vektor értéket feleltetünk meg.
* Létrehozunk egy képmátrixot, amelyben tároljuk a színértékeket.
* A reprezentációs mód a rácsra nem illeszkedő alakzatoknál torzít.
* Az ábrázolás részletességét a raszter felbontása határozza meg.
* Adott raszteren a képek tárigénye megegyezik. (*A fájlformátumokról, és a tömörítésből adódó előnyökről még később lesz szó.*)
* A tengelyek mentén történő egész pixeles eltolási műveletek egyszerűek.
* A skálázás művelet abban az esetben egyszerű (hibamentesen kivitelezhető), hogy ha a középpontja rácspontra esik, és a tengelyek szerint egész értékekkel skálázunk.
* Az egyéb eltolás, skálázás és forgatás műveletek torzítást okoznak. ("okoznak" - lehet olyan kép, amelyiknél nem, de általánosságban az adott raszterhez tartozó összes lehetséges képet tekintjük.)
* https://en.wikipedia.org/wiki/Raster_graphics

Vektorgrafikus megjelenítés
~~~~~~~~~~~~~~~~~~~~~~~~~~~

* A megjelenítendő alakzatok előállítási módját írjuk le.
* Felbontásról nem szükséges beszélnünk.
* A reprezentációhoz szükséges tárigényt az alakzatok száma, azok bonyolultsága határozza meg.
* Az eltolás, skálázás és forgatás transzformációk (és a további, mátrixszal leírhatóak is) pontosan elvégezhetőek.
* https://en.wikipedia.org/wiki/Vector_graphics

.. note::

  A fájlformátumokat és a grafikus szerkesztőprogramokat is alapvetően az előbbi két csoportba szokás sorolni.

Színmélység
~~~~~~~~~~~

* Az egy képpont színének megadásához szükséges bitek száma.
* Használják még a szín egy adott csatornájához tartozó érték leírásához szükséges bitek számára is.
* :math:`k` darab bit esetén :math:`2^k` féle szín áll rendelkezésünkre. (Feltéve, hogy színes kép esetén a :math:`k` mindhárom komponenst egyidejűleg tartalmazza.)
* https://en.wikipedia.org/wiki/Color_depth

.. note::

  A *megjeleníthető színek száma* és az *egyidejűleg megjeleníthető színek száma* bizonyos esetekben eltér. Például színpaletta használatával, pixelenként 8 bittel is tudunk használni :math:`2^{24}` féle színt, azonban ezek közül egyszerre csak maximum 256 féle lehet látható.

Képfrissítési frekvencia
~~~~~~~~~~~~~~~~~~~~~~~~

* A megjelenített képek váltogatásához szükséges idő reciproka.
* Mértékegysége Hz.
* Jellemzően *Frame Rate* vagy *Frame Per Second* néven hivatkoznak rá.
* https://en.wikipedia.org/wiki/Frame_rate

Kimeneti eszközök
-----------------

A megjelenített felület lehet

* sík (jellemzően ezt preferáljuk),
* domború (technológiai korlát miatt például),
* homorú (hogy közelebbről nagyobbnak tűnjön),
* egyéb (mert képesek vagyunk rá).

A megjelenítési tartomány többségében négyzet alakú, de akadnak kivételek, például

* okosórák,
* *notch*,
* Apple Vision külső megjelenítője.

Monitorok
~~~~~~~~~

CRT monitorok

* *Cathode Ray Tube*
* https://en.wikipedia.org/wiki/Cathode-ray_tube

Vektorgrafikus megjelenítés

* Hardver szintjén is megoldható a vektorgrafikus megjelenítés.
* https://en.wikipedia.org/wiki/Vector_monitor

Raszteres megjelenítés

* Manapság ez a gyakoribb.
* Többségében RGB színkeverés történik.
* A pixelek alakja, és a csatornák elrendezése változatos.

Technológiák

* LCD: *Liquid-Crystal Display*, https://en.wikipedia.org/wiki/Liquid-crystal_display
* LED: *Light Emitting Diode*, https://en.wikipedia.org/wiki/LED_display
* IPS
* OLED
* QLED

.. warning::

  A klasszikus LCD megjelenítőknél szükség van fehér háttérvilágításra, amelyet például fehér LED-ekkel oldanak meg. Figyelni kell arra, hogy a kijelzőben a LED pontosan mire szolgál!

Projektorok
~~~~~~~~~~~

* Speciális optikával ellátott, nagy fényerejű LCD kijelzők többségében.
* Az energiafelvétel és a hűtés is probléma.
* Különféle korrekciós lehetőségek, például fókusz beállítás, trapéz korrekció.
* Az interfészét és beállítási lehetőségeit tekintve nagyon hasonlít a monitorokra.
* A megjelenítés minőségét erősen befolyásolja a vászon és a fényviszonyok.

Statikus megjelenítő eszközök
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A statikus alatt számos dolgot érthetünk. A következő részben a *statikus* azt jelenti, hogy ha a kijelzőt kikapcsoljuk, akkor a legutoljára megjelenített kép megmarad rajta.

* Analóg órák, forgatható naptár
* Buszokon, állomásokon tekerős kijelzők (kis felbontású raszteres)

eInk kijelző

* Például boltokban
* Jellemző problémája az alacsony képfrissítési frekvencia és a szellemkép (*ghosting*).
* Külső (vagy saját beépített) megvilágítást igényel. A fénynek vissza kell róla verődnie, vagy a kép hátuljának megvilágítva kell lennie.
* A 2020-as évektől kezdve már protípus szintjén kezdtek megjelenni a színes változatok.

Nyomtatók
~~~~~~~~~

Külön említésre kerülnek, de tekinthetők a statikus kijelzők egy szélsőséges esetének.

* A számítógépek elsődleges kimeneti eszközei voltak igen sokáig.
* Az operációs rendszerekben ezeknek a nyomait a mai napi felfedezhetjük, például:

.. code:: python

  print('Hello, World!')

Technológiák

* Mátrix
* Tintasugaras
* Lézer

Színes nyomtatás esetében CMYK színkeverési módszer

Plotterek

3D nyomtató

* Extruder-es
* Gyantás gyomtatás

CNC gépek

Bemeneti eszközök
-----------------

Billentyűzet
Egér

Joystick
Kontrollereken például

CRT kompatibilis pozícionáló eszköz
Például kazettás, lövöldözős játékoknál

Érintőképernyő
Multitouch

Kamera
CCD

Szkenner

Kérdések
========

* Milyen előnyei és hátrányai vannak a raszteres és a vektorgrafikus megjelenítésnek?
* Hogy ha 12 bit a színmélység, akkor hány színt tudunk használni?
* Milyen paramétereket érdemes figyelembe venni egy monitor megvásárlásánál?

Feladatok
=========

* Számítsuk ki, hogy mennyi MBit/s adatátviteli sebességre van ahhoz szükség, hogy egy 1280x1024 felbontású videófolyamot 30 FPS-sel folyamatosan küldjünk (tömörítés nélkül)!

