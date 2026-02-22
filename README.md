# Totetuskuvaus


Jaoin kaikki vaaditut osat omiin sivuihinsa, sillä ensimmäinen versio jossa kaikki olivat päällekkäin oli vaikeaa korjata järkevästi.

eli tämän hetkinen rakenne on:

```
/ (root)
 ├── index.html        (etusivu + karuselli)
 ├── grid.html         (ruudukko)
 ├── cards.html        (kortit)
 ├── accordion.html    (haitari)
 ├── table.html        (taulukko)
 └── assets/
       └── style.css   (tyyli)
```
Näin ne kaikki ovat helposti muokattavissa ja ylläpidettävissä. Koodin luku on myös helpompaa.

Toistuvuuden kannalta, käytin suuresti lähteinäni aikaisempia luomiani verkkosivuja ja toisen toteutuksen verkkosivua jonka olin luonut.

En paljoa hyödyntänyt kurssilla listattuja materiaaleja, vaan etsin paljonkin tietoa tutuista sivuista, kuten getbootstrap.com ja w3schools.com. 

- https://www.w3schools.com/bootstrap5/bootstrap_dropdowns.php
- https://getbootstrap.com/docs/5.3/getting-started/introduction/
- Zed Dev Inline Assistant (Tekoäly)

---

## Index.html

Sivun ensimmäinen osa on etusivu, jossa on karusseli, joka näyttää erilaisia kuvia. Karusselin avulla käyttäjä voi selata erilaisia sisältöä helposti.

Loin sivulle aluksi nav-baarin seuraten kurssin ohjeita, ja en paljoa lähtenyt sitä muokkamaan.

Karusellin loin seuraten w3schools.com ohjeita bootstrapin käytöstä, koska minulla ei ollut lukittua aihetta niin käytin picsum.photos sivuilta satunnaisia kuvia, eli kuvat eivät ole tallennettu lokaalisti repositorioon.

Lisäominaisuutena tahdoin lisätä myös "toast"-ilmoituksen sivulle kun sen avaa.

Toast-ilmoituksen lisääminen onnistuu simppelisti:

```
<div class="position-fixed bottom-0 end-0 p-3" style="z-index: 11">
    <div id="toast" class="toast show">
        <div class="toast-header">
            <strong class="me-auto">Ilmoitus</strong>
            <small>nyt</small>
            <button class="btn-close" data-bs-dismiss="toast"></button>
        </div>
        <div class="toast-body">
            Tervetuloa! Sivulla ei tällä hetkellä ole tarkkaa teemaa,
            niin kuvat vaihtuvat satunnaisesti.
            <br />
            (Tämä on lisäämäni toiminto, joka lisää tekstiä ilmoituksen
            eli "toastin" sisälle.)
        </div>
    </div>
</div>
```
