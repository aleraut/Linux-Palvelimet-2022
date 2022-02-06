# h3 | Aleksis Rautiainen

## Sisällysluettelo

- [h3 | Aleksis Rautiainen](#h3--aleksis-rautiainen)
  - [Sisällysluettelo](#sisällysluettelo)
  - [Tehtävät](#tehtävät)
    - [a) Asenna Apache](#a-asenna-apache)
    - [b) Laita käyttäjien kotisivut toimimaan](#b-laita-käyttäjien-kotisivut-toimimaan)
    - [c) Tee validi HTML5 sivu](#c-tee-validi-html5-sivu)
    - [d) Surffaa oman palvelimesi weppisivuja](#d-surffaa-oman-palvelimesi-weppisivuja)
    - [e) Vaihda Apachen esimerkkisivu johonkin lyhyeen sivuun](#e-vaihda-apachen-esimerkkisivu-johonkin-lyhyeen-sivuun)
- [Lähteet](#lähteet)

## Tehtävät

### a) Asenna Apache

Ensimmäisenä päivitin pakettilistan komennolla sudo apt-get update, jonka jälkeen asensin apachen komennolla sudo apt-get install apache2. Komennolla "sudo service apache2 start" varmistetaan, että apache käynnistyy.

![](kuvat/apacheinstall.png)

Testasin apachen toiminnan ohjeen mukaan. Ensimmäisenä menin selaimessa osoitteeseen "http://localhost", jossa esiin tuli apachen esimerkkisivu. Sivulla lukee "It works", joten oletan apachen toimivan.

![](kuvat/localhost.png)

Apache-palvelimeni ip-osoitteen sain Terminaalista komennolla "ip addr". IP osoitteen sai kohdasta inet, ja se oli 10.0.2.15 .

![](kuvat/ipaddr.png)

Selaimessa menin osoitteeseen "http://10.0.2.15", jossa aukesi sama sivu kuin localhostilla.

![](kuvat/iphost.png)


### b) Laita käyttäjien kotisivut toimimaan

Ensin piti sallia käyttäjän kotihakemisto komennolla "sudo a2enmod userdir", ja käynnistää sen jälkeen apache uudelleen komennolla "sudo /etc/init.d/apache2 restart".

![](kuvat/userdir.png)

Seuraavaksi tein kotihakemistoon kansion "public_html" komennolla "mkdir public_html". Komennolla "whoami", sain käyttäjänimeni "aleraut", jonka avulla sain samalla koneella yhteyden paikalliselle palvelimelle "http://localhost/~aleraut/".

![](kuvat/publichtml.png)


### c) Tee validi HTML5 sivu

Seuraavaksi tein validin html5 sivun paikalliselle palvelimelle. Kotihakemistossani komennolla "ls", näin kansiot sen sisällä. menin juuri tekemääni public_html kansioon komennolla "cd public_html/". Sen sisällä loin index.html tiedoston komennolla "micro index.html", ja pääsin suoraan muokkaamaan sitä. Kirjotin sinne vain "Aleraut kotisivu". Päivitettyäni sivun selaimessa teksti ilmestyi ruudulle.

![](kuvat/kotisivu.png)

HTML-sivun piti olla validi, joten muokkasin html-tiedostoa "micro" komennolla, ja laitoin tiedoston validointi-nettisivulle.

![](kuvat/html.png)

![](kuvat/htmlcheck.png)

![](kuvat/alerautkoti.png)


### d) Surffaa oman palvelimesi weppisivuja

Etsin apachen lokitiedot "/var/log/apache2" -hakemistosta. En aluksi saanut oikeuksia sen lukemiseen, joten tein itsestäni root käyttäjän komennolla "sudo -i". Olisi varmaan ollut parempikin keino, mutta en keksinyt. Apache2 hakemistossa aloin seuraamaan access.log -tiedostoa komennolla "tail -f access.log". Päivitin omaa palvelintani selaimessa, ja tein virheellisen yrityksen poistamalla "~"-merkin nimen edestä.

![](kuvat/log.png)

Kuvasta näkee kaksi ns. riviä, jotka molemmat alkavat laitteeni ip-osoitteella 127.0.0.1. Tämän jälkeen näkyy päivämäärä ja tapahtuman kellonaika, sekä aikavyöhyke. Sen jälkeen näkyy haettu osoite (ensimmäisessä rivissä näkyy "~" nimen edessä ja toisessa ei). Numero 200 kertoo ensimmäisellä rivillä onnistuneesta latauksesta ja numero 404 kertoo epäonnistuneesta hausta (not found). Lopussa näkyy vielä selain-Mozilla ja käyttöjärjestelmä Linux. Muista tiedoista en ole varma.


### e) Vaihda Apachen esimerkkisivu johonkin lyhyeen sivuun

Vaihdoin apachen esimerkkisivun localhost-nettisivulla menemällä annettuun hakemistosijaintiin "/var/www/html/", ja siellä muokkasin index.html tiedostoa komennolla "micro index.html".

![](kuvat/wwwhtml.png)

![](kuvat/microlocal.png)

![](kuvat/uusilocal.png)


## Lähteet

terokarvinen.com tehtävänanto - [h3](https://terokarvinen.com/2021/linux-palvelimet-ict4tn021-3018/#h3)

[Install Apache Web Server on Ubuntu](https://terokarvinen.com/2008/install-apache-web-server-on-ubuntu-4/)
