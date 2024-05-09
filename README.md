>[!TIP]
>new Date()
>`dar JS new Date in 1 constructor mebowad ki data vaqt second millisecondro bo vositai xamon dar JS mesozan возвращает объект даты с текущей датой и временем.`
>`i new dat method dora`

>`Kak poluchit' tekushchuyu datu v JavaScript

V JavaScript my mozhem legko poluchit' tekushchuyu datu ili vremya, ispol'zuya novyy ob"yekt Date(). Po umolchaniyu on ispol'zuyet chasovoy poyas nashego brauzera i otobrazhayet datu v vide polnotekstovoy stroki, naprimer «Pt, 17 iyunya 2022 g., 10:54:59 GMT+0100 (britanskoye letneye vremya)», kotoraya soderzhit tekushchuyu datu, vremya i vremya. zona.
``` js
konstantnaya data = novaya data();
console.log(data); // Pt, 17 iyunya 2022 g., 11:27:28 GMT+0100 (britanskoye letneye vremya)
```
>`Davayte posmotrim, kak mozhno izvlech' iz etoy dlinnoy stroki tol'ko datu. My sdelayem yego boleye chitabel'nym i ponyatnym dlya pol'zovateley, ispol'zuya nekotoryye metody JavaScript, kotoryye rabotayut s ob"yektom daty.Kak ispol'zovat' metody daty v JavaScript`

#### Ob"yekt date podderzhivayet mnozhestvo metodov daty, no dlya etoy stat'i nam nuzhna tol'ko tekushchaya data, i my budem ispol'zovat' tol'ko tri metoda:
``` js
getFullYear() — my budem ispol'zovat' etot metod, chtoby poluchit' god v vide chetyrekhznachnogo chisla (gggg), naprimer 2022.
```
``` js
getMonth() — poluchayet mesyats v vide chisla (0–11), naprimer 2 dlya marta, poskol'ku eto indeks, nachinayushchiysya s nulya (to yest' on nachinayetsya s 0).
```
``` js
getDate() – poluchayet den' v vide chisla (1-31).
```
>`Davayte teper' ob"yedinim vse eto v zavisimosti ot formata, v kotorom my khotim, chtoby nasha data otobrazhalas':`
``` js
konstantnaya data = novaya data();
```
``` js
pust' den' = date.getDate();
pust' mesyats = ​​date.getMonth() + 1;
pust' god = date.getFullYear();
```
``` js
// Eto raspolozheniye mozhno izmenit' v zavisimosti ot togo, kakoy format daty my khotim videt'.
let currentDate = `${day}-${mesyats}-${god}`;
console.log(currentDate); // "17.06.2022"
```
>`Primechaniye. My dobavili yedinitsu k znacheniyu date.getMonth(), poskol'ku indeksatsiya nachinayetsya s 0. Predpolozhim, my ne khotim ispol'zovat' tire (-) mezhdu znacheniyami dat. Vse, chto nam nuzhno sdelat', eto zamenit' tire tem, chto my predpochitayem.
Kak ispol'zovat' metod toJSON()`

>~~My tol'ko chto uvideli, kak poluchit' tekushchuyu datu s pomoshch'yu metodov date. Teper' davayte posmotrim, kak ispol'zovat' metod toJSON(), kotoryy vozvrashchayet datu v formate gggg-mm-dd v dopolneniye k formatu vremeni chch:mm:ss.ms.~~
``` js
pust' data = novaya data().toJSON();
console.log(data); // 2022-06-17T11:06:50.369Z
```
`Poskol'ku nam nuzhna tol'ko tekushchaya data, my mozhem ispol'zovat' metod sreza() takim obrazom, chtoby poluchit' pervyye 10 simvolov:`

`pust' currentDate = novaya data().toJSON().slice(0, 10);
console.log(currentDate); // "17.06.2022"`

`Kak ispol'zovat'` 
#### toLocaleDateString()

`Eto yeshche odin prostoy metod, kotoryy vozvrashchayet ob"yekt daty v vide stroki s ispol'zovaniyem mestnykh soglasheniy. Naprimer, format daty razlichayetsya v zavisimosti ot yazyka, i etot metod prinimayet argument dlya ispravleniya etogo.`



#### Nachnem s peredachi argumenta:

#### pust' 
``` js
data = novaya data().toLocaleDateString();
console.log(data); // 17.06.2022
```
## Predpolozhim, nam nuzhno vremya v Germanii:
``` js
let date = new Date().toLocaleDateString("de-DE");
console.log(data); // 17.6.2022
```
>Primechaniye. Zdes' my mozhem poluchit' spisok vsekh kodov lokali.
Kak ispol'zovat' Moment.js

`Moment.js — odin iz samykh populyarnykh paketov dat, dostupnykh kazhdomu, i my takzhe mozhem ispol'zovat' yego dlya polucheniya tekushchey daty.`
Yesli v vashem proyekte ustanovlen Moment.js, vse, chto vam nuzhno sdelat', eto poluchit' tekushchuyu datu sleduyushchim obrazom:
```js
var data = moment ();
```
``` js
var currentDate = date.format('D/MM/GGGG');
console.log(currentDate); // "17.06.2022"
```
>My takzhe mozhem manipulirovat' im v zavisimosti ot togo, kakoy format daty my khotim videt'.


# Set in js
>[!TIP]
>`Nabory s pomoshyu set mi mozhem lekin iyo metonan danie lyuboi tipa qabul knan v kachestve vallues i esli povtorni wava i metona 1 giwa qabul kunad tamom va in misli object ast`
``` js
let a = new Set([1, 2, 3]);
let b = new Map([
  [1, "one"],
  [2, "two"],
  [4, "four"],
]);
console.log(a.union(b)); // Set(4) {1, 2, 3, 4}
```
`i eto imeet ~~key~~ i ~~vallue~~  kak i normalniy ~~object~~ no kak i my skazali vishe ono mozhet prinyat lyuboi tip v kachestve klyucha ya imeyu v vidu ili eto nachnyotsa s bukvi -minusovoi sifri ili symbol kak 👍 -eto`


``` js
let set1 = new Set([1, 2, 3, 4, 5]);

console.log(set1.has(1));
// Expected output: true

console.log(set1.has(5));
// Expected output: true

console.log(set1.has(6));
// Expected output: false
```

> i vot odin primer kak mi mozhem zabrat vallue s etogo masiva set mi ispolzuem ~~set~~
``` js
let mySet = new Set();
mySet.add(1); // Set [ 1 ]
```
>a spomoshyu add mi dobovlyaem chto to

![vv](./vv)
i v etom set est svoista kak i v objecte 