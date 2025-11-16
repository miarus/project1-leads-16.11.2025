P1-LEADS/
  node_modules/      ← kirjastot joita npm asentaa (ei muokata)
  public/            ← selaimelle näkyvät tiedostot
    ├─ index.html    ← sivun rakenne (lomake, taulukko)
    ├─ app.js        ← selaimen JavaScript (toiminnallisuus)
    └─ styles.css    ← ulkoasu (väritys, fontit, layout)
  leads.json         ← sovelluksen "tietokanta" (JSON-muotoinen tiedosto)
  server.js          ← Node/Express-palvelin (sovelluksen aivot)
  package.json       ← kuvaa projektia ja kertoo mitä paketit tarvitaan
  package-lock.json  ← lukitsee tarkat paketiversiot (automaattinen)


# Micro CRM Leads (Project 1)

## Live Deployment
Live: YOUR_RENDER_URL // https://project1-leads-16-11-2025.onrender.com/

## Run Locally

### Setup Instructions
npm install // Installs all project dependencies defined in the package.json file.
npm start // Executes the "start" script defined in package.json (e.g., node server.js).
Open http://localhost:3000/ // Instructs the user where to access the application in their browser.

## Features
- Create and list leads
- Filter by status and search by name or company





  app.js on frontendin logiikka- kaivetaan lomakkeen tiedot, lähetetään palvelimelle, haetaan 
  dataa serveriltä, luodaa html- rivejä taulukkoon. 

  server.s on backend. Expressin laitto, API-reiti (get, post, patch), datan validointi,
  tiedoston käsittely ( leads.json) 
  NPM-kirjastot Express - tuo valmiina http- palvelimen toiminallisuuden, reittien luontimetodit
  ( app.get, app.post), json ja lomakeparserit, staattisen tiedostopalvelimen. 
  >>mutta on päätettävä mitä reittejä on, mitä dataa niillä on. Eli highway ja kartasto edessä,
  tehtävä valinnat. 

  express: valmis runko, seinät ja perusta
  HTML: piirustukset visuuun
  CSS: sisustus ja maalaus visuuun
  app.js: sähköt ja napit, painat ja jotain tapahtuu
  server.js = talo konehuone, aivot
  leads.json: varastohuonne, tallennehuone


  1. yhteenveeto package.json
  **package.json tekee kolme tärkeintä asiaa:**

1️⃣ Määrittelee projektin nimen ja version  
2️⃣ Kertoo, mikä tiedosto käynnistyy (`server.js`)  
3️⃣ Antaa komennot:
- `npm start` → käynnistää palvelimen Renderissä
- `npm run dev` → käynnistää palvelimen paikallisesti. 


Oma tarina:

Tässä projektissa rakensin erittäin yksinkertaisen verkkosovelluksen. Sovelluksen idea oli
se, että käyttäjä voi täyttää lomakkeen, jolla kerätään nimi ja sähköpostiosoite. Nämä tiedot
 tallennetaan listaan, ja ne voidaan näyttää takaisin käyttäjälle sivulla. Projekti koostui
 muutamasta perusosasta: HTML-sivusta, joka näyttää lomakkeen, CSS-tiedostosta, joka
 muotoilee sivun ulkoasun, JavaScript-tiedostosta selaimen puolella, ja palvelimesta, joka
 käsittelee tiedot ja tallentaa ne. Palvelin tehtiin Node.js:llä ja Express-kirjastolla.
 Lisäksi loin pienen JSON-tiedoston, johon lomakkeen tiedot tallennetaan.
Projektin aikana opin paljon aivan perusasioita siitä, miten verkkosovellus toimii kulissien
 takana. Opin esimerkiksi sen, että selaimessa näkyvä sivu ja palvelimen koodi ovat eri
 asioita, mutta ne keskustelevat keskenään. Opin myös sen, mikä on “server.js”, mikä on
 “package.json”, miksi tarvitsemme “npm install” ja miksi “node_modules”-kansiota ei saa
 lähettää GitHubiin. Lisäksi opin GitHubin ja Renderin käytöstä: miten projektin voi laittaa
  verkkoon niin, että se toimii julkisella osoitteella. Minulle tämä oli haastava, koska
  moni asia oli uutta ja termit sekavia, mutta opin lopulta käytännön kautta.
Seuraavaksi parantaisin sovellusta lisäämällä siihen esimerkiksi mahdollisuuden poistaa
tietoja tai muokata niitä. Voisin myös lisätä oikein tehdyn ulkoasun ja selkeämmän
käyttöliittymän. Tärkeintä kuitenkin on, että ymmärrän nyt perusidean siitä, miten
yksinkertainen verkkopalvelu rakennetaan alusta loppuun.



In this project, I built a very simple web application. The idea of the application was that the user can fill in a form where they enter their name and email address. This information is saved into a list, and it can also be shown back to the user on the page. The project had a few basic parts: an HTML page that displays the form, a CSS file that styles the page, a JavaScript file that runs in the browser, and a server that processes and saves the data. The server was built with Node.js and the Express library. I also created a small JSON file where the form data is stored.

During the project, I learned many basic things about how a web application works behind the scenes. For example, I learned that the page the user sees in the browser and the code running on the server are different things, but they communicate with each other. I also learned what “server.js” and “package.json” are, why we need “npm install,” and why the “node_modules” folder should not be uploaded to GitHub. I also learned how to use GitHub and Render: how to deploy a project online so that it works with a public URL. This was challenging for me because many things were new and the terms were confusing, but in the end I learned through hands-on practice.

Next, I would improve the application by adding features such as deleting or editing the saved data. I could also create a better visual design and a clearer user interface. The most important thing is that I now understand the basic idea of how to build a simple web service from start to finish.