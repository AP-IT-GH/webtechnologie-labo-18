# Labo 18

Zorg dat je de volgende folder structuur volgt:

```
webtechnologie/
├─ labo-01/
│  ├─ oefening-01/
│  │  ├─ index.html
│  │  ├─ images/
│  │  │  ├─ image-1.jpg
│  │  │  └─ image-n.jpg
│  │  ├─ css/
│  │  │   ├─ reset.css
│  │  │   └─ style.css
│  │  └─ js/
│  │     └─ script.js
│  ├─ oefening-02/
│  └─ oefening-n/
├─ labo-02/
└─ labo-n/
```

- Gebruik steeds JS modules om globale variabelen te vermijden (`<script type="module" src="./path/to/script.js"></script>`)
- Volg de [Coding Guidelines](https://apwt.gitbook.io/webtechnologie/coding-guidelines)

## Oefeningen events

### oefening 1: eerste event afhandelen

#### leerdoelen

* kennismaken met een event listener in JavaScript

#### functionele analyse

Reageer op een muisklik op een knop door een bericht in de console weer te geven.

#### technische analyse

In jouw HTML plaats je een button-element met een id, bijvoorbeeld "myAction" en wat tekst, bijvoorbeeld "Klik op mij".

In jouw JavaScript-code selecteer je deze button op basis van het id en voeg je er een event listener aan toe om te reageren op het "click"-event.

Wanneer de knop wordt geklikt, toon dan "er werd op mij geklikt" in de console.

#### voorbeeldinteractie
![voorbeeldinteractie](./voorbeeldinteractie-eerste-event.gif)

### oefening 2: reageren in DOM

#### leerdoelen

* kennismaken met een event listener in JavaScript
* DOM-manipulatie naar aanleiding van event

#### functionele analyse

Reageer op een muisklik op een knop door een bericht op de website weer te geven.

#### technische analyse

In jouw HTML plaats je een button-element met een id, bijvoorbeeld "myAction" en wat tekst, bijvoorbeeld "Klik op mij". Daaronder plaats je een p-element met een id, bijvoorbeeld "myText". Je laat de p nog leeg.

In jouw JavaScript-code selecteer je deze button op basis van het id en voeg je er een event listener aan toe om te reageren op het "click"-event.

Wanneer de knop wordt geklikt, toon dan "er werd op mij geklikt" in de p.

#### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-reageren-in-dom.gif)

### oefening 3: reageren op form event

#### leerdoelen

* form event gebruiken
* default voorkomen

#### functionele analyse

Wanneer een gebruiker het formulier verzendt, toon je de naam van de gebruiker op het scherm.

#### technische analyse

Op jouw pagina staat een formulier met daarin 1 veld, nl. "voornaam".

Wanneer de gebruiker het veld heeft ingevuld (tip: required) en het formulier verzendt, zal jouw code voorkomen dat het formulier verzonden wordt.

Je toont de ingevulde naam van de gebruiker op het scherm in een welkomstboodschap.

#### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-reageren-form-event.gif)

### oefening 4: reageren op invoer van gebruiker

#### leerdoelen

* keyboard event gebruiken

#### functionele analyse

Wanneer een gebruiker in een invoerveld typt, toon je de toetsaanslagen van de gebruiker op het scherm.

#### technische analyse

Op jouw pagina staat een invoerveld, nl. "input".

Wanneer de gebruiker iets invult, toon je de ingevulde tekst van de gebruiker op het scherm.

#### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-reageren-invoer-gebruiker.gif)

### oefening 5: reageren op muisbeweging

#### leerdoelen

* mouse event gebruiken

#### functionele analyse

Je geeft de positie van de muis weer op het scherm

#### technische analyse

Op jouw pagina staat een tekst, nl.: "Jouw muis bevindt zich op x: 150, y: 300".

Telkens de gebruiker zijn muis beweegt, toon je de nieuwe coördinaten in de tekst.

#### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-reageren-muisbeweging.gif)

### oefening 6: DOM-element toevoegen door te klikken

#### leerdoelen

* DOM manipulatie
* click event

#### functionele analyse

Je voegt lijst-items toe door op een knop te drukken.

#### technische analyse

Jouw website bestaat uit een h1 "todo-lijst" en een oplijsten van enkele to-do's.

Er staat een knop onderaan de lijst. Als op deze knop geklikt wordt, zal er een to-do-item bijkomen op de lijst.

#### voorbeeldinteractie

![voorbeeldinteractie](./voorbeeldinteractie-dom-manipulatie-na-event.gif)

### oefening 7: raad de knop

#### leerdoelen

* dynamisch DOM-elementen aanmaken en toevoegen
* event listeners toevoegen aan dynamisch aangemaakte elementen
* willekeurige getallen genereren

#### functionele analyse

Er worden 100 knoppen op de pagina geplaatst. Precies 3 ervan zijn de "juiste" knoppen. De gebruiker moet proberen deze te vinden door erop te klikken. Klikken op een juiste knop markeert hem groen en geeft feedback. Klikken op een foute knop geeft een korte rode markering. Wanneer alle 3 juiste knoppen gevonden zijn, verschijnt er een bericht.

#### technische analyse

Bij het laden van de pagina voeg je via JavaScript 100 button-elementen toe aan het element met id `buttonGrid`. Kies willekeurig 3 unieke knoppen die de "juiste" zijn en log hun nummers naar de console.

Voeg aan elke knop een click-event listener toe. Wanneer geklikt:
- Is het een juiste knop: zet `disabled` op de knop, kleur hem groen, en update de statustekst (pas een class toe, bijvoorbeeld `found`, die de groene kleur en eventuele andere stijlen bevat).
- Is het een foute knop: zet `disabled` op de knop en kleur hem rood. (pas een class toe, bijvoorbeeld `miss`, die de rode kleur en eventuele andere stijlen bevat).

Wanneer alle 3 juiste knoppen gevonden zijn, toon je een felicitatiesbericht in het element met id `status`.

#### voorbeeldinteractie
![voorbeeldinteractie](./voorbeeldinteractie-buttons.gif)

## Oefeningen events met startbestanden

- De nodige bestanden staan reeds klaar in deze repository (startbestanden-8-9)
- Kopieer deze voor elke oefening.
- In je browser zou je het volgende moeten zien als je de pagina opent: ![startbestand](./startbestand.png)

### oefening 8: formuliervalidatie

Je zal het formulier afhandelen in JavaScript.

#### functionele analyse

* Zorg dat een error-bericht wordt getoont wanneer een veld niet ingevuld is.
* Zorg dat een success-bericht wordt getoont wanneer alle velden juist ingevuld zijn met daarin de waardes van het name, email en message veld.

#### technische analyse

* Maak een bestand form.js.
* Koppel het bestand form.js aan de index.html.
* Geef het form-element een id en haal het op in je form.js met querySelector.
* Voeg een submit-eventlistener toe aan form.
* Haal de 3 velden op en kijk na of ze zijn ingevuld.
* niet ingevuld: geef een foutmelding
* ingevuld: geef een succesmelding
* Toon de ingevulde waarden aan de gebruiker via een `alert`.

#### voorbeeldinteractie

![voorbeeldinteractie](./form.gif)

![alert na submit](./form-submit.png)

### oefening 9: frequently asked questions sectie (FAQ)

#### functionele analyse

* Maak een inklapbare FAQ met behulp van JavaScript.
* Voeg HTML toe zoals visueel weergegeven in de voorbeeldinteractie.
* Elk inklapbaar element bestaat uit:
* een button met class `collapsible`
* een p-element met class `context`

#### technische analyse

* Haal in faq.js alle elementen op met de klasse 'collapsible' en gebruik hierbij querySelectorAll.
* Loop over de array van elementen.
* Voeg voor elk element een 'click' eventlistener toe.
* Als er op een ingeklapt element wordt geklikt, wordt de inhoud zichtbaar.
* Als er op een opengeklapt element wordt geklikt, wordt de inhoud onzichtbaar.

#### voorbeeldinteractie

![voorbeeldinteractie](./faq.gif)