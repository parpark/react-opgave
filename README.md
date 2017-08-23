# PARKPARK ansættelsesopgave
Målet med den her opgave er at du får et indblik ind i den verden, at kode JavaScript for PARKPARK. Der forventes ikke at opgaven bliver fuldført, men at se hvordan du klarer udfordringen og hvor lang du kan nå. Hvis du kommer til samtale, vil vi kigge opgaven igennem sammen.

## Opgaven
København er Danmarks største udbyder af parkeringspladser og det er vigtigt for os at have indblik i hvilken slags parkeringer bliver fortaget der og hvordan vi kan blive større på markedet.

### User Stories

- Som bruger, kan jeg se antal parkeringer i perioden
- Som bruger, kan jeg se hvor mange parkeringer er fortaget per parkeringsselskab (udbyder)
- Som bruger, kan jeg se liste over parkeringer med udbyder, tidspunkt og koordinater
- Som bruger, kan jeg filtrere liste (og/eller kort) efter udbyder

#### Ekstra point
- Som bruger, kan jeg se parkeringer på et kort
    - Som bruger, kan jeg se hvilken udbyder har parkeringen udfra farve på kortet.
- Cache dataen, sådan at du ikke spørger kk.dk hver gang.
- Filtrer datasættet, sådan at vi ikke gemmer data, som vi ikke bruger.
- Indfør lidt CSS (med eller uden framework)
- Brug Git. I stedet for at sende os en zip fil, send os en Github link.

## Før du starter

- Læs en React tutorial (for eksempel: https://facebook.github.io/react/tutorial/tutorial.html)
- Installerer Node.js på din computer: https://nodejs.org/en/
- Installerer `create-react-app`: https://github.com/facebookincubator/create-react-app
- Lav et projekt: `create-react-app min-fine-opgave`
- Åben mappen i din kode-editor. Hvis du mangler en, kan vi anbafale:
    - Visual Studio Code (https://code.visualstudio.com/)
    - Atom (https://atom.io).

## Tips

- Du kan bruge `componentDidMount()` metoden på din komponent for at hente data og sætte til state med `this.setState()`. Du kan også bruge state-managers, så som Redux eller mobX.
- Københavns dataset er her: `http://data.kk.dk/parking/latest/50` og dokumentationen her: `http://data.kk.dk/dataset/parkeringstilladelser-parking-rights`.
- Vi anvender moderne JavaScript, så der er tilladt at bruge ES2017 funktioner. Classic JS er også fint.
- Der forventes at du kan anvende søgemaskiner for at finde frem til en løsning.
- Du må gerne bruge libraries som du har lyst til.
- Du kan bruge `fetch()` til at hente data fra server. Eksempel:
```javascript
// https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch
class ExampleComponent extends React.Component {
    state: {
        parkingData: null
    }
    componentDidMount () {
        fetch('http://data.kk.dk/parking/latest/50')
        .then((response) => response.json())
        .then((json) => {
            this.setState({ parkingData: json })
        })
        .catch((err) => {
            // Handle error
        })
    }

    render () {
        return (
            // Render logic
        )
    }
}
```

## Kontakt

Finder du fejl i opgaven, eller har spørgsmål, kan du kontakte Andri Óskarsson på <ao@parkpark.dk>.
