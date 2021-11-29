# CORS ongelmien korjaaminen
Jotkin avoimet rajapinnat aiheuttavat selaimessa [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS/Errors)-virheitä. Ne voidaan ohittaa käyttämällä välityspalvelinta kuten esim. cors anywhere: 
https://cors-anywhere.herokuapp.com/

### Ohje:
   1. Lisää ennen fetch-komentoa muuttuja `const proxy = 'https://cors-anywhere.herokuapp.com/';`
   2. Lisää ko. muuttuja haun eteen: `fetch(``${proxy}https://open-api.myhelsinki.fi/jne......``
