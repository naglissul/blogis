# IT VBE template

createdAt: 2021-06-10

Senos programos (iki 2023 m.) informatikos VBE struktūros šablonas/konspektas.

Gražesnis šio puslapio informacijos formatavimas [čia, GitHub'e](https://github.com/naglissul/npw/blob/main/src/content/teach/sinopses/it-vbe-old.md).

## KLAUSIMAI

### Autoriaus teisės

#### Turtinės (iki savininko mirties ir 70 metų po):

- Kontroliuoti panaudojimą (leisti arba uždrausti atgaminti, leisti, keisti, kopijuoti ir tt),
- Gauti atlyginimą (už kiekvieną kūrinio panaudojimą)

#### Neturtinės (neterminuotai):

- Teisė į autoriaus vardą,
- Aurotystės teisė,
- Teisė į kūrinio neliečiamybę.

#### Objektai:

- Muzikos kūriniai
- Filmai
- Knygos
- t. t.

#### Ne objektai:

- Oficialūs valstybės simboliai ir ženklai (vėliava, herbas, himnas)
- Folkloro kūriniai
- Idėjos, procedūros, procesai...
- (dar keletas yra, bet aš šituos įsiminiau)

#### Teisėtai-neteisėtai-pasielgė klausimas (kai nusiprerka kažką ir pasidalina su draugais):

- Neteisėtai, nes įsigytą kūrinį galima naudoti tik asmeniniais tikslais, jo negalima platinti
  ARBA
- Teisėtai, nes įsigytą kūrinį galima platinti, jei tai leidžia pardavėjai.

### Saugumas

#### Prevention:

- Antivirusinės programos naudojimas (+ virusų duomenų bazės atnaujinimas)
- Ugniasienės (užkardos) naudojimas
- (daugiau yra, aišku, bet aš šituos įsiminiau)

#### Negeras laiškas:

- Vietoj temos - simbolių kratinys (arba nėra temos)
- Nenurodytas siuntėjas arba yra nepažįstamas
- Neįprasta kalba
- Daug klaidų (rašybos, gramatikos)
- Nuorodos į įtartinus šaltinius

#### Slaptažodis:

(Simbolių kiekis nežinau, googlas skirtingai rodo, bet bent 8 turėtų būt manau)

Recommended to include:

- a (maž raidės)
- A (didž raidės)
- ! (simboliai)
- 1 (skaičiai)

### Elektroninės valdžios vartai

#### Paslaugos:

- Elektroninis įvairių pažymų užsakymas
- Elektroninis prašymų teikimas
- Elektroninis gyvenamosios vietos deklaravimas

## WORDAS:

#### Rodyklė

Nuorodos -> Indeksas

1. pažymėt visą žodį - Žymeti įrašą (taip visiem žodžiams)
2. Įterpti indeksą

#### Nuoroda

Įterpimas -> Saitai

1. žodžio kairė pusė žymeklis - Žymelė
2. Hipersaitas

#### Išnašos

Nuodoros ->

#### Turinys

Nuorodos ->

## EXELIS

#### Filtras

1. Ant lentelės click
2. Duomenys -> Filtras
3. lentelės viršuj kur reik prie kurių reikia stulpelių rodyklytes spaust ir filtruot ten

#### Rūšiuoti

1. Ant lentelės click
2. Duomenys -> Rūšiuoti (ten jau ir tvarkytis viską)

#### Grafikas

Diagramos -> Dviejų reikšmių

## PROGRAMAVIMAS

### Pirma užduotis

```c++
#include <fstream>
using namespace std;

int func() {
    // funkcija pagal reikalavima
}

int main() {
    setlocale(LC_ALL, "Lithuanian");

    ifstream fd;
    ofstream fr;
    int n;
    int a[30], b[30]; // salygoj duota tas 30 ar kazks pns
    int i;
    //ir dar kiti reikalingi kintamieji

    //IVEDIMAS
    fd.open("U1.txt");
    fd >> n;
    for ( i = 0; i < n; i++) {
        fd >> a[i] >> b[i]; // ar kazkas panasaus, bet regis be teksto
        //galima ir struktūras naudot, bet pirmoj užduoty manau nelabai apsimoka
    }
    fd.close();

    //VEIKSMAI
    k = func(); //čia jau susikurt funkcija reiktu pagal reikalavimus
    // ir visokie veiksmai.

    //ISVEDIMAS
    fr.open("U1rez.txt");
    //isvedimas, cia manau nebus problemu, vel su tais for loopais
    fr.close();

    return 0;
}
```

### Antra užduotis

```c++
#include <fstream>
using namespace std;

struct dalykas {
    char vardas[21];
    //arba string vardas;
    int reiksme;
    //ar dar kazkas pagal konkretu atveji
};

void rikiavimas (int pirmas[], string antras[], int n) {
    int i, j;
    for (i = 0; i < n - 1; i++) {
        for (j = i; j < n; j++) {
            if (pirmas[i] > pirmas[j] or pirmas[i] == pirmas[j] and antras[i] > antras[j]) { //!!! > jei didėjimo tvarka, < jei mažėjimo
                swap(pirmas[i], pirmas[j]);
                swap(antras[i], antras[j]);
            }
        }
    }
}

void func() {
    // kokia dar ten pagal reikalavimus funkcija
}

int main() {
    setlocale(LC_ALL, "Lithuanian");

    ifstream fd;
    ofstream fr;
    int n;
    int k;
    dalykas a[30]; //pagal salyga tas 30
    //!!!jei struktūroje yra string:
    char zodis[21];
    //ir dar kiti reikalingi kintamieji

    //IVEDIMAS
    fd.open("U2.txt")
    fd >> n;
    fd.ignore();
    for (i = 0; i < n; i++) {
        //!!!jei strukturoj string:
        fd.get(zodis, 21);
        a[i].vardas = zodis;

        //!!!jei strukturoj char[]:
        fd.get(a[i].vardas, 21);

        fd >> a[i].reiksme; //ir kiti ivedimai
        fd.ignore();
    }
    fd.close();

    //VEIKSMAI
    rikiavimas();
    z = func();
    //kiti veiksmai

    //ISVEDIMAS
    fr.open("U2rez.txt");
    //isvedimo loopai
    fr.close();

    return 0;
}
```

### DIDELIS KOMENTARAS:

- jei naujoje eilutėje, kai skaitoma iš failo, yra skaitomas tekstas, nuskaitoma į char masyvą - reikia prieš tą skaitymą, buvusios eilutės pabaigoj, rašyti fd.ignore();
- kaip pačiame antros programos šablone parašiau !!! komentaruose, jei yra nuskaitomas string - reikia pirmiausia turėti kažkokį laikinai naudojamą kintamąjį - char masyvą. į jį nuskaitom su fd.get(); tekstą ir tuomet priskiriam tą tekstą tam string kintamajam; (jei įvedamas tekstas yra vienas žodis be tarpų, galima ir tiesiog įvesti kaip string, bet taip dar nemačiau egzaminų užduotyse kad būtų)
- string naudojam kai reikia rikiuoti;
- char[] naudojam kai tekstas su tarpais (galima sakyti visada 😃, todėl ir būna reikalingas tas konvertavimas iš char[] į string: char[] reikalinga įvedant tekstą su tarpais, string reikalinga rikiuojant)
- Antroje programoje bent jau man ne visada gaunas išlaikyti tokią tvarką (Įvedimas, veiksmai, išvedimas) ir tuomet susimaišo veiksmai su išvedimu ir įvedimu, kitaip sakant jau imant duomenis iš failo tvarkosi viskas ir veiksmai atliekami bei vos net iš iškart išvedami rezultatai gali būt (na, retai, retai taip man gaunas)
- Pirmoje programoje tvarką kaip ir gaunas išlaikyt man, todėl ir rašau iš eilės viską - įvedimas, veiksmai, išvedimas
