# Progressive Enhancement

Een oefening in het ontwerpen en bouwen van UI components volgens het principe van Progressive Enhancement

In het college _S09W2-01-Progressive-Enhancement_ wordt behandeld wat Progressive Enhancement is, en wordt deze deeltaak uitgelegd.


## Doel van deze opdracht

Één van de mooiste [principes](https://www.w3.org/DesignIssues/Principles.html) van het web is dat iedereen met een computer en een browser het web kan gebruiken. [Het web is voor iedereen](https://www.w3.org/mission/). 

Maar het web is geen gecontroleerde (programmeer) omgeving. Je kan er gerust van uit gaan dat niemand precies hetzelfde te zien krijgt als wat jij in je browser ziet. Er zijn technische beperkingen, zoals afmetingen van de browser, type van de browser engine, versie van de browser, combinatie van browser extensies, grootte van het apparaat, manier van interactie, verschillende operating systems, kwaliteit van de hardware, en kwaliteit van het netwerk. En er zijn mensen, allemaal verschillende mensen...

Het doel van deze opdracht is te leren hoe je een website kan ontwerpen en maken met behulp van _Progressive Enhancement_ zodat het voor iedereen _toegankelijk_ is.

### Progressive Enhancement

Progressive Enhancement is een _strategie voor ontwerpen en coderen_, waarmee je er voor kunt zorgen dat je website het altijd doet, voor iedereen.
Bouw een website op in lagen, zodat een browser kan 'terugvallen' naar een werkende versie als een CSS- of JS-techniek niet wordt ondersteund: 

<!--
1) Bepaal eerst de _core functionality_ van wat je gaat maken
2) Bouw die functionaliteit met de _simpelste techniek_ (meestal HTML, met een klein beetje One Column Mobile First CSS voor de huisstijl)
3) Voeg daarna _extra enhancements_ toe met CSS en client-side JS, om de User Experience te verbeteren (de leukste stap!)
-->
1) Bouw de functionaliteit robuust, met de simpelste techniek​ (HTML!)​
2) Voeg Baseline CSS voor de huisstijl toe​
3) Enhance de functionaliteit _geleidelijk_ voor een betere User Experience​ (De leukste stap. Met moderne CSS en client-side JS.)​


## Aanpak

Voor deze opdracht ga je een aantal UI componenten ontwerpen, bouwen en testen in verschillende lagen, volgens het principe van _Progressive Enhancement_. 

Fork deze leertaak en ga aan de slag met de [files die klaar staan](https://fdnd-task.github.io/progressive-enhancement/).

Voor elk component staat een HTML-file klaar met een demo video van het eindresultaat. 
In de HTML van elk component staan wat hints en content die je nodig hebt.

Maak in Sprint 9, 10 en 11 alle user interface componenten. Eke woensdag gaan we een UI component bespreken.

### UI componenten

- [Veelgestelde vragen](https://fdnd-task.github.io/progressive-enhancement/faq.html)
- [Switch control](https://fdnd-task.github.io/progressive-enhancement/switch.html)
- [Mobiel menu](https://fdnd-task.github.io/progressive-enhancement/menu.html)
- [Favorieten picker](https://fdnd-task.github.io/progressive-enhancement/pickers.html)
- [Carrousel](https://fdnd-task.github.io/progressive-enhancement/carrousel.html)
- [Rating](https://fdnd-task.github.io/progressive-enhancement/rating.html)
- [File upload met preview](https://fdnd-task.github.io/progressive-enhancement/file.html)
- [Tabbladen](https://fdnd-task.github.io/progressive-enhancement/tabs.html)

<!--
#### Voor Sprint 11

Voor Sprint 11 is het het interessantst om componenten uit je ontwerp voor de leertaak in Sprint 11 te gebruiken. 
Je mag ook componenten uit bovenstaande lijst gebruiken.
Het is een individuele opdracht - dus elke teamlid werkt eigen componenten uit (of maakt een substantieel andere uitwerking van dezelfde component).

Ieder teamlid werkt minimaal 2 componenten uit.
-->

### Aanpak (per component)

1. Maak een _issue_ met als titel het UI component. Beschrijf in de _description_ in eigen woorden wat dit component _eigenlijk_ is. Maak een breakdownschets van de interactie, en bedenk met welke _robuuste HTML_ dit kan. Gebruik de demo video om een idee te krijgen, maar laat je niet afleiden door hoe het er uit ziet.
2. Onderzoek met [CanIUse.com](https://caniuse.com/) welke Baseline CSS je nodig hebt om dit component te stylen in de huisstijl. Gebruik de hints en de content in de code die klaarstaat, en de bronnen hieronder. Koppel je commits aan je issue. Test deze simpele versie op verschillende browsers en devices, via GitHub Pages. (Je hebt hiervoor NodeJS, Express en Render niet nodig.)
3. Voeg eventueel geleidelijk meer moderne CSS & JS _enhancements_ toe, aan de hand van de bronnen en coding strategieën hieronder. Test deze “enhanced” versie(s) op verschillende browsers en devices; het is bij deze stap prima als niet elke browser dit precies hetzelfde doet. Het zijn namelijk _enhancements_, die niet per se vereist zijn.

## Strategieën en voorbeelden voor verschillende enhancements

Stap 3, de _enhancements_, doe je niet op slechts één manier. Je kunt hiervoor verschillende code strategieën gebruiken. Hieronder staan een aantal van deze manieren, met een voorbeeld. Per component heb je waarschijnlijk (een combinatie van) een aantal manieren nodig.

### De Cascade

Browsers negeren CSS values die ze niet kennen. Maak hier slim gebruik van als je bijvoorbeeld nieuwere features wilt gebruiken.

```css
body {
  color: red;
  color: color(display-p3 1 0 0);
}
```

Tip: sommige browsers en apparaten kunnen überhaupt geen kleur laten zien (denk aan e-readers), dus hou ook hier rekening mee.

### Feature detection in CSS: `@supports`

Test of een browser een bepaalde feature ondersteunt, voordat je ook _gerelateerde_ properties verandert. In dit voorbeeld maak je bijvoorbeeld _alleen_ de kleur transparant als de browser _ook_ `background-clip` ondersteunt.

```css
h1 {
  color: #A675F5;

  @supports (background-clip: text) {
    color: transparent;
    background: linear-gradient(#66E5BF, #A675F5);
    background-clip: text;
  }
}
```

### Media Queries in CSS: `@media`

Met media queries maak je een layout complexer, met bijvoorbeeld meerdere kolommen of animaties:

```css
body {
  color: #A675F5;
  @media (min-width: 40em) {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  @media (prefers-reduced-motion: no-preference) {
    opacity: 0;
    animation: --reveal 3s ease-in forwards;
  }
}
@keyframes --reveal {
  to {
    opacity: 1;
  }
}
```

### Feature detection in JS

In JavaScript kun je controleren of een bepaalde feature ondersteund wordt, voordat je deze gebruikt. Browsers die deze feature niet ondersteunen, zorgen dan niet voor een error. In dit voorbeeld wordt `document.startViewTransition` alleen gebruikt als het ook echt ondersteund wordt.

```javascript
if (document.startViewTransition) {
  document.startViewTransition(function() {
    veranderDeLayout()
  })
} else {
  veranderDeLayout()
}
```

### Verrijk UI met JS

Gebruik client-side JavaScript om een prima werkend formulier in HTML nét iets prettiger te maken. Je wilt bijvoorbeeld een filter maken waarbij de checkbox het formulier submit. Zorg dan dat je eerst HTML maakt die altijd werkt, dus met een submit button:

```html
<form method="GET" action="/filteren">
  <label>
    <input type="checkbox" name="show-all">
    Toon alles
  </label>
  <button type="submit">Filter</button>
</form>
```

En leg daar een beetje JavaScript overheen met het driestappenplan:

```javascript
let form = document.querySelector('form')
let checkbox = document.querySelector('input[type="checkbox"]')
let button = document.querySelector('button')

// Laat de checkbox het formulier submitten
checkbox.addEventListener('click', function() {
  form.submit()
})

// Verberg de knop met JavaScript, want die is nu niet meer nodig
button.hidden = true
```

Mocht er iets mis gaan, of niet ondersteund worden in JavaScript, dan valt je UI terug naar eentje mét submit button.


### Verberg UI die JS vereist

Als je client-side JavaScript voor functionaliteit gebruikt, en je hebt daar bepaalde UI elementen voor nodig, verberg deze dan eerst in je HTML. Met JavaScript kun je ze tonen. Mocht er iets mis gaan (en dat gebeurt vaker dan je denkt of hoopt), dan heeft je bezoeker in ieder geval geen knoppen die niks doen.

```html
<button id="knop" hidden>Toon volgende foto</button>
```

```javascript
let btn = document.getElementById('knop')
btn.addEventListener('click', function() {
  // Hier komt complexere code
});

// Toon de knop met JavaScript
btn.hidden = false
```

Tip: combineer _JS feature detection_ met deze patronen

### Gebruik binnen HTML zelf Progressive Enhancement

Veel features in HTML zelf zijn al _progressively enhanced_. Eén van de oudste voorbeelden hiervan is de volgende. In browsers die het `video` element niet ondersteunen, krijg je gewoon een link naar de download, zodat je de video buiten de browser kunt bekijken. Browsers die `video` wel ondersteunen, spelen die af, en laten de link niet zien.

```html
<video src="video.mp4">
  <a href="video.mp4">Download video</a>
</video>
```

Browsers negeren dus HTML elementen die ze niet kennen.

Een ander voorbeeld gaat over _Responsive Images_, waar we in Sprint 10 meer van gaan vertellen. Browsers die `picture` _en_ AVIF ondersteunen, zullen `foto.avif` downloaden. Browsers die _of_ `picture` _of_ AVIF niet kennen, zullen die delen negeren en gewoon `foto.jpg` downloaden.

```html
<picture>
  <source type="image/avif" srcset="foto.avif">
  <img src="foto.jpg">
</picture>
```

### Polyfills

Veel features zijn (tijdelijk) met JavaScript na te maken. Dit worden _polyfills_ genoemd. Het `<details>` element is bijvoorbeeld “Baseline 2024, Newly available”. Je kunt dit element dus prima gebruiken (onbekende HTML wordt genegeerd en de inhoud wordt gewoon getoond), maar misschien is het handig om er een kleine _polyfill_ bij te maken. In dit voorbeeld combineer je _feature detection_ met het driestappenplan dat je al kent:

```html
<details>
  <summary>Meer details</summary>
  <p>Door slim gebruik te maken van HTML en Progressive Enhancement,
     maak je _robuuste websites_, die het voor meer mensen doen.</p>
</details>
```

```js
if (!('open' in document.createElement('details'))) {
  var summary = document.querySelector('summary')
  var p = document.querySelector('p')
  summary.addEventListener('click', function() {
    p.hidden = !p.hidden
  })
  p.hidden = true
}
```

Browsers die het `<details>` element kennen, negeren dit stukje JavaScript. En over een paar jaar, als de ondersteuning nog wat beter is, kun je het helemaal weggooien.

## Bronnen

- [Can I Use](https://caniuse.com/)
- [Baseline (compatibility) @ MDN](https://developer.mozilla.org/en-US/docs/Glossary/Baseline/Compatibility)
- [@supports in CSS @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@supports)
- [Implementing feature detection @ MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Testing/Feature_detection)
- [Progressive Enhancement @ MDN](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement)
- [Progressive Enhancement Resources](https://github.com/voorhoede/progressive-enhancement-resources)

## Definitions of Done

Deze opdracht is done als:

- [ ] Je hebt alle user interface componenten stap voor stap voltooid, en je voortgang, analyse, gesignaleerde knelpunten, schetsen en testresultaten in issues opgenomen
- [ ] Je hebt per component de functionaliteit beschreven en robuuste HTML geschreven
- [ ] Je hebt per component één of meerdere strategieën voor Progressive Enhancement gecombineerd en deze uitgelegd in je issue
- [ ] Je hebt per component getest op meerdere browsers en devices en je kunt verschillen verklaren en begrijpelijk overbrengen in je issue
