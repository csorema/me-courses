1. Koordinátarendszerek, transzformációk, színek
================================================

A számítógépi grafikában alapvetően az a cél, hogy különféle alakzatokat, különféle színekkel jelenítsünk meg. Mindkettőhöz szükségünk lesz koordinátarendszerekre, mivel ezek segítségével tudjuk számszerűsíteni azokat.

Koordinátarendszerek
--------------------

Vektor

* Rendezett :math:`n`-es. Esetünkben általában :math:`\mathbb{R}^n`.
* Az :math:`n` a tér dimenzióját adja meg.

.. admonition:: Példa

  A :math:`(1, 8, 0, -3, 7) \in \mathbb{R}^5` egy 5 dimenziós valós vektor.

Vektortér

* https://en.wikipedia.org/wiki/Vector_space

Descartes koordinátarendszer
----------------------------

A tér pontjait, mint a tengelyekhez tartozó halmazok Descartes szorzatának elemeit kezeljük.

Háromdimenziós térbeli pont esetén a jelölések.

* :math:`(x, y, z) \in \mathbb{R}^3`
* :math:`\textbf{x} = (x_1, x_2, x_3) \in \mathbb{R}^3`
* Geometriában használatos jelölés még, hogy :math:`P \in \mathbb{R}^3`, koordinátánként pedig :math:`(P_x, P_y, P_z)`.

.. warning::

  A skalárok vektoroktól való megkülönböztetéséhez nyomtatott formában (mint itt a jegyzetben is) általában félkövér betűtípust használunk. (Például az :math:`s` az egy skalár, míg a :math:`\textbf{v}` az egy vektor.) Írásban ugyanilyen célból egy nyilat szokás felé rajzolni.

Jellemzően euklideszi térben gondolkozunk.

normál vektor
-------------

A görbére, felületre merőleges vektor.

* https://mathworld.wolfram.com/NormalVector.html
* https://en.wikipedia.org/wiki/Normal_(geometry)

Speciális esete az egység hosszúságú normál vektor.

:math:`\textbf{n}`

Egyenes leírása
---------------

Az általános egyenlet explicit alakja: :math:`Ax + By + C = 0, \quad A^2 + B^2 \neq 0`.

Megadható az :math:`Ax + By = D` alakban is.

Normál vektoros egyenlet. Tegyük fel, hogy ismert egy :math:`(x_0, y_0)` pont, 

Egyenesek metszése

Merőleges vetítés

Sík leírása
-----------

Normál vektoros egyenlet

két pont távolsága

pont-egyenes távolsága

pont-sík távolsága

Homogén koordinátarendszer
--------------------------

* https://en.wikipedia.org/wiki/Homogeneous_coordinates

:math:`P = (x, y, z, w)`

A :math:`w` egy arányossági tényező.

* A Déscartes koordinátarendszerbeli pontokat a homogén koordinátarendszerbeliek részhalmazának tekintjük.
* A homogén koordinátarendszerbeli leírás nem egyértelmű. Egy Déscartes koordinátarendszerbeli pontot végtelen sok homogén koordinátarendszerbeli ponttal meg tudunk adni.
* A végtelenül távoli pontok tulajdonképpen irányokat jelölnek. Ezeknél a :math:`w` értéke 0.

A következőkben a koordinátarendszerek közötti átírási módot láthatjuk. Három dimenziós esetekre vonatkoznak, de egyszerűen általánosítható a módszer alacsonyabb és magasabb dimenzióba is.

Déscartes :math:`\rightarrow` Homogén

:math:`(x, y, z) \rightarrow (x, y, z, 1)`

Homogén :math:`\rightarrow` Déscartes

:math:`(x, y, z, w) \rightarrow \left(\dfrac{x}{w}, \dfrac{y}{w}, \dfrac{z}{w}\right)`

* Az osztás nyilván csak akkor végezhető el, hogy ha :math:`w \neq 0`.
* A :math:`w = 0` esetben beszélünk végtelenül távoli pontról, melynek nincs Déscartes koordinátarendszerbeli megfelelője.

A homogén koordinátarendszer használata tehát az alábbiak miatt előnyös.

* A pont és az egyenes reprezentációja megegyezik.
* Tudunk vele ábrázolni végtelenül távoli pontokat.
* A számítások egyszerűbben leírhatóak lesznek.

Transzformációk
---------------

A transzformációk osztályozása

Mátrixok

Egységmátrix

mátrix inverz számítása

Transzformációs mátrixok

mátrix verem

Színek
------

Színérzékelés: pálcikák, csapok

Additív színkeverés

Szubtraktív színkeverés

HSV, HSL

színterek, színmélység

Kérdések
========

* Milyen előnyei miatt használunk homogén koordináta rendszert?
* Milyen színek vannak az RGB színkocka :math:`(0, 0, 0)` és :math:`(1, 1, 1)` pontját összekötő szakaszon?

Feladatok
=========

**(1.)** Adjunk meg a :math:`(2, -1, 4)` Déscartes koordinátarendszerbeli pontnak olyan homogén koordinátarendszerbeli felírását, melyben a koordináták összege pontosan 60 értékre adódik!

Két ponton áthaladó egyenes (homogén koordinátákkal)

Két egyenes metszése (homogén koordinátákkal)

Mátrix inverz számítás

Lightness érték számítás

