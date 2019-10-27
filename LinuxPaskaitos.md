Paskaita 1
Paskaita 2
Darbas su vi redaktoriumi
Vi yra komandų eilutės teksto rengyklė. „Vi“ yra skirta kaip paprasto teksto rengyklė (panaši į „Notepad“ „Windows“ arba „Textedit“, „Mac“), priešingai nei teksto apdorojimo rinkinys, toks kaip „Word“ ar „Pages“. Tačiau ji turi daug daugiau galios, palyginti su „Notepad“ ar „Textedit“.
VI redaktorius turi tris režimus:
1.Komandinis- šiame režime galima naršyti po failą ir vykdyti teksto redagavimo komandas. 
2.Teksto įvedimo - šiuo režimu į tekstą bus įterpiamos paprastos lotyniškos raidės.
3.Ed- režimas naudojamas valdyti failai (pvz., išsaugoti failą, perskaityti failą ir kt.)
vi failo vardas
Vi komandiniame režime:
ESC:q! Enter - išeiti iš failo neišsaugoję
ESC:w! Enter - išeiti iš failoe išsaugoję pakeitimus
ESC:q  Enter - baigti darbą
ESC:wq Enter - išeiti iš failo išsaugodami
Norėdami pereiti į įvesties režimą, turime  paspausti tokias komandas:
„i“ aktyvuoja redagavimą 
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
o įterpti iš naujos eilutės (po dabartine eilute)
a įvesties režimu už žymeklio
5yy atsiminti 5 eilutes
Perkelkite žymeklį į norimą vietą
      p įdėti įsimintas eilutes po žymekliu
      P įdėti  įsimintas eilutes per žymeklį

      J Klijuoti  dvi eilutes
      / Įvesti  paieškos modelį - ieškokite
      n Pakartoti paiešką
d sunaikinti fragmentą
y įsiminti fragmentą
! komanda perduoti fragmentą per filtrą
? linija ieškoti aukstyn
/ linija žiūrėti žemyn
n pakartoti paiešką
N grįžti į paskutinę rastą eilutę


    
Paskaita 3
Paskaita 4
Paskaita 5
Procesai
 Procesas- abstrakcija, kuria pasiule Linux OS kurejai,duodanti galimybe stebeti ir valdyti keliu vienu metu  vykdomu programu darba.
 Fiziskai proceso atvaizda sudaro:vykdomasis programos kodas,duomenys (kintamieji ir tt.),busenos ar konteksto informacija (duomenys,reikalingi procesui restauruoti, neprarandant informacijos).
 Naujas procesas yra sukuriamas naudojant sistemines funkcijos  komanda "fork()"(kadangi tai vienintelis vartotojo budas sukurti nauja procesa operacineje sistemoje UNIX), jos issaukimo sintakse "pid=fork()".Sios funkcijos ivykdymo rezultate abieju procesu(tevo, vaiko) kontekstas sutampa, isskyrus kintamojo PID  griztamaja reiksme(tevui- vaiko proceso identifikatorius, vaikui- PID  yra nulines reiksmes).Branduolio veiksmai tuo metu1:1.Islaisvina procesu lenteleje vieta naujam procesu.
2.Priskiria procesui-vaikui unikalu identifikacijos koda (PID).
3.Atlieka proceso-tevo konteksto logine kopija.
4.Padidina failu(susijusiu su procesu) skaiciaus skaitiklio reiksmes failu, indeksu lentelese.
5. Grazina procesui-tevui proceso-vaiko identifikacijos koda, o procesui-vaikui nuline reiksme.
  Tai yra: branduolys iesko vietos procesu lenteleje proceso-vaiko kontekstui konstruoti ir tikrina ar vartotojas nevirsijo maksimaliai leistino lygiagreciai paleistu procesu skaiciaus apribojimo.Branduolys priskiria naujam procesui nauja unikalu identifikatoriu. 
  Kai procesai vyksta vienu laiku, tada jiems uzdedamas skaiciaus apribojimas ir ne vienas vartotojas negali uzimti procesu lenteleje per daug vietos, trukdant kities vartotojams kurti naujus procesus.
Toliau branduolys priskiria nulines reiksmes procesu lentelems irasu laukams. Po to jis skiria atminti proceso erdvei(jo puslapio lentelems ir sritims), kuria algoritmo pagalba proceso-tevo sriciu kopijas prijungia kiekviena sriti prie proceso-vaiko. Baigiasi statine proceso konteksto dalis ir kuriamas dinaminis (procesas-tevas baigia atlikineti fork, naujas procesas jau gali pasileisti).
https://www.slideshare.net/donatasbukelis/operacines-sistemos-teorija
Paskaita 6
