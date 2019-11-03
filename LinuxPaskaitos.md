#Paskaita 1
#Paskaita 2
#Paskaita 3
##Darbas Su Vi Redaktoriumi##
VI yra komandų eilutės teksto rengyklė. „Vi“ yra skirta kaip paprasto teksto rengyklė (panaši į „Notepad“ „Windows“ arba „Textedit“, „Mac“), priešingai nei teksto apdorojimo rinkinys, toks kaip „Word“ ar „Pages“. Tačiau ji turi daug daugiau galios, palyginti su „Notepad“ ar „Textedit“.
VI REDAKTORIUS TURI TRIS REŽIMUS:
1.Komandinis- šiame režime galima naršyti po failą ir vykdyti teksto redagavimo komandas. 
2.Teksto įvedimo - šiuo režimu į tekstą bus įterpiamos paprastos lotyniškos raidės.
3.Ed- režimas naudojamas naudotis failu (pvz., išsaugoti failą, perskaityti failą ir kt.)
vi failo vardas
VI KOMANDINIAME REŽIME:
ESC:q! Enter - išeiti iš failo neišsaugoję
ESC:w! Enter - išeiti iš failoe išsaugoję pakeitimus
ESC:q  Enter - baigti darbą
ESC:wq Enter - išeiti iš failo išsaugodami
Norėdami pereiti į įvesties režimą, turime  paspausti tokias komandas:
„i“ aktyvuoti redagavimą 
„A“ intarpas nuo eilutės pabaigos
„cw“ pakeisti dabartinį žodį
ESC GRĮŽTI Į KOMANDOS REŽIMĄ
CTRL- [grįžti į komandos režimą
norėdami pereiti į Failų tvarkymo režimą, paspauskite
    ":" (perjungti į ED redagavimo režimą)
Galima judėti po failą komandomis:
h, j, k, l kairėn, žemyn, aukštyn, dešinėn
„Ctrl-F“ puslapis žemyn
„Ctrl-B“ puslapis aukštyn
Dar kelios naudingos komandos:
o įterpti iš naujos eilutės 
a įvesties režimas už žymeklio
5yy atsiminti 5 eilutes
Perkelkite žymeklį į norimą vietą
      p įdėti įsimintas eilutes po žymekliu
      P įdėti  įsimintas eilutes per žymeklį

      J Klijuoti  dvi eilutes
      / Įvesti  paieškos modelį - ieškokite
      n Pakartoti paiešką
d panaikinti fragmentą
y įsiminti fragmentą
! komanda perduoti fragmentą per filtrą
? linija ieškoti aukstyn
/ linija žiūrėti žemyn
n pakartoti paiešką
N grįžti į paskutinę rastą eilutę

 <a href="http://lib.ru/unixhelp/vibegin.txt">
 <a href="https://neoserver.ru/help/osnovnie-komandi-redaktora-vi-vim">


#Paskaita 4
#Paskaita 5
##Procesai##
  PROCESAS- abstrakcija, kurią pasiūlė Linux OS kūrėjai,duodanti galimybę stebėti ir valdyti kelių vienu metu  vykdomų programų darbą.
  Fiziškai proceso atvaizdą sudaro:VYKDOMASIS PROGRAMOS KODAS,DUOMENYS (KINTAMIEJI IR TT.),BŪSENOS AR KONTEKSTO INFORMACIJA (DUOMENYS,REIKALINGI PROCESUI RESTAURUOTI, NEPRARANDANT INFORMACIJOS).
 Naujas procesas yra sukuriamas naudojant sisteminės funkcijos  komandą "fork()"(kadangi tai vienintelis vartotojo būdas sukurti naują procesą operacinėje sistemoje UNIX), jos iššaukimo sintaksė "pid=fork()".Šios funkcijos įvykdymo rezultatei abiejų procesų(tėvo, vaiko) kontekstas sutampa, išskyrus kintamojo PID  grįžtamąja reikšme(tėvui- vaiko proceso identifikatorius, vaikui- PID  yra nulinės reikšmės). BRANDUOLIO VEIKSMAI TUO METU:
1. Išlaisvina procesų lentelėje vietą naujam procesui.
2. Priskiria procesui-vaikui unikalų identifikacijos kodą(PID).
3. Atlieka proceso-tėvo konteksto loginę kopiją.
4. Padidina failų(susijusių su procesu) skaičiaus skaitiklio reikšmes failų, indeksų lentelėse.
5. Grąžina procesui-tėvui proceso-vaiko identifikacijos kodą, o procesui-vaikui nulinę reikšmę.
  Tai yra: branduolys ieško vietos procesų lentelėje proceso-vaiko kontekstui konstruoti ir tikrina ar vartotojas neviršijo maksimaliai leistino lygiagrečiai paleistų procesų skaičiaus apribojimo.Branduolys priskiria naujam procesui naują unikalų identifikatorių. 
  Kai procesai vyksta vienu laiku, tada jiems uždedamas skaičiaus apribojimas ir ne vienas vartotojas negali užimti procesų lentelėje per daug vietos, trukdant kities vartotojams kurti naujus procesus.
Toliau branduolys priskiria nulines reikšmes procesų lentelėms įrašų laukams. Po to jis skiria atmintį proceso erdvei(jo puslapio lentelėms ir sritims), kuria algoritmo pagalba proceso-tėvo sričių kopijas, prijungia kiekvieną sritį prie proceso-vaiko. Baigiasi statinė proceso konteksto dalis ir kuriamas dinaminis (procesas-tėvas baigia atlikinėti fork, naujas procesas jau gali pasileisti).

<a href="https://www.slideshare.net/donatasbukelis/operacines-sistemos-teorija">
#Paskaita 6
