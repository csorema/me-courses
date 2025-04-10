4. Térbeli alakzatok leképzése síkra
====================================

Az alapvető célunk jelen esetben: térbeli objektumok ábrázolása síkon.

A vetítés egy dimenzióvesztő leképzés.

* Elvész a mélységinformáció.
* A vetített képből nem tudjuk rekonstruálni az eredeti térbeli objektumot.

Mátrixos felírás

* https://en.wikipedia.org/wiki/3D_projection

Párhuzamos vetítés
------------------

Orthogonális vetítés
--------------------

Merőleges vetítés, orthografikus projekció, analemma

A párhuzamos vetítés egy alapesete.

* https://en.wikipedia.org/wiki/Oblique_projection

Mátrixos felírás

Perspektivikus vetítés
----------------------

Középpontos vetítés.
A vetítés középpontjának a szempozíciót tekintjük.

A valódi kamerákhoz képest az egyik eltérés, hogy nem általában vesszük figyelembe a lencsék torzítását.

* Izometrikus megjelenítés
* Két és fél 3D

.. TODO: Mutatni rá játékokból példákat!

OpenGL
------

Nézeti gúla

:code:`glFustrum` függvény paraméterei

Kérdések
========

Feladatok
=========

* Tegyük fel, hogy orthogonálisan szeretnénk vetíteni az :math:`(x, z)` síkra. A szempozíciónk a :math:`(3, 5, 7)` pontban van. Írja fel a vetítéshez tartozó mátrixot!
* Orthogonális vetítést feltételezünk. A térbeli :math:`(7, -1, 2)` pontot az :math:`x = 6, z = 3` pontra vetítettük le. Melyik síkra történt a vetítés? Hol volt a szempozíciónk a térben?
* Adott a :math:`(2, -8, 10)` pont a térben. Perspektivikus leképzést feltételezve hova kerül a síkon, hogy ha a szempozíciónk az origó, és a képernyősík attól 3 egység távolságra van?
* Perspektív transzformációval a :math:`(2, -8, 10)` pontot a :math:`(0.2, -0.8)` pontba képeztük le. Milyen messze van a szempozíciónk a képernyő síkjától?

