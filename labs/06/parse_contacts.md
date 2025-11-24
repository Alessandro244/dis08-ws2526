# Parsing contact information from the command line

## Extract all email addresses from the text.

```bash
grep -Eo "[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}" contacts.csv | awk '{print $0 "<br>"}' # br, damit in Markdown Zeilenumbruch entsteht
```

### Output
augue.ac@hotmail.couk<br>
adipiscing.lacus.ut@protonmail.net<br>
placerat.velit@protonmail.com<br>
sodales.elit@outlook.com<br>
tristique.neque@hotmail.org<br>
purus.in@yahoo.net<br>
a@yahoo.edu<br>
placerat@hotmail.net<br>
pede@protonmail.com<br>
eros.non.enim@icloud.edu<br>
sem.mollis@protonmail.edu<br>
dui.fusce.diam@hotmail.couk<br>
in.consequat@icloud.net<br>
in.lorem.donec@aol.ca<br>
dictum.eu@aol.edu<br>
placerat@hotmail.com<br>
tellus@google.net<br>
luctus.sit@outlook.org<br>
et.magnis@aol.edu<br>
mattis.semper@google.couk<br>
maecenas.libero.est@google.couk<br>
metus.in.lorem@outlook.ca<br>
nullam.velit.dui@aol.couk<br>
vestibulum.ante.ipsum@aol.com<br>
a.dui@protonmail.com<br>
phasellus.fermentum@hotmail.com<br>
massa.non@google.net<br>
nunc.pulvinar@hotmail.ca<br>
id.ante@hotmail.com<br>
nulla.integer.vulputate@icloud.edu<br>
suspendisse.sed.dolor@protonmail.couk<br>
mauris.non@protonmail.net<br>
enim@icloud.couk<br>
dui.nec@yahoo.net<br>
orci.ut@protonmail.com<br>
vel.nisl.quisque@aol.edu<br>
interdum@aol.ca<br>
amet.luctus.vulputate@google.ca<br>
ipsum.dolor.sit@aol.org<br>
nostra.per@aol.com<br>
ac.ipsum@yahoo.ca<br>
eu.enim.etiam@icloud.ca<br>
et.rutrum@icloud.couk<br>
convallis.convallis@yahoo.ca<br>
ipsum.primis@hotmail.org<br>
ac@aol.net<br>
aenean.massa@aol.edu<br>
phasellus@outlook.net<br>
pellentesque.massa@outlook.com<br>
malesuada@outlook.com<br>
massa@icloud.org<br>
id@google.net<br>
lacus.ut@protonmail.couk<br>
cursus.integer@hotmail.com<br>
sem.semper@hotmail.couk<br>
aenean.euismod@yahoo.org<br>
lobortis.class@yahoo.ca<br>
risus.donec@aol.net<br>
sagittis.placerat.cras@yahoo.com<br>
aliquam.adipiscing.lobortis@google.ca<br>
nullam@outlook.net<br>
sed.dictum@aol.net<br>
commodo.hendrerit@hotmail.couk<br>
non.magna@outlook.edu<br>
aenean@google.edu<br>
leo.vivamus.nibh@aol.org<br>
placerat.augue@aol.net<br>
montes.nascetur@icloud.couk<br>
auctor.quis.tristique@hotmail.org<br>
fermentum.fermentum@google.com<br>
sagittis.lobortis@hotmail.edu<br>
posuere.vulputate@icloud.com<br>
semper@icloud.org<br>
sit.amet@protonmail.couk<br>
senectus.et.netus@icloud.com<br>
cubilia.curae.phasellus@hotmail.net<br>
vitae.semper@google.org<br>
aliquet.molestie@protonmail.ca<br>
semper.auctor@yahoo.couk<br>
tristique.senectus@outlook.edu<br>
felis.purus.ac@protonmail.net<br>
mauris.sapien.cursus@icloud.org<br>
posuere.cubilia.curae@protonmail.couk<br>
cras@hotmail.ca<br>
aliquet.odio@yahoo.couk<br>
volutpat.nulla@google.net<br>
convallis.convallis@icloud.ca<br>
etiam.bibendum@hotmail.com<br>
odio@yahoo.edu<br>
eget.nisi@icloud.net<br>
sed.nunc@aol.couk<br>
dui.augue@outlook.org<br>
auctor.nunc@google.org<br>
est.ac@protonmail.edu<br>
at@yahoo.edu<br>
ultricies@yahoo.com<br>
aliquam@hotmail.org<br>
sed.pede.nec@aol.couk<br>
varius.nam.porttitor@protonmail.edu<br>
leo.morbi@aol.com<br>

## Extract all phone numbers from the text.

```bash
awk -F, 'NR>1 {print $NF}' contacts.csv | awk '{print $0 "<br>"}' # br, damit in Markdown Zeilenumbruch entsteht und mit awk einfach die letzte Spalte (Telefonnummern) geprintet ab Zeile>1 damit Spaltenname nicht mit dabei ist
```

### Output
(836) 811-6616<br>
(221) 605-4530<br>
(424) 937-3765<br>
(751) 973-6476<br>
(235) 444-8645<br>
1-216-210-2453<br>
1-498-278-1558<br>
1-668-811-3565<br>
1-400-336-6506<br>
(645) 267-2154<br>
(633) 561-2222<br>
1-946-737-5281<br>
1-323-567-8621<br>
(764) 385-4170<br>
(573) 457-2876<br>
1-703-319-7464<br>
1-388-313-1996<br>
(463) 754-2505<br>
(745) 151-1748<br>
(136) 311-1164<br>
1-445-247-4964<br>
1-832-643-6786<br>
(430) 249-1364<br>
(619) 782-3186<br>
(314) 352-5426<br>
1-781-822-4103<br>
(746) 275-2337<br>
(975) 531-7436<br>
1-406-523-1871<br>
(873) 788-9710<br>
1-762-979-5720<br>
1-648-738-4794<br>
(712) 943-2762<br>
1-152-482-1963<br>
(626) 124-2043<br>
(811) 308-2587<br>
(635) 457-8823<br>
1-897-878-2723<br>
(710) 187-2256<br>
(675) 372-1176<br>
(740) 362-4105<br>
(767) 708-7483<br>
(678) 955-5583<br>
1-324-652-0461<br>
1-614-767-1851<br>
(758) 738-8672<br>
1-403-632-6348<br>
1-628-537-7213<br>
(387) 415-4632<br>
1-236-479-3538<br>
1-111-205-4254<br>
(513) 848-1824<br>
(801) 923-6268<br>
(696) 773-5037<br>
1-298-228-9308<br>
(555) 767-3243<br>
(343) 698-0617<br>
1-852-835-9403<br>
1-127-824-4671<br>
(553) 534-2804<br>
1-485-516-7822<br>
(113) 393-3065<br>
(836) 763-3572<br>
1-745-788-9398<br>
(841) 768-0531<br>
(638) 185-3708<br>
1-613-182-8301<br>
1-555-600-4713<br>
1-517-442-9773<br>
(813) 856-5256<br>
(503) 606-1859<br>
1-379-352-9451<br>
1-638-850-8809<br>
1-867-232-7225<br>
1-452-216-8119<br>
1-615-465-5506<br>
(716) 111-7225<br>
(366) 231-7987<br>
1-938-513-2615<br>
1-607-566-7804<br>
(227) 715-5459<br>
(866) 170-3628<br>
(277) 572-2391<br>
1-756-534-6948<br>
(448) 542-7818<br>
(956) 351-3724<br>
(477) 415-3275<br>
1-869-798-0813<br>
1-868-331-1980<br>
(533) 237-8554<br>
1-301-323-0477<br>
1-788-814-5232<br>
1-681-363-6861<br>
(243) 677-3406<br>
(416) 844-3108<br>
(108) 368-3267<br>
1-455-448-1775<br>
(273) 843-5131<br>
(572) 547-5575<br>
(433) 308-6684<br>


## Extract all names that start with the letter 'J'.

```bash
grep -E '^J' contacts.csv | cut -d',' -f1 | awk '{print $0 "<br>"}' # br, damit in Markdown Zeilenumbruch entsteht und nur Namen die mit einem "J" beginnen sollen gefunden werden, String soll nur bis zum Komma (dort startet dann die nächste Spalte) ausgegeben werden
```

### Output
James Monroe<br>
John O'Neill<br>
Jameson Wallace<br>
Jamal Parsons<br>
Judah Branch<br>
Jaquelyn Le<br>
Jenna Herrera<br>

## Extract all street names that contain the word 'St'.

```bash
awk -F, 'NR>1 {adressen=$2; gsub(/^"|"$/,"",adressen); print adressen "<br>"}' contacts.csv # br, damit in Markdown Zeilenumbruch entsteht und zweite Spalte (Adressen) ausgeben, Anführungszeichen entfernen falls vorhanden weil ein , im String in der CSV die Anführungszeichen erzeugt, damit ein Komma in der Adresse nicht als Spaltentrenner interpretiert wird
```

### Output
413-2451 Lobortis<br>
2877 Nec Avenue<br>
Ap #350-8665 Ultricies Av.<br>
Ap #988-4035 Mi St.<br>
Ap #891-4549 Massa. St.<br>
799-5917 Erat St.<br>
P.O. Box 673<br>
5182 Penatibus St.<br>
P.O. Box 751<br>
Ap #458-8430 Rutrum Rd.<br>
Ap #271-6656 Sollicitudin Street<br>
771-1102 Sollicitudin Rd.<br>
Ap #788-4844 Curabitur Road<br>
8480 Amet Avenue<br>
987-6959 Interdum. Road<br>
1846 Quam Road<br>
9014 A Road<br>
P.O. Box 333<br>
8197 Et Avenue<br>
Ap #415-3325 Dapibus Rd.<br>
6564 Proin Street<br>
Ap #397-8170 Libero St.<br>
915-3764 Est St.<br>
P.O. Box 496<br>
P.O. Box 477<br>
6601 Eget Road<br>
P.O. Box 250<br>
4491 Vitae<br>
287 Velit. Avenue<br>
P.O. Box 462<br>
Ap #622-3257 Ultricies Road<br>
P.O. Box 113<br>
P.O. Box 778<br>
P.O. Box 101<br>
P.O. Box 352<br>
Ap #715-6617 Dolor Street<br>
319-379 Mi<br>
8059 Dui Av.<br>
106-627 Consequat St.<br>
Ap #373-3604 Mollis. Street<br>
669-6549 Morbi St.<br>
578-4253 Justo. Av.<br>
Ap #639-6437 Dolor. Street<br>
9647 Ipsum Road<br>
2537 Ornare<br>
6183 Nisl Rd.<br>
Ap #723-4802 Curae Avenue<br>
129-6019 Tellus Av.<br>
Ap #374-4908 Quam<br>
Ap #697-9528 Aliquet St.<br>
320-8453 Velit. Avenue<br>
573-117 Senectus Rd.<br>
377-9673 Quis Avenue<br>
Ap #486-9308 At<br>
Ap #854-4643 Sem<br>
6737 Gravida. Ave<br>
797-3522 Fames Rd.<br>
P.O. Box 872<br>
227-1473 Porttitor Street<br>
408-7191 Nec Street<br>
Ap #961-2908 Erat St.<br>
7445 Morbi Ave<br>
P.O. Box 245<br>
Ap #791-5007 Eget Rd.<br>
120-5863 At St.<br>
Ap #176-5922 Enim Rd.<br>
Ap #915-7067 Laoreet Ave<br>
P.O. Box 897<br>
4046 Ornare<br>
447-3645 Gravida Rd.<br>
6149 Ac Ave<br>
P.O. Box 830<br>
P.O. Box 283<br>
5837 Libero. Av.<br>
7360 Neque Street<br>
360-8053 Dapibus St.<br>
P.O. Box 434<br>
Ap #512-8744 Lectus Avenue<br>
Ap #555-4749 Nibh Rd.<br>
Ap #870-162 Donec Rd.<br>
Ap #506-313 Egestas<br>
167-9812 Curae Av.<br>
7087 Suscipit<br>
778-4032 Placerat<br>
P.O. Box 299<br>
Ap #146-8548 Sed St.<br>
P.O. Box 918<br>
P.O. Box 450<br>
9709 Quisque St.<br>
711-7689 Sit Ave<br>
Ap #806-7090 Massa. St.<br>
Ap #987-1774 Non Street<br>
P.O. Box 528<br>
6458 Ac Rd.<br>
Ap #667-423 Consequat Ave<br>
3445 Et Rd.<br>
P.O. Box 976<br>
P.O. Box 578<br>
Ap #479-1566 Parturient Rd.<br>
Ap #773-2384 Lacus. Road<br>

## Extract the last names of all people.
```bash
awk -F, 'NR>1 {split($1,nachname," "); print nachname[2] "<br>"}' contacts.csv # br, damit in Markdown Zeilenumbruch entsteht und String in Spalte 1 (wo der Name ist) beim Leerzeichen splitten und rest (Nachname) printen
```

### Output
Rios<br>
Patel<br>
Mckee<br>
Melendez<br>
Carter<br>
Patrick<br>
Holmes<br>
Hodge<br>
Monroe<br>
Osborn<br>
O'donnell<br>
Sellers<br>
Key<br>
Mcintyre<br>
Newman<br>
Ochoa<br>
Booker<br>
Mcbride<br>
Shannon<br>
Randolph<br>
Diaz<br>
Reed<br>
Mitchell<br>
Langley<br>
Brooks<br>
O'Neill<br>
Palmer<br>
Mcintosh<br>
Robertson<br>
Day<br>
Richards<br>
Parks<br>
Walsh<br>
Wallace<br>
Gill<br>
Wise<br>
Chang<br>
Simmons<br>
Oneil<br>
Mooney<br>
Castro<br>
Velez<br>
Reid<br>
Price<br>
Herman<br>
Hart<br>
Nunez<br>
Mclean<br>
Levy<br>
Cervantes<br>
Hyde<br>
Parsons<br>
Ortega<br>
Wilder<br>
Blankenship<br>
Vinson<br>
Morgan<br>
Torres<br>
Thornton<br>
Serrano<br>
Daniel<br>
Howe<br>
Hartman<br>
Winters<br>
Rivers<br>
Owen<br>
Head<br>
Branch<br>
Page<br>
Underwood<br>
Holloway<br>
Logan<br>
Rodgers<br>
Mcdaniel<br>
Waller<br>
Booker<br>
Osborne<br>
Cantu<br>
Carney<br>
Sanders<br>
Le<br>
Wise<br>
Hawkins<br>
Delaney<br>
Bradshaw<br>
Avery<br>
Boone<br>
Kinney<br>
Drake<br>
Meadows<br>
Cochran<br>
Hansen<br>
Richard<br>
Herrera<br>
Duffy<br>
Mcfadden<br>
West<br>
Cooley<br>
Leblanc<br>
Marks<br>

## Extract all email domains (part after the @ sign).

```bash
grep -Eo "[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}" contacts.csv | awk -F@ '{print $2 "<br>"}' # br, damit in Markdown Zeilenumbruch entsteht und Befehl aus der ersten Aufgabe, die alle Mailadressen ausgibt genommen und mit awk nur den Teil nach dem @ sign ausgegeben
```

### Output
hotmail.couk<br>
protonmail.net<br>
protonmail.com<br>
outlook.com<br>
hotmail.org<br>
yahoo.net<br>
yahoo.edu<br>
hotmail.net<br>
protonmail.com<br>
icloud.edu<br>
protonmail.edu<br>
hotmail.couk<br>
icloud.net<br>
aol.ca<br>
aol.edu<br>
hotmail.com<br>
google.net<br>
outlook.org<br>
aol.edu<br>
google.couk<br>
google.couk<br>
outlook.ca<br>
aol.couk<br>
aol.com<br>
protonmail.com<br>
hotmail.com<br>
google.net<br>
hotmail.ca<br>
hotmail.com<br>
icloud.edu<br>
protonmail.couk<br>
protonmail.net<br>
icloud.couk<br>
yahoo.net<br>
protonmail.com<br>
aol.edu<br>
aol.ca<br>
google.ca<br>
aol.org<br>
aol.com<br>
yahoo.ca<br>
icloud.ca<br>
icloud.couk<br>
yahoo.ca<br>
hotmail.org<br>
aol.net<br>
aol.edu<br>
outlook.net<br>
outlook.com<br>
outlook.com<br>
icloud.org<br>
google.net<br>
protonmail.couk<br>
hotmail.com<br>
hotmail.couk<br>
yahoo.org<br>
yahoo.ca<br>
aol.net<br>
yahoo.com<br>
google.ca<br>
outlook.net<br>
aol.net<br>
hotmail.couk<br>
outlook.edu<br>
google.edu<br>
aol.org<br>
aol.net<br>
icloud.couk<br>
hotmail.org<br>
google.com<br>
hotmail.edu<br>
icloud.com<br>
icloud.org<br>
protonmail.couk<br>
icloud.com<br>
hotmail.net<br>
google.org<br>
protonmail.ca<br>
yahoo.couk<br>
outlook.edu<br>
protonmail.net<br>
icloud.org<br>
protonmail.couk<br>
hotmail.ca<br>
yahoo.couk<br>
google.net<br>
icloud.ca<br>
hotmail.com<br>
yahoo.edu<br>
icloud.net<br>
aol.couk<br>
outlook.org<br>
google.org<br>
protonmail.edu<br>
yahoo.edu<br>
yahoo.com<br>
hotmail.org<br>
aol.couk<br>
protonmail.edu<br>
aol.com<br>

## Find all entries where the phone number ends with '7'.

```bash
awk -F, 'NR>1 {print $NF}' contacts.csv | awk '/7$/ {print $0 "<br>"}' # br, damit in Markdown Zeilenumbruch entsteht und Befehl aus der zweiten Aufgabe, die alle Telefonnummern ausgibt genommen und mit awk nur die Telefonnumern geprintet die mit einer 7 enden
```

### Output
(746) 275-2337<br>
(811) 308-2587<br>
(696) 773-5037<br>
(343) 698-0617<br>
(366) 231-7987<br>
1-301-323-0477<br>
(108) 368-3267<br>

## Extract all instances of first names that end with the letter 'e'.

```bash
awk -F, 'NR>1 {split($1,vorname," "); print vorname[1]}' contacts.csv | awk '/e$/ {print $0 "<br>"}' # br, damit in Markdown Zeilenumbruch entsteht und Befehl aus der Aufgabe genommen, die alle Nachnamen der Personen findet und Befehl so geändert das nur die Vornamen gefunden werden, die mit einem e enden
```

### Output
Vance<br>
Reese<br>
Kaye<br>
Bruce<br>
Brielle<br>
Brielle<br>
Kylie<br>
Reece<br>
Bree<br>
Cade<br>
Clare<br>





























