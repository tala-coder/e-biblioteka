# Specifikacije za završni projekat

# E-biblioteka 

## Uvod

Cilj ovog projekta je izrada web aplikacije E-biblioteka namjenjene za korištenje u školskim ustanovama. Aplikacija treba da omogući pristup za dva tipa korisnika i to, učenicima i školskim bibliotekarima. Učenicima će biti dostupan pregled svih raspoloživih knjiga u biblioteci kao i mogućnost rezervacije određene knjige. Bibliotekari će imati pristup bazi podataka sa mogućnošću uređivanja, dodavanja, brisanja te zaduživanja i razduživanja odabranih knjiga od strane učenika. Izradom ove aplikacije će biti značajno olakšan pristup korisnicima. Aplikacija će im biti dostupna u bilo kojem trenutku. Time će se ponuditi brži i fleksibilniji način u odnosu na postojeći sistem biblioteka. Svi podaci o zaduživanju i razduživanju će biti trajno arhivirani, a time će se korištenje papira i registara za evidenciju smanjiti na minimum.

## Detaljnije specifikacije

Bibliotekari i učenici se na web portal prijavljuju koristeći istu login stranicu, koja na osnovu korisničkog imena utvrđuje da li je riječ o bibliotekaru ili učeniku. Na osnovu toga provjerava ispravnost pristupnih parametara i kreira sesiju.

Ukoliko se korisnik prijavi u svojstvu bibliotekara, aplikacija treba da mu omogući da dodaje nove knjige, mijenja ili briše postojeće knjige iz baze, kao i da vrši zaduživanje i razduživanje knjiga učenicima. Svaka knjiga treba da bude uvrštena u određenu kategoriju, a pored opštih podataka treba da ima kratak opis i fotografiju korica. Potrebno je da se podaci o historiji zaduživanja/razduživanja evidentiraju trajno, kako ne bi došlo do gubitka podataka. Bibliotekari treba da imaju uvid u pojedinačno kretanje svake knjige, kao i da u svakom trenutku imaju pregled trenutno pozajmljenih knjiga, gdje se koja knjiga nalazi na zaduženju i kada treba da bude vraćena. Pored toga, treba da dobijaju statističke podatke oblika: koji naslovi su najtraženiji, koji autori najčitaniji, opterećenost svake pojedinačne knjige, broj izdavanja/pozajmljivanja tokom određenog vremenskog perioda. Nijedna knjiga ne može da se obriše iz baze, već može samo da se obilježi kao nedostupna u nekom od sljedećih svojstava: izgubljena, uništena ili nedostupna iz drugih razloga.

Ukoliko se korisnik prijavi u svojstvu učenika aplikacija treba da mu omogući pregled knjiga po kategorijama, mogućnost pretrage, kao i informaciju da li je knjiga trenutno raspoloživa ili ne. Pored toga, učenici treba da imaju pregled svojih trenutnih zaduženja. Za knjige koje su trenutno zadužene, učenik može da vidi očekivan datum kada knjiga treba da bude vraćena i može da napravi rezervaciju za trenutno pozajmljenu knjigu. Bibliotekar vidi rezervacije za knjigu te kada bude vraćena može je ostaviti u posebnoj sekciji za rezervisane knjige. Rezervacije traju jedan dan nakon čega im ističe rezervacija te bivaju selektirane za vraćanje na police, ukoliko nisu pozajmljene u toku tog dana onom učeniku koji je izvršio rezervaciju.

Grafički interfejs web sajta treba da bude realizovan sa responsive dizajnom, da bi korisnici mogli koristiti aplikaciju i preko mobilnih uređaja.

## Tehnologije

Aplikacija će biti realizovana na Node.js platformi korišćenjem Express biblioteke, a baza podataka će biti NoSql (MongoDB). Za postupak provjere identiteta korisnika koji upućuje zahtjeve back-end dijelu aplikacije koristit će se mehanizam sesija ili JWT (JSON Web Tokena). Grafički korisnički interfejs se generiše na strani klijenta (client side rendering), korišćenjem React biblioteke, dok podatke doprema asinhrono iz back-end dijela aplikacije (iz API-ja). Za dizajn grafičkog interfejsa aplikacije koristiti će se CSS biblioteke (Bootstrap CSS biblioteka). Izrada projekta i promjene kodova će biti praćene korištenjem alata za verziranje koda Git, a kôd aplikacije je dostupan na javnom Git spremištu (GitHub).


