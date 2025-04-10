3. Alapvető grafikai algoritmusok
=================================

A következőkben az algoritmusoknál raszteres megjelenítőt feltételezünk. Ezeknél a képernyőn megjelenített adatok valamilyen képmátrixba, videómemóriába kerülnek.

* Ez egy kétdimenziós tömb.
* A tömbben lévő értékek mutatják, hogy milyen színű legyen az adott képpont.

A jellegzetes geometriai alkazataink folytonosak, a raszterizálás viszont diszkrét és véges. A raszterzilásra tekinthetünk úgy, mint egy mintavételezési folyamatra.

Gyakorlati szempontból problémát jelent, hogy különböző konvenciók vannak a koordináták megadásához.

* Geometriai jelölésrendszert feltételezve a vízszintes tengely az :math:`x`, a függőleges tengely az :math:`y`. Az :math:`x` érték balról-jobbra, az :math:`y` érték pedig lenntről felfelé szokott növekedni.
* Lineáris algebra és numerikus módszerek kapcsán a mátrixot sor és oszlop szerint szokás indexelni.
* A grafikus megjelenítő eszközöknél az origó a bal felső sarokban szokott lenni. Az :math:`x` érték balról-jobbra nő, az :math:`y` érték fenntről-lefelé.

Rajzoló algoritmusok
--------------------

Az egyszerűbb elemektől a bonyolultabbak felé kerülnek bemutatásra az algoritmusok.

Pontok
~~~~~~

Egy pontot adott raszteres megjelenítőn a képmátrix megfelelő értékének az átállításával lehet megjeleníteni.

* A képpontonkénti elérés nem feltétlenül hatékony.
* A videómemóriához nincs mindig közvetlen hozzáférésünk.
* Bizonyos rendszerek a pontoknak is definiálnak vastagságot, így gyakorlatilag négyzetként vagy körlapként jelenítik meg azokat.

Téglalapok
~~~~~~~~~~

A téglalapoknak egy speciális esetéről lesz szó, amelyeknél

* az oldalak párhuzamosak a tengelyekkel, és
* a téglalap egész képpontokat fed csak le.

Szakaszok rajzolása, élsimítás
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A raszteres képernyő véges, ezért egyenesek helyett inkább csak szakaszok rajzolásáról beszélhetünk.

A szakasz rajzolásához a legegyszerűbb megoldás a DDA.

A Bresenham algoritmus ennél egy hatékonyabb megoldást ad.

* https://en.wikipedia.org/wiki/Digital_differential_analyzer_(graphics_algorithm)
* https://en.wikipedia.org/wiki/Bresenham%27s_line_algorithm

Háromszög kitöltés
~~~~~~~~~~~~~~~~~~

* *Triangle Rasterization*
* A kitöltött háromszöget megjeleníthetjük úgy, mint közvetlenül egymás alá rajzolt vízszintes szakaszokat.

Kör, ellipszis rajzolása
~~~~~~~~~~~~~~~~~~~~~~~~

A kört és az ellipszist is sokszögként közelíthetjük.

A háromszögekhez hasonlóan egymás alá rajzolt szakaszokként jeleníthetjük meg a kitöltött alakzatot.

Képelemek vágása
~~~~~~~~~~~~~~~~

Szakaszmetsző eljárások

Cohen-Sutherland algoritmus

* Danny Cohen, Ivan Sutherland

* https://en.wikipedia.org/wiki/Line_clipping#Fast_clipping
* https://en.wikipedia.org/wiki/Cohen%E2%80%93Sutherland_algorithm

Poligonok vágása

* https://en.wikipedia.org/wiki/Sutherland%E2%80%93Hodgman_algorithm

Floodfill algoritmus
~~~~~~~~~~~~~~~~~~~~

* https://en.wikipedia.org/wiki/Flood_fill

Szoftveres eszközök
-------------------

GUI toolkit-ek
~~~~~~~~~~~~~~

* Graphical User Interface
* *Widget*: *Window Gadget*

* Windows API
* GTK
* KDE
* Java Swing

* https://en.wikipedia.org/wiki/List_of_widget_toolkits

Grafikus függvénykönyvtárak
~~~~~~~~~~~~~~~~~~~~~~~~~~~

* HTML5 Canvas API
* https://en.wikipedia.org/wiki/Category:Graphics_libraries

[] 2D rajzoló API-k összehasonlítása

OpenGL, DirectX, Vulkan

* 2D-s megjelenítésre is alkalmasak.
* Később kerülnek még részletezésre.

Esemény- és programvezérelt programozás
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Az alkalmazásunk szempontjából eseményeknek tekinthetjük például az alábbiakat:

* billentyűzet esemény,
* egér esemény,
* időzítő esemény,
* hálózati kérésre adott válasz esemény.

Aszinkron eseményekről van szó.

* Az eseményvezérelt programozás azt jelenti, hogy a programban végrehajtandó műveleteket bizonyos eseményekhez rendeljük.
* Programvezérelt esetben a programkódunkban kell azt (szinkron módon) vizsgálni, hogy következett-e be esemény.

Interaktív grafikus felületek kialakítása
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A programunkban be- és kimenet kezelésére egyaránt szükség van.

A különféle (hardveres vagy grafikus elemekhez kötött) vezérlők segítségével interakcióba tudunk lépni a virtuális terünk elemeivel.

SDL2
~~~~

* https://www.libsdl.org/

Kérdések
========

Feladatok
=========

