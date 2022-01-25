# h1 | Aleksis Rautiainen

## Sisällysluettelo

- [h1 | Aleksis Rautiainen](#h1--aleksis-rautiainen)
  - [Sisällysluettelo](#sisällysluettelo)
  - [Tehtävät](#tehtävät)
    - [z) Lue ja tiivistä](#z-lue-ja-tiivistä)
      - [FSF: FSF Free Software Definition](#fsf-fsf-free-software-definition)
      - [Karvinen 2021: Install Debian on VirtualBox](#karvinen-2021-install-debian-on-virtualbox)
      - [Karvinen 2016: Raportin kirjoittaminen](#karvinen-2016-raportin-kirjoittaminen)
      - [Välimäki 2005: Rise of Open Source: 5 Open Source Licenses as Alternative Governance Mechanisms: 5.1.1 - 5.1.4 (sivu 113 - 121)](#välimäki-2005-rise-of-open-source-5-open-source-licenses-as-alternative-governance-mechanisms-511---514-sivu-113---121)
    - [a) Asenna Linux](#a-asenna-linux)
    - [b) Listaa testaamasi koneen rauta](#b-listaa-testaamasi-koneen-rauta)
    - [c) Asenna kolme itsellesi uutta ohjelmaa](#c-asenna-kolme-itsellesi-uutta-ohjelmaa)
    - [d) Mitä lisenssiä kukin näistä ohjelmista käyttää?](#d-mitä-lisenssiä-kukin-näistä-ohjelmista-käyttää)
- [Lähteet](#lähteet)

## Tehtävät

### z) Lue ja tiivistä

#### FSF: FSF Free Software Definition

- Vapaata ohjelmistoa (free software) ei kuulu ymmärtää ilmaisena ateriana, vaan sananvapautena.
- Vapaa ohjelmisto vaatii vapaan käytön, ohjelman vapaan tutkimisen, jakamisen vapauden ja vapauden jakaa muokattuja versioita.
- Vapaa ohjelmisto ei tarkoita että se ei olisi kaupallista.

#### Karvinen 2021: Install Debian on VirtualBox

- Lataa Debian [täältä](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/current-live/amd64/iso-hybrid/).
- Lataa VirtualBox ja valitse sen menusta Machine: New...
- Luo virtuaalinen kovalevy.
- Aseta Debian ISO Image virtuaaliseksi CD-ROM-levyksi.
- Käynnistä ja valitse LIVE.
- Suorita asennus ja valitse hyvä salasana.
- Kirjaudu sisään.

#### Karvinen 2016: Raportin kirjoittaminen

- Raportoi täsmällisesti ja samaan aikaan kun teet.
- Hyvä raportti on Toistettava, Täsmällinen, Helppolukuinen ja se viittaa lähteisiin.
- Muista lisätä vakiotekstejä.
- Vältä pahoja mokia, kuten turhaa sepittämistä.

#### Välimäki 2005: Rise of Open Source: 5 Open Source Licenses as Alternative Governance Mechanisms: 5.1.1 - 5.1.4 (sivu 113 - 121)

- Avoin lähdekoodi on vapaa käyttää, vapaa kopioida, vapaa muokata ja siinä on avoin lähdekoodi.
- Avoin lähdekoodi ei ole missään nimessä tekijänoikeuksien vastainen.
- Historiallisesta perspektiivistä avoin lähdekoodi voidaan jakaa neljään isoon lisenssikategoriaan: GNU-, akateemiset-, yhteisö- ja yrityslisenssit

### a) Asenna Linux

#### Linux VirtualBoxiin

Ensimmäisenä asensin Debianin VirtualBoxiin.

![](kuvat/create.png)

![](kuvat/harddisk.png)

Asetin Debian ISO Imagen virtuaaliseksi CD-ROM-levyksi.

![](kuvat/debiancd.png)

#### Käynnistys

Käynnistin virtuaalisen Linuxin ja valitsin LIVEn.

![](kuvat/startup.png)

![](kuvat/desktop.png)

Kokeilin Linuxin toimivuutta menemällä työpydältä selaimeen TeroKarvinenCom:iin. Tämän avulla sain selville hiiren, näppäimistön, verkon ja näytön toimivuuden.

![](kuvat/testi.png)

#### Debianin asennus

Suoritin Debianin asennuksen, valitsin hyvän salasanan ja käynnistin Linuxin uudelleen.

![](kuvat/debianinstall.png)

![](kuvat/installing.png)

![](kuvat/alldone.png)

#### Ensimmäinen sisäänkirjautuminen ja askeleet

Suoritin ensimmäisen sisäänkirjautumisen ja selvitin toimivuuden uudelleen.

![](kuvat/firstlogin.png)

Avasin terminaalin ja tein tarvittavat alkutoimenpiteet.

![](kuvat/terminal.png)

![](kuvat/firewall.png)

### b) Listaa testaamasi koneen rauta

#### sudo lshw

'sudo lshw -short -sanitize' komento ei toiminut, jonka takia jouduin ensin asentaa lshw paketin.

![](kuvat/lshw.png)

Komennolla 'sudo lshw -short -sanitize' terminaaliin avautui lista VirtualBoxin käyttämästä laitteistosta. Ainoastaan prosessori "AMD Ryzen 5" näyttää olevan oman tietokoneeni laitteistoa, sillä muut laitteistot näyttävät olevan VirtualBoxin omia joita en osaa enempää avata.

![](kuvat/laitteisto.png)

### c) Asenna kolme itsellesi uutta ohjelmaa

#### Thunderbird

Ensimmäiseksi ohjelmaksi löysin sähköposti ohjelman Thunderbirdin, josta en ole koskaan ennen edes kuullut. Ohjelma on mozillan oma sähköposti ohjelma, joka toimii melko samalla tavalla kuin microsoftin ja googlen ohjelmat.

![](kuvat/thunderbird.png)

![](kuvat/thunderbirdlinux.png)

#### Krita

Toiseksi ohjelmaksi asensin Krita nimisen paint ohjelman, ja se vaikuttaa helppokäyttöiseltä ja melko monipuoliselta.

![](kuvat/installingkrita.png)

![](kuvat/krita.png)

![](kuvat/kritalinux.png)

#### VLC media player

Kolmantena ohjelmana asensin VLC media playerin, joka on ilmainen avoimen lähdekoodin multimediasoitin.

![](kuvat/vlc.png)

![](kuvat/vlclinux.png)

### d) Mitä lisenssiä kukin näistä ohjelmista käyttää?

#### Thunderbird

Thunderbird on avoimen lähdekoodin cross-platform sähköposti ja kalenteri sovellus. Avoimen lähdekoodin pitää noudattaa tiettyjä sääntöjä. esimerkiksi sen pitää olla kaikille vapaassa käytössä.

#### Krita

Krita on vapaa ja avoimen lähdekoodin paint ohjelma. Sen on tehnyt artistit jotka haluavat parhaat taidetyökalut kaikille. Avoimen lähdekoodin pitää noudattaa tiettyjä sääntöjä. esimerkiksi sen pitää olla kaikille vapaassa käytössä.

#### VLC media player

VLC on vapaa ja avoimen lähdekoodin multimediasoitin. Kaikki ovat vapaita käyttämään sitä ilmaiseksi, mutta sillä on omistaja. Avoimen lähdekoodin pitää noudattaa tiettyjä sääntöjä. esimerkiksi sen pitää olla kaikille vapaassa käytössä.


## Lähteet

Tero Karvinen - [h1](https://terokarvinen.com/2021/linux-palvelimet-ict4tn021-3018/#h1)

[FSF: FSF Free Software Definition](https://www.gnu.org/philosophy/free-sw.html)

[Karvinen 2021: Install Debian on VirtualBox](https://terokarvinen.com/2021/install-debian-on-virtualbox/)

[Karvinen 2016: Raportin kirjoittaminen](https://terokarvinen.com/2006/raportin-kirjoittaminen-4/)

[Välimäki 2005: Rise of Open Source: 5 Open Source Licenses as Alternative Governance Mechanisms](http://lib.tkk.fi/Diss/2005/isbn9529187793/isbn9529187793.pdf)

[Thunderbird](https://www.thunderbird.net/en-US/)

[Krita](https://krita.org/en/)

[VLC media player](https://www.videolan.org/)
