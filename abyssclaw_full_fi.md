# AbyssClaw-projektin määrittely
**Alaotsikko: OpenClaw-pohjainen ennakoivan turvallisuuden havaitsemis-, puolustus- ja hallinta-alusta**

## 1. Projektin yleiskuva

### 1.1 Projektin nimi
**AbyssClaw ennakoivan turvallisuuden havaitsemis- ja puolustusalusta**

### 1.2 Tavoite ja rooli
AbyssClaw on OpenClaw’n päälle rakennettu tietoturvakyvykkyyksien alusta. Se keskittyy organisaatioiden keskeisiin tarpeisiin verkko-, järjestelmä- ja sovellusturvallisuudessa sekä näkyvän hyökkäyspinnan, konfiguraatioturvallisuuden, haavoittuvuuksien hallinnan ja riskien suljetun käsittelyketjun alueilla.  
Yhtenäisen omaisuusnäkymän, jatkuvan tarkastuksen, riskikorrelaation, ennakoivan puolustuksen, korjausten verifioinnin ja hallintamittareiden avulla alusta mahdollistaa siirtymisen passiivisesta reagoinnista ennakoivaan havaitsemiseen, ennakoivaan varoittamiseen, ennakoivaan puolustukseen ja ennakoivaan korjaamiseen.

### 1.3 Tausta
Kun liiketoimintajärjestelmät ovat yhä useammin internetiin avautuvia, pilvipohjaisia, kontitettuja ja API-vetoisia, perinteinen manuaaliseen tarkastukseen ja hajanaisiin työkaluihin perustuva turvallisuuden hallintamalli on paljastanut selviä heikkouksia:

- Omaisuuskanta ei ole selkeä eikä hyökkäyspinta näy riittävästi
- Haavoittuvuuksien havaitseminen viivästyy ja korjausjaksot ovat pitkiä
- Riskit ovat hajallaan verkko-, isäntä-, väliohjelmisto- ja sovelluskerroksissa ilman yhtenäistä analyysia
- Korjausvastuut ovat epäselviä eikä suljettua prosessia synny
- Korkean riskin muutoksille, virhekonfiguraatioille, heikoille salasanoille ja käyttöoikeusongelmille ei ole jatkuvaa ehkäisyä

AbyssClaw’n tavoitteena on muuttaa OpenClaw’n kyvykkyydet teknisesti rakennetuksi, alustamaiseksi ja toimintamalliksi juurrutetuksi järjestelmäksi, joka muodostaa kestävän, auditoitavan, mitattavan ja suljetun tietoturvan hallintakehyksen.

---

## 2. Projektin tavoitteet

### 2.1 Kokonaistavoite
Rakentaa integroitu tietoturva-alusta, joka kattaa omaisuuden tunnistamisen, riskien havaitsemisen, haavoittuvuuksien löytämisen, perustason tarkastukset, ennakoivan puolustuksen, korjausten varmistuksen ja operatiivisen analyysin, jotta organisaation tietoturvariskiä voidaan pienentää jatkuvasti.

### 2.2 Osa-alueiden tavoitteet
**Ennakoiva havaitseminen**  
Tunnistaa jatkuvasti ulkoisen näkyvyyden, verkkopalvelut, järjestelmäkonfiguraatioiden riskit, sovellusten heikkoudet, riippuvuusriskit ja poikkeavat käyttöoikeudet.

**Ennakoiva puolustus**  
Yhdistää tarkastusten tulokset suojausstrategioihin, perustason kovennukseen, pääsynhallintaan, konfiguraatioiden tiukennukseen ja hälytyksiin, jotta todellinen hyökkäyspinta pienenee.

**Riskien ehkäisy**  
Siirtää turvallisuustarkastukset etupainotteisesti omaisuuden käyttöönottoon, järjestelmämuutoksiin, julkaisuun ja konfiguraatiomuutoksiin, jotta riskit voidaan löytää ennen tapahtumia, hallita muutosten aikana ja arvioida jälkikäteen.

**Haavoittuvuuksien hallinta**  
Luoda täysi prosessi, joka kattaa haavoittuvuuksien löytämisen, luokittelun, arvioinnin, vastuuttamisen, korjaamisen, uudelleentestauksen ja sulkemisen.

**Tietoturvaoperaatiot**  
Hyödyntää yhtenäisiä koontinäkymiä, trendianalyysiä, omistajuuskartoitusta ja KPI-mittaristoa, jotta tietoturvatoiminta siirtyy työkalukeskeisyydestä hallittuun toteutukseen.

---

## 3. Laajuus

### 3.1 Kattavuus
AbyssClaw kattaa pääasiassa seuraavat kohteet:

- Verkon rajapintaomaisuus: julkiset IP-osoitteet, verkkotunnukset, aliverkkotunnukset, avoimet portit ja verkkopalvelut
- Järjestelmätason omaisuus: palvelimet, virtuaalikoneet, pilvi-isännät, käyttöjärjestelmät ja väliohjelmistot
- Sovellustason omaisuus: verkkosovellukset, API-palvelut, hallintajärjestelmät ja mobiilitaustapalvelut
- Alustaympäristöt: kontit, kuva-arkistot, Kubernetes ja CI/CD-ympäristöt
- Komponentit ja riippuvuudet: kolmannen osapuolen kirjastot, perustason komponentit, avoimen lähdekoodin riippuvuudet ja väliohjelmistoversiot
- Identiteetti- ja käyttöoikeuskohteet: heikot salasanat, liialliset oikeudet, jaetut tilit ja pitkään vaihtamattomat tunnistetiedot
- Konfiguraatio- ja politiikkakohteet: turvallisuusperustasot, näkyvyyssäännöt, pääsynhallinta, turvaryhmät ja WAF-/isäntäsuojauksen asetukset

### 3.2 Rajauksen ulkopuolelle jäävä
Projektirajauksen selkeyttämiseksi seuraavat asiat eivät kuulu tämän vaiheen ydinlaajuuteen:

- Ulkoisten kohteiden testaus ilman valtuutusta
- Tuotantoympäristöjen korkean riskin tuhoavat validoinnit
- Laiton tunkeutuminen, luvaton hallinta tai käyttörajoitusten ohitus
- Kokeelliset hyökkäysesittelyt, joilla ei ole liiketoiminnallista turvallisuustarvetta

Kaikkien AbyssClaw’n tarkastus-, validointi- ja korjaustoimien on noudatettava laillista valtuutusta, minimaalista vaikutusta, täydellistä auditointia ja palautettavuutta.

---

## 4. Periaatteet

### 4.1 Lainmukaisuus ja vaatimustenmukaisuus
Kaikkien tarkastustoimien tulee perustua selkeään valtuutukseen, rajauksen vahvistamiseen, vastuiden vahvistamiseen ja auditointijälkiin, jotta alustaa käytetään vain lailliseen puolustukseen, turvallisuusarviointiin ja riskien hallintaan.

### 4.2 Ennakoivuus etusijalla
Etusija annetaan jatkuvalle havaitsemiselle, jatkuvalle valvonnalle ja jatkuvalle kovennukselle sen sijaan, että odotetaan tapahtumia ja reagoidaan vasta niiden jälkeen.

### 4.3 Minimaalinen vaikutus
Kaikissa skannaus-, validointi- ja linkitetyissä toimissa on hallittava taajuutta, rinnakkaisuutta, laajuutta ja ajoitusta, jotta tuotantopalveluihin ei synny merkittävää häiriötä.

### 4.4 Suljettu riskinkäsittely
Alustan ei tule vain tuottaa ongelmalistoja, vaan myös ohjata omistajuutta, korjaamista, uudelleentestausta ja sulkemista, jotta haavoittuvuuksien hallinta todella toteutuu.

### 4.5 Auditoitavuus ja mitattavuus
Alustan tulee säilyttää toimintalokit, skannaustiedot, politiikkamuutokset ja korjaustilat sekä muuntaa ne mitattaviksi tunnusluvuiksi johtamisen tueksi。

---

## 5. Kokonaisratkaisu

OpenClaw toimii AbyssClaw’n perustana, ja ratkaisu jäsennetään viiteen kerrokseen:

### Kerros 1: Omaisuuden hahmotuskerros
Tunnistaa ja hallitsee kaikki verkko-, järjestelmä-, sovellus- ja pilviresurssit muodostaen täydellisen omaisuusluettelon ja hyökkäyspintakartan.

### Kerros 2: Havaitsemis- ja analyysikerros
Toteuttaa haavoittuvuuksien tunnistuksen, perustasotarkastukset, konfiguraatioauditoinnin, riippuvuusanalyysin, riskikorrelaation ja priorisoinnin.

### Kerros 3: Puolustuksen linkityskerros
Kytkee löydökset puolustustoimiin, kuten kovennuspolitiikkoihin, hälytysten korotuksiin, pääsyn rajoittamiseen, tilien hallintaan, paikkaussuosituksiin ja konfiguraation kiristämiseen.

### Kerros 4: Hallinnan sulkukerros
Vastuuttaa, seuraa, uudelleentestaa, hyväksyy ja arkistoi riskit poikkiorganisatorisen yhteistyömallin avulla.

### Kerros 5: Operatiivisen päätöksenteon kerros
Parantaa kokonaisvaltaista turvallisuuskyvykkyyttä raportoinnin, koontinäkymien, trendianalyysin ja kypsyystason arvioinnin kautta.

---

## 6. Ydinkyvykkyydet

## 6.1 Ennakoiva omaisuuden tunnistaminen
AbyssClaw ratkaisee ensin näkyvyyden ongelman.  
Omaisuustiedon keruun, verkkotunnusten yhdistelyn, näkyvyyden tunnistamisen, palvelusormenjälkien, järjestelmätietojen keruun ja sovellusten sisäänmenopisteiden kartoituksen avulla alusta rakentaa yhtenäisen turvallisuusomaisuuden näkymän.

Keskeiset kyvykkyydet:

- Internetiin näkyvän hyökkäyspinnan tunnistaminen
- Verkkotunnus- ja aliverkkotunnusomaisuuden kokoaminen
- IP- ja porttipalvelujen tunnistaminen
- Isäntä- ja järjestelmäversioiden keruu
- Sovellusten sisäänmenopisteiden, rajapintojen ja taustapolkujen tunnistaminen
- Pilviresurssien ja konttiomaisuuden synkronointi

Tuloksena saadaan yhtenäinen omaisuusluettelo, riskitunnisteet, kriittisyysluokat ja omistussuhteiden kartoitus.

---

## 6.2 Ennakoiva riskien ja haavoittuvuuksien havaitseminen
Alusta rakentaa jatkuvan tarkastuskyvykkyyden verkko-, järjestelmä- ja sovelluskerroksiin.

### Verkkokerros
Tunnistaa tarpeettomasti näkyvät palvelut, heikon reunasuojauksen, poikkeavat portit, vanhentuneet protokollat ja virheelliset pääsypolitiikat.

### Järjestelmäkerros
Keskittyy käyttöjärjestelmähaavoittuvuuksiin, perustason poikkeamiin, heikkoihin salasanoihin, puuttuviin korjauksiin, vaarallisesti käytössä oleviin palveluihin, virheellisiin käyttöoikeuksiin ja puutteelliseen lokitukseen.

### Sovelluskerros
Keskittyy tunnistautumis- ja valtuutuspuutteisiin, syötteiden validoinnin heikkouksiin, virhekonfiguraatioihin, arkaluonteisen tiedon vuotoihin, riippuvuuksien haavoittuvuuksiin, rajapintojen liialliseen näkyvyyteen ja julkaisuun liittyviin turvallisuuspuutteisiin.

### Riippuvuus- ja toimitusketjukerros
Tunnistaa kolmannen osapuolen komponenttiversioiden riskit, peruskuvien heikkoudet, avoimen lähdekoodin tunnetut haavoittuvuudet ja build-putken riskit.

Alustan ei tule vastata vain kysymykseen “kuinka monta haavoittuvuutta löytyi”, vaan myös seuraaviin:

- Mitkä riskit ovat todennäköisimmin ensimmäisiä hyväksikäytön kohteita
- Mitkä ongelmat vaikuttavat ydinliiketoimintaan
- Mitkä haavoittuvuudet tuottavat suurimman korjaushyödyn
- Mitkä asiat vaativat välitöntä suojausta versionvaihdon odottamisen sijaan

---

## 6.3 Ennakoiva puolustus
AbyssClaw ei pidä ongelmien löytämistä päätepisteenä, vaan sen tulee ohjata puolustaviin toimiin.

Alustan tulee tukea seuraavia linkitetyn puolustuksen kyvykkyyksiä:

- Nopeat rajaussuositukset korkean riskin näkyvyydelle
- Suositukset tarpeettomien näkyvien palveluiden poistamiseksi käytöstä
- Automaattinen validointi ja korjaussuositukset perustason poikkeamille
- Poikkeavien tilien, heikkojen salasanojen ja käyttöoikeusepätasapainon hallinta
- Pääsynhallinnan vahvistaminen kriittisille sovellusten sisäänmenopisteille
- Väliaikaiset lievennyskeinot korkean riskin haavoittuvuuksille
- Kytkentäperusteet suojauslaitteille tai politiikkajärjestelmille

Painopiste ei ole “automaattisessa hyökkäyksessä”, vaan **automaattisessa riskin pienentämisessä**.  
AbyssClaw’n ydinarvo näkyy siinä, että mitä aikaisemmin havaitaan, sitä aikaisemmin altistus pienenee; mitä nopeammin arvioidaan, sitä nopeammin riskiä hallitaan.

---

## 6.4 Riskien ehkäisy
AbyssClaw’n tulee siirtää tietoturva etupainotteisesti omaisuuden käyttöönottoon, julkaisumuutoksiin ja päivittäisiin operaatioihin.

Alustan tulee tukea:

- Uusien omaisuuskohteiden automaattista sisällyttämistä tarkastusalaan
- Perustaso- ja haavoittuvuustarkastuksia ennen uusien järjestelmien käyttöönottoa
- Riippuvuus- ja konfiguraatioriskien tarkastamista ennen julkaisuja
- Erovalidointia kriittisten konfiguraatiomuutosten jälkeen
- Reaaliaikaisia hälytyksiä korkean riskin näkyvyysmuutoksista
- Pitkäaikaisten jäännösriskien määräaikaista tarkastelua

Riskien ehkäisyn tavoitteena on vähentää turvattomia käyttöönottoja eikä vain kompensoida ongelmia jälkikäteen.

---

## 6.5 Haavoittuvuuksien hallinta ja korjausten suljettu ketju
Haavoittuvuuksien hallinta on projektin vaikuttavuuden ydin.  
Alustan tulee muodostaa täydellinen prosessi:

**Havaitseminen**  
Ongelmat kirjataan automaattisen skannauksen, politiikkatarkastusten, manuaalisen validoinnin ja lokianalyysin perusteella.

**Arviointi**  
Ongelmat luokitellaan liiketoiminnan kriittisyyden, hyödynnettävyyden, näkyvyystilan, kompensoivien kontrollien ja aiempien hyväksikäyttöolosuhteiden perusteella.

**Vastuuttaminen**  
Ongelmat osoitetaan vastuullisille järjestelmä-, sovellus-, operaatio- tai kehitystiimeille.

**Korjaaminen**  
Ongelmat käsitellään paikkauksilla, konfiguraatiomuutoksilla, käyttöoikeuksien vähentämisellä, komponenttipäivityksillä, koodikorjauksilla tai väliaikaisilla lievennyksillä.

**Uudelleentestaus**  
Korjatut ongelmat todennetaan ja varmistetaan, onko riski todella suljettu.

**Sulkeminen**  
Todisteet, sulkupäätelmät ja aikaleimat säilytetään auditointia ja jälkiarviointia varten.

Prosessin on oltava jäljitettävä, tilastoitavissa ja arvioitavissa, jotta vältetään tilanne, jossa ongelmia löytyy paljon mutta korjataan vähän.

---

## 6.6 Tietoturvatiedon ja kokemuksen kerryttäminen
AbyssClaw’n tulee muuntaa historiallinen kokemus alustan tietopääomaksi, mukaan lukien:

- Haavoittuvuuksien luokittelu- ja korjaussuosituskirjasto
- Järjestelmien ja väliohjelmistojen kovennusperustasot
- Yleisten riskien käsittelyohjeet
- Kartoitus turvallisen kehityksen vaatimuksiin
- Historialliset tapahtumat ja korjausesimerkit
- Omistajuuskartoitus ja toistuvuusanalyysi

Näin alusta ei ole vain skanneri, vaan todellinen **organisaatiotason tietoturvatiedon alusta**.

---

## 7. Järjestelmäarkkitehtuuri

## 7.1 Arkkitehtuurin rooli
AbyssClaw käyttää mallia “yhtenäinen alusta + modulaariset kyvykkyydet + laajennettava integraatio”, jotta käyttöönotto on nopea ja kasvu skaalautuva.

## 7.2 Suositeltu kerrosmalli

### Omaisuuden integraatiokerros
Vastaa CMDB:n, pilvialustojen, isäntäluetteloiden, verkkotunnusluetteloiden, konttialustojen ja sovellusluetteloiden liittämisestä.

### Tehtävien ajoituskerros
Vastaa tarkastusten orkestroinnista, jaksotuksesta, nopeusrajoituksista, resurssikiintiöistä ja vaikutuksen hallinnasta.

### Kyvykkyyksien suorituskerros
OpenClaw ja siihen liittyvät moduulit toteuttavat varsinaisen havaitsemisen, perustason tarkastuksen, versiotunnistuksen, riippuvuusanalyysin, validoinnin ja riskien koonnin.

### Datan analyysikerros
Vastaa riskikorrelaatiosta, luokittelusta, trendianalyysistä, vastuiden kartoituksesta ja historiallisesta vertailusta.

### Alustapalvelukerros
Tarjoaa tiketöinnin, ilmoitukset, koontinäkymät, raportit, käyttöoikeudet, auditoinnin ja tietopankkitoiminnot.

### Linkitetyn hallinnan kerros
Yhdistyy paikanhallintaan, konfiguraatiokeskuksiin, hälytysalustoihin, identiteetinhallintaan, omaisuusjärjestelmiin ja kehitysprosesseihin muodostaen suljetun ketjun.

---

## 8. Toiminnalliset moduulit

| Moduuli | Kuvaus | Ydinarvo |
|---|---|---|
| Omaisuuden hallintamoduuli | Rakentaa omaisuusluettelon, palvelusormenjäljet, omistussuhteet ja kriittisyysluokat | Ratkaisee epäselvän omaisuusnäkyvyyden |
| Näkyvän hyökkäyspinnan hallintamoduuli | Tunnistaa internetiin näkyvät sisäänmenopisteet, avoimet portit ja ulospäin näkyvät palvelut | Löytää todellisen hyökkäyspinnan |
| Haavoittuvuuksien tunnistusmoduuli | Toteuttaa jatkuvaa tarkastusta verkko-, järjestelmä-, sovellus- ja riippuvuuskerroksissa | Löytää tekniset riskit |
| Perustason tarkastusmoduuli | Tarkistaa käyttöjärjestelmien, väliohjelmistojen, tilien ja konfiguraatioiden vaatimustenmukaisuuden | Vähentää perustason virheitä |
| Riskikorrelaatiomoduuli | Yhdistää näkyvyystilan, liiketoiminnan kriittisyyden, haavoittuvuuden vakavuuden ja kompensoivat kontrollit | Parantaa priorisoinnin tarkkuutta |
| Korjausten sulkemismoduuli | Tikettivirta, vastuuttaminen, korjaustila, uudelleentestaus ja sulkeminen | Parantaa hallinnan tehokkuutta |
| Puolustuksen linkitysmoduuli | Käynnistää politiikkasuosituksia, vähentää näkyvyyttä, korottaa hälytyksiä ja tiukentaa perustasoja | Lyhentää suojauksen vasteaikaa |
| Operatiivisen analyysin moduuli | Koontinäkymät, raportit, trendit, SLA ja toistuvuusanalyysi | Tukee johtamispäätöksiä |
| Tietopankkimoduuli | Korjausohjeet, tapauskertymä ja standardikartoitus | Rakentaa organisaation kyvykkyyttä |

---

## 9. Roolit ja vastuut

## 9.1 Alustan ylläpitäjä
Vastaa alustan konfiguraatiosta, käyttöoikeuksien hallinnasta, kyvykkyyksien integraatiosta, tehtävien orkestroinnista, auditointilokeista ja operatiivisesta ylläpidosta.

## 9.2 Tietoturvaoperaatioiden henkilöstö
Vastaa riskien arvioinnista, prioriteettien säädöstä, tikettien jakelusta, strategiasuosituksista, uudelleentestauksen vahvistamisesta ja raportoinnista.

## 9.3 Järjestelmäoperaatioiden omistaja
Vastaa palvelimista, väliohjelmistoista, verkkolaitteista, perustason konfiguraatioista ja paikkauksiin liittyvästä korjaamisesta.

## 9.4 Sovelluskehityksen omistaja
Vastaa sovellushaavoittuvuuksien korjauksista, riippuvuuspäivityksistä, konfiguraatioiden optimoinnista ja julkaisuun liittyvistä korjauksista.

## 9.5 Liiketoimintajärjestelmän omistaja
Vastaa liiketoimintavaikutuksen arvioinnista, korjaussuunnitelmien vahvistamisesta ja julkaisuikkunoiden koordinoinnista.

## 9.6 Johto- ja auditointiroolit
Vastaavat projektin valvonnasta, mittareiden arvioinnista, resurssien koordinoinnista ja politiikkojen tarkastuksesta.

---

## 10. Prosessit

## 10.1 Riskien havaitsemisprosessi
Kun omaisuuskohteet on liitetty alustaan, järjestelmä suorittaa tarkastustehtävät suunnitelman mukaisesti, muodostaa riskilistan ja luokittelee löydökset automaattisesti niitä vastaaviin omaisuus- ja vastuualueisiin.

## 10.2 Riskien luokitteluprosessi
Arviointi perustuu haavoittuvuuden vakavuuteen, internet-näkyvyyteen, kompensoivien kontrollien olemassaoloon ja siihen, vaikuttaako asia ydintoimintaan.

Suositellut tasot:

- **Kriittinen**: suoraan näkyvä, vaikuttaa ydinjärjestelmiin ja sisältää korkean todellisen riskin; vaatii välitöntä käsittelyä
- **Korkea**: voi aiheuttaa merkittävää turvallisuusvaikutusta ja on korjattava määritellyssä ajassa
- **Keskitaso**: voi olla hyödynnettävissä ja tulee käsitellä suunnitellun julkaisun tai jaksollisen korjauksen yhteydessä
- **Matala**: lähinnä optimointi- ja hallintakohde, käsitellään resurssisuunnittelun mukaan

## 10.3 Korjausten sulkemisprosessi
Arvioinnin jälkeen alusta muodostaa automaattisesti tai puoliautomaattisesti korjaustehtävät, osoittaa ne vastuullisille omistajille, seuraa korjaustilaa ja käynnistää uudelleentestauksen korjausten jälkeen.

## 10.4 Puolustuksen linkitysprosessi
Vahvistettujen korkean riskin näkyvyyskohteiden osalta alusta voi koordinoida väliaikaisia lievennystoimia nykyisten suojausjärjestelmien puitteissa, kuten pääsyn rajoittamista, konfiguraation kiristämistä, hälytysten korotusta ja kohdennettua valvontaa.

## 10.5 Arviointi ja parantaminen
Korkean vaikutuksen haavoittuvuudet, toistuvat ongelmat ja myöhästyneet korjaukset tulee arvioida, jotta politiikat, prosessit ja standardit paranevat.

---

## 11. Riskiluokitus ja käsittelystrategia

### Kriittinen
Koskee asioita, jotka ovat internetiin näkyviä, vaikuttavat ydinomaisuuteen ja sisältävät korkean todellisen riskin.  
Vaikutusalue on vahvistettava heti, lievennystoimet priorisoitava ja juurisyyn korjaus tehtävä sen jälkeen.

### Korkea
Koskee asioita, jotka voivat lyhyellä aikavälillä aiheuttaa merkittävää vaikutusta.  
Ne on korjattava määräajassa ja niitä on seurattava erillisinä kohteina.

### Keskitaso
Koskee asioita, jotka vaativat hallintaa mutta eivät muodosta välitöntä riskiä.  
Ne tulee sisällyttää normaaleihin muutoksiin, versiopäivityksiin tai perustason korjauksiin.

### Matala
Koskee pitkäaikaisia optimointikohteita.  
Ne tulee sisällyttää hallintasuunnitelmaan ja teknisen velan seurantaan.

Projektissa korostettava keskeinen periaate on, että käsittelystrategian on perustuttava liiketoiminnan kriittisyyteen ja näkyvyystilaan, ei pelkästään teknisiin pisteisiin.

---

## 12. Turvallisuus- ja vaatimustenmukaisuusvaatimukset

AbyssClaw’n on täytettävä seuraavat vaatimukset:

### 12.1 Valtuutusten hallinta
Kaikilla skannaus-, validointi- ja linkitetyillä toimilla on oltava selkeästi määritellyt valtuutusrajat. Rajauksen ulkopuoliset toimet on estettävä.

### 12.2 Auditointijälki
Alustan on tallennettava tehtävien käynnistykset, parametrimuutokset, tulosten käyttö, tikettivirrat ja linkitetyt toimet jäljitettävyyden varmistamiseksi.

### 12.3 Vähimmän oikeuden periaate
Alustan käyttäjien ja integroitujen järjestelmien on noudatettava vähimmän oikeuden periaatetta luvattoman käytön ja arkaluonteisen datan altistumisen rajoittamiseksi.

### 12.4 Datan suojaus
Tarkastustulokset, omaisuustiedot, haavoittuvuuksien yksityiskohdat ja tilitiedot tulee suojata käyttöoikeuksilla, peittää tarvittaessa ja tallentaa turvallisesti.

### 12.5 Vaikutusten hallinta
Korkean taajuuden tehtäviin, arkaluonteisiin tehtäviin ja kriittisten liiketoimintajaksojen tarkastuksiin tulee sisällyttää nopeusrajoitus, sallintalistat ja hyväksyntämenettelyt.

---

## 13. Toteutustiekartta

## 13.1 Vaihe yksi: perustan integrointi
Tavoitteena on muodostaa vähimmäiskelpoiset alustakyvykkyydet, mukaan lukien:

- OpenClaw-kyvykkyyksien integrointi ja alustointi
- Keskeisten omaisuuskohteiden liittäminen
- Perusskannaus ja perustason tarkastus
- Riskilista ja omaisuuskoontinäkymät
- Alustava tikettipohjainen sulkumekanismi

## 13.2 Vaihe kaksi: hallinnan linkitys
Tavoitteena on luoda poikkiosastollinen korjausten suljettu ketju:

- Omistajuuskartoitus
- Integraatio tiketöintijärjestelmiin
- Korjausten uudelleentestauksen käyttöönotto
- Trendiraportointi ja SLA-hallinta
- Korkean riskin asioiden linkitetyt puolustusstrategiat

## 13.3 Vaihe kolme: etupainotteinen ehkäisy
Tavoitteena on upottaa turvallisuus operaatio- ja kehitysprosesseihin:

- Uusien omaisuuskohteiden automaattinen liittäminen
- Riskitarkastukset ennen julkaisuja
- Automaattinen validointi konfiguraatiomuutosten jälkeen
- Riippuvuus- ja kuvapohjariskien tarkastusten siirtäminen vasemmalle
- Jatkuva turvallisuusperustason varmistaminen

## 13.4 Vaihe neljä: älykkäät operaatiot
Tavoitteena on parantaa automaatiota ja päätöksenteon tukea:

- Älykäs priorisointisuositus
- Ongelman toistuvuusanalyysi
- Korjausten vaikuttavuuden arviointi
- Riskikeskittymien tunnistaminen
- Johdon hallintanäkymät

---

## 14. Toimitettavat tuotokset

Projektin valmistuttua suositellaan seuraavia tuotoksia:

- AbyssClaw-alustajärjestelmä
- Yhtenäinen omaisuus- ja riskiluettelo
- Havaitsemisstrategiat ja perustasokirjasto
- Haavoittuvuuksien hallintaprosessi ja politiikkadokumentit
- Korjaus- ja uudelleentestausmekanismit
- Operatiivisten raporttien mallipohjat
- Rooli-, käyttöoikeus- ja auditointisuunnitelmat
- Tietoturvatietopankki ja korjauskäsikirja
- Projektin hyväksyntäraportti

---

## 15. Vaikuttavuusmittarit

AbyssClaw’ta ei tule arvioida vain löydösten määrän perusteella, vaan hallinnan vaikuttavuuden perusteella. Suositeltuja mittareita ovat:

### 15.1 Havaitsemismittarit
- Liitettyjen omaisuuskohteiden kattavuusaste
- Internetiin näkyvien kohteiden tunnistusaste
- Riskien havaitsemisen ajantasaisuus
- Perustasotarkastuksen kattavuus

### 15.2 Hallintamittarit
- Kriittisten ja korkean riskin haavoittuvuuksien korjausaika
- Haavoittuvuuksien uudelleentestauksen läpäisyaste
- Määräajan ylittäneiden ratkaisemattomien asioiden osuus
- Toistuvien ongelmien uusiutumisaste

### 15.3 Puolustusmittarit
- Hyökkäyspinnan pienentymisaste
- Poikkeavien näkyvien palvelujen supistumisaste
- Heikkojen salasanojen ja korkean riskin konfiguraatioiden siivousaste
- Korkean riskin lievennystoimien toteutusaste

### 15.4 Johtamismittarit
- Vastuutahojen reagoinnin ajantasaisuus
- Tikettien sulkemisaste
- Auditoinnin jäljitettävyysaste
- Kuukausittainen riskin vähenemistrendi

---

## 16. Keskeiset riskit ja vastatoimet

### 16.1 Epätäydellinen omaisuuden liittäminen
Tämä voi johtaa puutteelliseen tarkastuskattavuuteen ja vääristyneeseen riskinarvioon.  
Ratkaisuna on monilähteinen liittäminen ja säännöllinen omaisuustäsmäytys.

### 16.2 Skannaus vaikuttaa liiketoimintaan
Korkeataajuinen tai sopimaton tarkastus voi vaikuttaa tuotantojärjestelmiin.  
Ratkaisuna ovat tehtävien luokittelu, taajuuden hallinta, kriittisten aikajaksojen välttäminen ja vaiheittainen validointi.

### 16.3 Epäselvä korjausvastuu
Tämä voi johtaa haavoittuvuuksien pitkäaikaiseen kertymiseen.  
Ratkaisuna on omaisuuksien omistajuuden ja vastuiden ketjujen määrittely tiketeissä.

### 16.4 Liikaa tuloksia mutta liian vähän toimintaa
Tämä johtaa tilanteeseen, jossa “koontinäkymät ovat rikkaita mutta korjauksia ei tehdä”.  
Ratkaisuna on priorisoinnin, sulkumittauksen ja johdon koontinäkymien korostaminen.

### 16.5 Liiallinen riippuvuus yhdestä työkalusta
Tämä voi rajoittaa alustan pitkän aikavälin kyvykkyyttä.  
Ratkaisuna on säilyttää modulaarinen laajennettavuus, jotta AbyssClaw pysyy korvattavana, integroitavana ja skaalautuvana OpenClaw’n päällä.

---

## 17. Projektin arvoyhteenveto

AbyssClaw’n ydinarvo ei ole vain uuden tietoturvatyökalun lisääminen, vaan ennakoivan havaitsemisen, ennakoivan puolustuksen, jatkuvan hallinnan ja korjausten suljetun ketjun rakentaminen OpenClaw’n ympärille.

Se ei ratkaise vain yksittäisiä haavoittuvuuksia. Se ratkaisee seuraavat perustavanlaatuiset ongelmat:

- Omaisuudet tulevat aidosti näkyviksi
- Riskit tulevat aidosti arvioitaviksi
- Ongelmat saavat aidon omistajuuden
- Korjaukset voidaan aidosti varmentaa
- Tietoturvasta tulee aidosti osa päivittäistä toimintaa ja liiketoimintaprosesseja

Lopulta AbyssClaw auttaa organisaatiota rakentamaan kestävän, mitattavan ja kehittyvän tietoturvan hallintakyvykkyyden, pienentää verkko-, järjestelmä- ja sovelluskerrosten kokonaisriskialtistusta sekä parantaa liiketoiminnan turvallisuutta ja vakautta.

---

# Liite: yhden lauseen määritelmä
**AbyssClaw on OpenClaw’n päälle rakennettu ennakoivan tietoturvan hallinta-alusta. Yhtenäisen omaisuusnäkyvyyden, jatkuvan riskien havaitsemisen, ennakoivan puolustuksen linkityksen ja haavoittuvuuksien suljetun korjausketjun avulla se mahdollistaa verkko-, järjestelmä- ja sovellusturvallisuuden riskien jatkuvan pienentämisen.**

---
