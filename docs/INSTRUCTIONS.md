

# Progressive Enhancement

Een oefening in het ontwerpen en bouwen van UI components volgens het principe van Progressive Enhancement

In het college _S09W2-01-Progressive-Enhancement_ wordt behandeld wat Progressive Enhancement is, en wordt deze deeltaak uitgelegd.



## Doel van deze opdracht

Één van de mooiste [principes](https://www.w3.org/DesignIssues/Principles.html) van het web is dat iedereen met een computer en een browser het web kan gebruiken. [Het web is voor iedereen](https://www.youtube.com/watch?v=UMNFehJIi0E). 

Maar het web is geen gecontroleerde (programmeer) omgeving. Je kan er gerust van uit gaan dat niemand precies hetzelfde te zien krijgt als wat jij in je browser ziet. Er zijn technische beperkingen, zoals afmetingen van de browser, type van de browser, versie van de browser, combinatie van browser extensies, grootte van het apparaat, manier van interactie, kwaliteit van de hardware, en kwaliteit van het netwerk. En er zijn mensen, allemaal verschillende mensen...

Het doel van deze opdracht is te leren hoe je een website kan ontwerpen en maken met behulp van _Progressive Enhancement_ zodat het voor iedereen _toegankelijk_ is.

### Progressive enhancement

Progressive Enhancement is een _strategie voor ontwerpen en coderen_, waarmee je er voor kunt zorgen dat je website het altijd doet, voor iedereen.
Bouw een website op in lagen, zodat een browser kan 'terug vallen' naar een werkende versie als een CSS- of JS-techniek niet wordt ondersteund: 

1) Bepaal eerst de _core functionality_ van wat je gaat maken
2) Bouw die functionaliteit met de _simpelste techniek_ (meestal HTML, met een klein beetje One Column Mobile First CSS voor de huisstijl)
3) Voeg daarna _extra enhancements_ toe met CSS en client-side JS, om de User Experience te verbeteren (de leukste stap!)

![image](https://github.com/fdnd-task/progressive-enhancement/assets/1391509/f6d0490b-6748-4fc8-8a63-d33d2f2d0b68)
<br><small>_The skateboard may be a little slower, but it doesn’t stop the user getting to where they want to go. So, if the user’s browser doesn’t support JavaScript or modern CSS then it doesn’t break_ - Andy Bell
</small>



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

1. Maak een _issue_ met als titel het UI component. Beschrijf in de _description_ in eigen woorden wat dit component is, wat de _core functionaliteit_ is en wat de enhancement(s) is/zijn. Gebruik de demo video om een idee te krijgen. Schets het component en de interactie.
2. Onderzoek welke HTML je voor de _core functionaliteit_ nodig hebt, maak hiervan een breakdownschets, en codeer je HTML met minimale CSS voor de huisstijl. Gebruik de hints en de content in de code die klaarstaat, en de bronnen hieronder. Koppel je commits aan je issue. Test deze simpele versie op verschillende browsers en devices, via GitHub Pages.
3. Voeg eventueel meer CSS & JS _enhancements_ toe, aan de hand van de bronnen en coding strategieën hieronder. Test deze “enhanced” versie(s) op verschillende browsers en devices.

<!--
### Strategiën voor verschillende enhancements

- Met @supports (background-clip: text)
- Feature detection in JS (<button hidden> + feature detect + button.hidden=false)
- Door HTML goed op te bouwen (<video src=video.mp4><a href=video.mp4>Download video</a></video>)
- Door ok te zijn met verschillen in browsers (zoals high def color -> op een Kindle sowieso geen kleur)
- Met een polyfill (invoker commands)
- Door een goede one column layout (nesting, custom props?)
- Door “progressive enhancement”
-->

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


## Criteria

Deze opdracht is done als:

<!--
UI Events DOD:
“Je hebt de 11 basis interacties stap voor stap voltooid, en je voortgang, breakdown schetsen en testresultaten zijn in issues opgenomen.”

Nieuwe DOD's:
- [ ] Je hebt alle user interface componenten stap voor stap voltooid, en je voortgang, analyse, gesignaleerde knelpunten, schetsen en testresultaten in issues opgenomen
- [ ] Je hebt per component eerst de core functionaliteit en vervolgens de enhancement(s) beschreven in de analyse van je issue
- [ ] Je hebt per component één of meerdere strategieën voor Progressive Enhancement gecombineerd en deze uitgelegd in je issue
- [ ] Je hebt per component getest op meerdere browsers en devices en je kunt verschillen verklaren en begrijpelijk overbrengen in je issue
-->

- [ ] Je hebt minstens drie user interface componenten stap voor stap in een _issue_ gedocumenteerd en uitgewerkt in code
- [ ] De breakdownschetsen zijn opgenomen in het issue
- [ ] Bij elke schets staat een korte uitleg van de code
- [ ] Je werk is te bekijken via GitHub Pages

