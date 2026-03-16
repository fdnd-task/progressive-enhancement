

# Progressive Enhancement

Een oefening in het ontwerpen en bouwen van UI components volgens het principe van Progressive Enhancement

In het college _S09W2-01-Progressive-Enhancement_ wordt behandeld wat Progressive Enhancement is, en wordt deze deeltaak uitgelegd.



## Doel van deze opdracht

Één van de mooiste [principes](https://www.w3.org/DesignIssues/Principles.html) van het web is dat iedereen met een computer en een browser het web kan gebruiken. [Het web is voor iedereen](https://www.w3.org/mission/). 

Maar het web is geen gecontroleerde (programmeer) omgeving. Je kan er gerust van uit gaan dat niemand precies hetzelfde te zien krijgt als wat jij in je browser ziet. Er zijn technische beperkingen, zoals afmetingen van de browser, type van de browser, versie van de browser, combinatie van browser extensies, grootte van het apparaat, manier van interactie, kwaliteit van de hardware, en kwaliteit van het netwerk. En er zijn mensen, allemaal verschillende mensen...

Het doel van deze opdracht is te leren hoe je een website kan ontwerpen en maken met behulp van _Progressive Enhancement_ zodat het voor iedereen _toegankelijk_ is.

### Progressive enhancement

Progressive Enhancement is een _strategie voor ontwerpen en coderen_, waarmee je er voor kunt zorgen dat je website het altijd doet, voor iedereen.
Bouw een website op in lagen, zodat een browser kan 'terugvallen' naar een werkende versie als een CSS- of JS-techniek niet wordt ondersteund: 

<!--
1) Bepaal eerst de _core functionality_ van wat je gaat maken
2) Bouw die functionaliteit met de _simpelste techniek_ (meestal HTML, met een klein beetje One Column Mobile First CSS voor de huisstijl)
3) Voeg daarna _extra enhancements_ toe met CSS en client-side JS, om de User Experience te verbeteren (de leukste stap!)
-->
1) Bouw de functionaliteit robuust, met de simpelste techniek​ (HTML en Server-Side Rendering)​
2) Voeg basic CSS voor de huisstijl toe​
3) Enhance de functionaliteit _geleidelijk_ voor een betere User Experience​ (De leukste stap. Moderne CSS en client-side JS.)​


## Aanpak

Voor deze opdracht ga je een aantal UI componenten ontwerpen, bouwen en testen in verschillende lagen, volgens het principe van _Progressive Enhancement_. 

Fork deze leertaak en ga aan de slag met de [files die klaar staan](https://fdnd-task.github.io/progressive-enhancement/).

Voor elk component staat een HTML-file klaar met een demo video van het eindresultaat. 
In de HTML van elk component staan wat hints en content die je nodig hebt.

### UI componenten

Maak in Sprint 9, 10 en 11 alle user interface componenten: 

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

1. Maak een _issue_ met als titel het UI component. Beschrijf in de _description_ in eigen woorden wat dit component _eigenlijk_ is. Gebruik de demo video om een idee te krijgen, maar laat je niet afleiden door hoe het er uit ziet. Schets het component en de interactie.
2. Onderzoek welke HTML je nodig hebt om dit component _robuust_ neer te zetten, maak hiervan een breakdownschets, en codeer je HTML met minimale CSS voor de huisstijl. Gebruik de hints en de content in de code die klaarstaat, en de bronnen hieronder. Koppel je commits aan je issue. Test deze simpele versie op verschillende browsers en devices, via GitHub Pages.
3. Voeg eventueel geleidelijk meer CSS & JS _enhancements_ toe, aan de hand van de bronnen en coding strategieën hieronder. Test deze “enhanced” versie(s) op verschillende browsers en devices.

### Strategiën en voorbeelden voor verschillende enhancements (TODO: Lijst nog uitwerken en verduidelijken)

- Met @supports (background-clip: text)
- Door de cascade goed te gebruiken
- Feature detection in JS (`<button hidden>` + feature detect + button.hidden=false)
- Door HTML goed op te bouwen (`<video src=video.mp4><a href=video.mp4>Download video</a></video>`)
- Door nieuwe features in HTML (responsive images volgorde/opt-in)
- Door ok te zijn met verschillen in browsers (zoals high def color -> op een Kindle sowieso geen kleur)
- Met een polyfill (invoker commands)
- Door een goede one column layout (nesting, custom props?)
- Door “progressive enhancement” (duh)
- Media queries / user preference media features
- Container queries
- View Transitions

<!--
#### Voor Sprint 11
11. In Sprint 11 is het doel pleasurable (ga lekker los).
12. Documenteer je experiment.
-->

### Bronnen

- [@supports in CSS @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@supports)
- [Implementing feature detection @ MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Testing/Feature_detection)
- [Progressive Enhancement @ MDN](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement)
- [Progressive Enhancement Resources](https://github.com/voorhoede/progressive-enhancement-resources)


### Inspiratie

- [Styling & Customizing File Inputs the Smart Way](https://tympanus.net/codrops/2015/09/15/styling-customizing-file-inputs-smart-way/)
- [It All Starts with a Humble `<textarea>`](https://24ways.org/2019/it-all-starts-with-a-humble-textarea/)
- [Making a Better Custom Select Element](https://24ways.org/2019/making-a-better-custom-select-element/)
- [Progressive Enhancement and Data Visualizations](https://css-tricks.com/progressive-enhancement-data-visualizations/)


## Definitions of Done

Deze opdracht is done als:

- [ ] Je hebt alle user interface componenten stap voor stap voltooid, en je voortgang, analyse, gesignaleerde knelpunten, schetsen en testresultaten in issues opgenomen
- [ ] Je hebt per component de functionaliteit beschreven en robuuste HTML geschreven
- [ ] Je hebt per component één of meerdere strategieën voor Progressive Enhancement gecombineerd en deze uitgelegd in je issue
- [ ] Je hebt per component getest op meerdere browsers en devices en je kunt verschillen verklaren en begrijpelijk overbrengen in je issue
