# CORS ongelmien korjaaminen
Jotkin avoimet rajapinnat aiheuttavat selaimessa [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS/Errors)-virheitä. Ne voidaan ohittaa käyttämällä välityspalvelinta kuten esim. allOrigins: 
https://allorigins.win/

### Ohje:
   1. Lisää ennen fetch-komentoa muuttuja: `const proxy = 'https://api.allorigins.win/get?url=';`
   2. Lisää em rivin jälkeen toinen muuttuja, johon tallennat rajapinnan osoitteen parametreineen: `const haku = https://open-api.myhelsinki.fi/jne......';`
   3. Yhdistetään edelliset: `const url = proxy + encodeURIComponent(haku);`
   4. Tehdään haku: `fetch(url).then(jne....`
