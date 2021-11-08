**Attribuutti**
Luokan sisällä oleva muuttuja. Epätarkka termi, katso myös kenttä (field) ja ominaisuus (property)
```java
public class Ihminen{

public String nimi;
int ika;

}
```

**CharAt**

**Class**
Tietojen "yläluokka". Tämän sisälle luodaan metodit, muuttujat etc. Luokan nimen tulee olla myös tiedostonnimenä, muuten tiedostoa ei ajeta. Class-tietoja voi olla vain yksi/tiedosto. 
```java
public class Ihminen{
//kaikki tämän luokan sisällä olevat asiat kuuluvat samaan luokkaan
//tästä tehdään tietosto nimeltä "Ihminen"
}
````

**Equals**
equals() on boolean-tyyppisen arvon palauttava metodi, joka vertaa kahta samaa tyyppiä olevaa objektia keskenään ja kertoo, ovatko ne sama objekti. Metodi on peritty Object-luokasta, ja sen toimintatapa riippuu metodin toteuttavasta luokasta. Yleinen käyttötarkoitus on String-tyyppisten objektien vertailu.
```java
boolean totuusArvo = true;
String nimi1 = "Teppo";
String nimi2 = "Seppo";
String nimi3 = "Teppo";
totuusArvo = nimi1.equals(nimi2);
//totuusArvo-muuttujan arvo on nyt false, koska String-objektit eivät ole sisällöltään samanlaiset
totuusArvo = nimi1.equals(nimi3);
//totuusArvo-muuttujan arvo on nyt true, koska String-objektit ovat sisällöltään samanlaiset
```

**For**
Toistorakenne, jossa toistetaan aaltosulkeiden {} sisällä määriteltyä koodilohkoa kaarisulkeiden () sisällä määriteltyjen sääntöjen mukaan.
```
for(lause 1; lause 2; lause 3){
//Aaltosulkeiden sisäpuolella koodia
}
```
Lause 1 suoritetaan vain kerran, ennen kuin toisto alkaa.
Lause 2 määrittelee ehdon, jonka toteutuessa aaltosulkeiden {} sisältö toistetaan. Jos ehto on tarkistettaessa epätosi, toisto päättyy.
Lause 3 suoritetaan jokaisen toiston jälkeen.
```java
for(int i = 0; i < 10, i++){
//Tätä pätkää tehdään 10 kertaa
}
```

**IDE**
IDE, integrated development environment eli ohjelmointiympäristö on ohjelma tai ohjelmistopaketti, joka toimii ohjelmoinnin työkaluna. Yksinkertaisimmillaan IDE voi sisältää vain tekstieditorin ja ohjelmointikielen kääntäjän. Moderni IDE kuitenkin yleensä sisältää monia muita ominaisuuksia, kuten debuggaustyökaluja, koodivirheiden automaattista korostamista sekä ennakoivaa kirjoittamista.

**If**
Valintarakenne. 
```java
int x = 1;
if(x == 1){
//if-lauseen sisälle määritelty ehto palauttaa toden, suoritetaan tämä koodinpätkä
}

x = 2;
if(x == 1){
//if-lauseen sisälle määritelty ehto palauttaa epätoden, tätä ei suoriteta
}
```

**Else**
If-lauseen jälkeen on mahdollista sijoittaa else-avainsanan perään uusi koodilohko, joka toteutetaan jos if-lause palautti epätoden.
```java
if(x == 1){
//Tehdään tämä koodinpätkä
}
else{
//Tehdään tämä koodinpätkä
}
```

**Käyttäjätietojen kysyminen**
Katso "Print"

**Käyttäjätietojen tallentaminen**
Katso "Scanner"

**Luokka**
Katso "Class"

**Main**

**Math.random**

**Merkkijono**
String-tyypin olio. Voi myös joissain tilanteissa viitata char-tyyppiseen taulukkoon char[], jota voi pitää hyvin kirjaimellisesti merkkien jonona.

**Metodi**
Luokan sisällä oleva funktio. Javassa kaikkien funktioiden tulee olla jonkin luokan sisällä, joten tässä kontekstissa funktio ja metodi ovat synonyymejä. Tässä wikissä javan funktioista käytetään sekaannuksen välttämiseksi ainoastaan termiä metodi.

Metodi on koodilohko, joka suoritetaan vain silloin, kun metodia kutsutaan. Alla esimerkki mahdollisimman yksinkertaisesta metodista:
```java
void static printStuff(){
        System.out.println("Stuff");
    }
```
Oletetaan että metodi on luokan TestClass sisällä. Tätä metodia voidaan silloin kutsua seuraavasti:
```java
TestClass.printStuff();
```
Jos metodi kirjoitettaisiin ilman static-avainsanaa, olisi printStuff() -metodi ns. instanssimetodi. Tämä tarkoittaa sitä, että päästäksemme metodiin käsiksi on ensin luotava ilmentymä (olio/object/instance) luokasta TestClass. Metodikutsu tapahtuisi silloin seuraavasti:
```java
TestClass ilmentymaTestClassista = new TestClass(); //Tässä luodaan ilmentymä TestClassista, nimellä "ilmentymaTestClassista"
ilmentymaTestClassista.printStuff(); //Tässä kutsutaan luomamme ilmentymän kautta TestClass-luokkaan kirjoitettua metodia printStuff()
```

**Muuttuja**
Muuttuja (variable) on nimetty säiliö, johon voidaan tallentaa dataa. Muuttujalle täytyy antaa luomisvaiheessa tyyppi ja nimi. Muuttujan voi joutua myös alustamaan; muuttujan alustaminen (initialization) tarkoittaa jonkin arvon asettamista muuttujaan ensimmäisen kerran. Yleisesti näin tehdään, jotta vältyttäisiin null-arvon sisältävän muuttujan käsittelyltä.
```java
int luku; //Tätä muuttujaa ei ole alustettu, joten sen arvo on tällä hetkellä null. Null-arvon käsittelemisen yrittäminen voi aiheuttaa virheitä.

char charEsimerkki = 'A';
//tyyppi = char, nimi = charEsimerkki
double doubleEsimerkki = 1,23;
//tyyppi = double, nimi = doubleEsimerkki
int intEsimerkki = 1;
//tyyppi = int, nimi = intEsimerkki
String stringEsimerkki = "Esimerkki";
//tyyppi = String, nimi = stringEsimerkki
```
*(vrt attribuutti)*

**Olio**
Luokan ilmentymä (instance). Kirjoitetaan seuraavanlainen luokka:
```java
public Class Ihminen{

        public String nimi;
        public int ika;
        
//Alla on yksinkertainen konstruktori, jolla voidaan asettaa luokan muuttujiin arvoja kun luokasta luodaan ilmentymä.
        public Ihminen(String nimi, int ika){
                this.nimi = nimi;  
                this.ika = ika;    
                
/*this-avainsana mahdollistaa kahden samannimisen muuttuja tunnistamisen erillisinä. This-avainsanalla merkitty "nimi" -muuttuja viittaa nyt muuttujaan, joka on määritelty jo aiemmin tässä luokassa. Näin se tunnistetaan erillisenä "nimi" -nimisestä parametrista, joka konstruktorille on annettu.*/
        }     
}
```
Ilmentymän tästä luokasta voimme luoda seuraavasti:
```java
Ihminen Jari = new Ihminen("Jari Uimonen", 45)
```

**Osajoukko**
Tietty osa merkkijonosta. 
Esimerkki <- merkkijono
mer <- osajoukko

**Print**
Tulostetaan haluttuja tietoja
`System.out.print("Hei kaikki");`

**Päämetodi**

**Scanner**
Tietojen lukuun käytettävä valmisluokka
```java
Scanner esimerkki = new Scanner(System.in)
System.out.print("Mitä kuuluu")
String esimerkki = esimerkki.nextLine();
```

**String.length()**
String-luokan metodi, joka palauttaa merkkijonon pituuden.
```java
String esimerkkiString = "Esimerkki";
int pituus = esimerkkiString.length();
//pituus == 8 merkkiä
```

**Taulukko**
Taulukon (array) avulla voidaan tallentaa useampi samaa tyyppiä oleva arvo yhteen muuttujaan. Taulukon kokoa ei ole mahdollista muuttaa sen luomisen jälkeen. Taulukoita luodaan ja käytetään hakasulkeiden [] avulla.
Esimerkkejä tavoista luoda taulukkoja:
```java
String[] esimerkkiString = {"Jepa", "jepa", "jee"};
//String-tyypin olioita sisältävä taulukko, sisältää 3 String-oliota. Olemassaolevat indeksit ovat siis esimerkkiString[0], esimerkkiString[1] ja esimerkkiString[2]
                                                    
int[] lukuTaulukko;
//tämä taulukko on muodostettu teknisesti oikein mutta sen koko on 0, koska sille ei ole annettu mitään kokoa luontivaiheessa. Taulukkoon ei siis voida koskaan tallentaa mitään. Älä tee näin.

int[] lukutaulukko2 = new int[10]; //Tämä taulukko on muodostettu oikein. Sen koko on 10. Koska taulukon alkioihin ei ole sijoitettu mitään arvoja, java antaa int-tyypin alkioille oletusarvoksi 0. Tämä poikkeaa paikallisen muuttujan luomisesta siten, että oletusarvo ei tällä kertaa olekaan null, ks. "Muuttuja"-termin esimerkin ensimmäinen rivi.
```
Taulukkoja voidaan käydä läpi toistorakenteiden avulla. Tässä esimerkki yllä olevan esimerkkiString-taulukon läpikäymisestä for-loopin avulla:
```java
for(int i = 0; i < esimerkkiString.length(), i++){
        System.out.println(esimerkkiString[i]);     //Jokaisella kierroksella printataan taulukon indeksin i arvo.
        esimerkkiString[i] = esimerkkiString[i] + " loopattu" //Muutetaan jokaista alkiota lisäämällä tekstiä perään.
}
```
Nyt esimerkkiString-taulukon jokaisen stringin perässä lukee myös "loopattu".

**Tietojen vertailu**
Kun halutaan vertailla primitiivien (int, short, long, float, double, char, byte, boolean) yhtäläisyyttä, voidaan käyttää operaattoria ==
```java
int i = 1;
int j = 2;
boolean ovatkoSamat = i == j;
//ovatkoSamat on epätosi
```
Javassa String ei ole primitiivi vaan luokan ilmentymä, joten sitä ei voida vertailla samalla operaattorilla. String-tyypin, kuten muidenkin oliotyyppien, vertailuun käytetään esimerkiksi instanssimetodia .equals()
```java
String a = "Aapelinmäki";
String b = "Aapelinmäki";

boolean ovatkoSamat = a == b;
boolean ovatkoSamatEquals = a.equals(b);

//ovatkoSamat on epätosi, sillä == operaattori tarkistaa, ovatko a ja b samassa muistiosoitteessa ja siten täsmälleen sama objekti. Näin ei ole.
//ovatkoSamatEquals on tosi, sillä .equals() tarkastelee String-olioiden sisältöä ja toteaa niiden olevan samanarvoisia.
```
Katso "Equals" ylempää nähdäksesi toisen esimerkin.

**Toistaminen**
Katso "for" ja "while"

**While**
Toistetaan tiettyä koodia niin kauan, kunnes kaarisulkeissa määritetty ehto ei enää täyty.
```java
while(int a != 0){
        System.out.print("Anna numero");
        a = scan.nextInt;
}
```
