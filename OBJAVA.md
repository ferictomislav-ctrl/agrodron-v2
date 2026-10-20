# Objava postojeće aplikacije bez promjene izračuna

`index.html` ostaje identičan izvornoj provjerenoj aplikaciji. U korijenu je dodana prazna datoteka `.nojekyll` za posluživanje postojećeg statičkog sadržaja bez Jekyll obrade. Instalacija i build nisu potrebni.

## Trenutačno stanje

Repozitorij je privatni. Nije promijenjena vidljivost, paket ni naplata. Nije potvrđena HTTPS objava. Dostupna GitHub integracija nema operacije za Pages postavke, a pokušaj čitanja Pages API-ja iz okruženja vratio je `Forbidden`. To nije dokaz da korisnikov GitHub paket ne podržava Pages: pravo na Pages za privatni repozitorij treba provjeriti u korisničkom sučelju.

Sites izvršne skripte nedostaju; prethodni neuspješni postupak nije ponavljan. Drugi pronađeni servisi za objavu (Vercel i Render) nisu povezani s ovim razgovorom.

## Prvi korak

Prijavite se u GitHub i otvorite:
https://github.com/ferictomislav-ctrl/agrodron-v2/settings/pages

Provjerite prikazuje li se odjeljak **Build and deployment** ili poruka koja traži promjenu paketa/vidljivosti. Ako GitHub zahtijeva nadogradnju, nemojte je aktivirati i nemojte mijenjati privatnost repozitorija. Vratite se u razgovor i prenesite prikazanu poruku.

## Postavke ako ih postojeći paket dopušta

- Source: **Deploy from a branch**.
- Branch: **main**.
- Folder: **/ (root)**.
- Save.

Ne treba dodavati GitHub Actions workflow ni mijenjati aplikaciju. Pričekajte da Pages u postavkama prikaže stvarnu adresu objavljene stranice. Ta je adresa mjerodavna; ne treba nagađati URL.

Napomena: privatnost izvornog repozitorija i vidljivost objavljene web stranice nisu ista postavka. Klasičan Pages može javno posluživati stranicu čiji je izvor u privatnom repozitoriju. Poslovni unosi ove aplikacije pohranjuju se lokalno u pregledniku, a izvezeni JSON ne dodaje se u repozitorij automatski.

## Provjera nakon objave

1. Otvoriti stvarnu HTTPS adresu i potvrditi da prikazuje kalkulator, a ne GitHub datoteku ili 404.
2. Učitati ilustrativni primjer uz potvrdu, promijeniti brojčani unos i potvrditi promjenu rezultata.
3. Provjeriti prikaz na računalnoj i mobilnoj širini.
4. Ponovno potvrditi da je repozitorij ostao privatni.

Do završetka ovih provjera ne treba tvrditi da je aplikacija objavljena i provjerena.
