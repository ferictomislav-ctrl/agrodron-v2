# AgroDron – isplativost na vlastitom gospodarstvu

Samostalna aplikacija na hrvatskom za usporedbu postojeće traktorske prskalice, kombinacije s jednim DJI Agras T100, jednog T100 i dvaju T100. Isključivo vlastita proizvodnja; bez prihoda od uslužnih poslova.

## Otvaranje bez instalacije

1. Preuzmite repozitorij preko **Code → Download ZIP** i raspakirajte ga, ili preuzmite `index.html` preko gumba **Download raw file** u GitHubovu prikazu datoteke.
2. Otvorite `index.html` dvostrukim klikom u suvremenom pregledniku. Internet, poslužitelj, biblioteke i API ključevi nisu potrebni.
3. Unesite svoje podatke. Prazno nije nula. Početne cijene opreme već su unesene, nepoznati poslovni podaci su prazni.
4. Izvezite JSON za sigurnosnu kopiju. Automatsko spremanje vrijedi samo za konkretan preglednik i lokaciju datoteke; preglednik ga može ograničiti.
5. Za PDF odaberite **Ispis / PDF → Spremi kao PDF**.

Gumb **Ilustrativni primjer** učitava izmišljene operativne podatke uz potvrdu. Možete uvesti i priloženi `primjer.json`. Ti podaci nisu potvrđena izvedba T100 niti preporuka za kupnju.

## Metodologija

- Fizički hektari odvojeni su od godišnjih tretiranih hektara. Kulture se zbrajaju do fizičke površine.
- Raspodjela po tretmanu: stvarni dron + vlastita prskalica + redovna vanjska usluga + zamjenska usluga = površina tretmana.
- Kvar prebacuje odabrani udio planirane dronske površine na zamjensku službu. Ta površina ne stvara trošak rada i baterijskog trošenja drona.
- B podržava paralelan rad odvojenih ekipa ili uzastopan rad zajedničke ekipe. C i D konzervativno zbrajaju faze. Provjera je po pojedinom tretmanu; preklapanja različitih tretmana nisu automatski raspoređena.
- Neto ulaganje uključuje nepovrativi PDV i primitak prodaje prskalice. Bruto plaćanje opreme, neto ulaganje i subvencija prikazani su zasebno. Traktor se ne prodaje.
- Godišnji operativni novčani trošak ne uključuje amortizaciju niti procijenjeno trošenje baterija. Stvarne kupnje baterija ulaze u višegodišnji prikaz prema zasebnom rasporedu. Raspored mora biti potvrđen za svaki scenarij; za plan bez zamjena unesite red s 0 komada.
- Ekonomski trošak uključuje amortizaciju bez baterija te procijenjeno trošenje baterija jednom. Subvencija ne mijenja amortizaciju.
- Jednostavni povrat koristi novčanu operativnu uštedu. Posebno je prikazan povrat uz dodatne koristi. Višegodišnji tok ne uključuje dodatne koristi, diskontiranje, inflaciju, financiranje ili završnu prodaju.
- Operativne cijene i zamjene baterija unosite kao ekonomske cijene nakon odbitka povrativog PDV-a. Porezne stope u postavkama primjenjuju se na investiciju.
- Rezervna prskalica ostaje neaktivna uz svoje fiksne troškove i amortizaciju; vanjska zamjena je izričiti korisnički odabir. Da biste planirali vlastitu prskalicu u radu, koristite B.
- Nema automatske pretpostavke o dopuštenosti primjene, nižoj dozi sredstava, jednakoj učinkovitosti ni dvostrukom učinku dva drona.

## Provjera

Provjereno u Chromiumu preko lokalnog HTTP poslužitelja: prikaz na 1440 i 390 px, automatski unos i izračun, spremanje i ponovno učitavanje, izvoz i uvoz JSON-a, vraćanje početnih vrijednosti uz potvrdu te odsutnost JavaScript grešaka i mobilnog vodoravnog prelijevanja. Pregledani su snimci prikaza.

Provjerene računice: 26.776,70 € osnovni paket, 35.966,70 € s opcijama, dodatnih 21.268 € za drugi komplet, 5.000 tretiranih ha u primjeru, raspodjela površina, PDV i odbitak, subvencija, prodaja, negativna ušteda, prazni i nulti unosi, trošenje baterija, neispravni udjeli i pojedinačni rokovi. Aplikacija nema vanjske mrežne ovisnosti. Izravna navigacija na `file://` blokirana je administrativnom politikom testnog preglednika, pa izravno otvaranje te adrese u tom okruženju nije potvrđeno. Funkcionalnost samostalnog preuzetog HTML-a provjerena je učitavanjem njegova sadržaja bez vanjskih zahtjeva.

Test računica bez dodatnih paketa: `node tests.cjs`. Node nije potreban za rad aplikacije.

## Dostupnost

Ovo je izvorni kod i datoteka za preuzimanje, a ne potvrđena javno objavljena aplikacija. GitHub Raw nije hosting aplikacije. U okruženju nedostaju izvršne skripte Sites potrebne za podržano pakiranje i objavu, pa objava nije dovršena. Lokalni rad aplikacije ne ovisi o objavi.
