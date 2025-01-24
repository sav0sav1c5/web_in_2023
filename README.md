# Projekat iz Web programiranja (WEB) - Platforma za praćenje pročitanih knjiga

## Opis
Ovaj repozitorijum sadrži kompletan materijal za timski projektni zadatak u okviru kursa **Web programiranje (2022/2023)**. Projekat predstavlja razvoj aplikacije koja omogućava korisnicima praćenje pročitanih knjiga, pisanje recenzija i kreiranje različitih lista knjiga (polica), po uzoru na **Goodreads**.

Aplikacija podržava funkcionalnosti za neprijavljene korisnike, čitaoce, autore i administratore, sa jasno definisanim ulogama i mogućnostima.

## Specifikacije projekta

### Model podataka

#### Korisnik
- Ime, Prezime
- Korisničko ime (jedinstveno)
- Mejl adresa (jedinstvena)
- Lozinka
- Datum rođenja
- Profilna slika
- Opis
- Uloga (Čitalac, Autor, Administrator)
- Police

**Dodatno za autora:**
- Status naloga (aktivan/neaktivan)
- Spisak knjiga

#### Knjiga
- Naslov, Naslovna fotografija
- ISBN
- Datum objavljivanja
- Broj strana
- Opis
- Žanr
- Ocena

#### Polica
- Naziv
- Primarna (da/ne)
- Stavke police

#### Recenzija
- Ocena
- Tekst
- Datum recenzije
- Korisnik

#### Zahtev za aktivaciju naloga autora
- Email, Telefon
- Poruka
- Datum
- Status (na čekanju/odobren/odbijen)
- Autor

### Funkcionalnosti korisnika

#### Neprijavljeni korisnik
- Pregled i pretraga knjiga, recenzija, žanrova i korisničkih profila.
- Registracija (kreira se profil čitaoca).
- Podnošenje zahteva za aktivaciju naloga autora.

#### Čitalac
- Upravljanje primarnim i korisnički definisanim policama.
- Dodavanje recenzija za pročitanih knjige.
- Ažuriranje profila.

#### Autor
- Funkcionalnosti čitaoca.
- Dodavanje i ažuriranje knjiga koje je autor napisao.

#### Administrator
- Dodavanje autora u sistem i upravljanje zahtevima za aktivaciju naloga autora.
- Upravljanje knjigama i žanrovima.
- Ažuriranje profila neaktiviranih autora.

## Struktura Projekta

- `WEB/` - Backend implementacija u Javi koristeći Spring Boot.
- `FRONT/` - Frontend implementacija u HTML, CSS i opciono JavaScript/Vue.js.

## Pokretanje Projekta

1. Klonirajte repozitorijum:
   ```bash
   git clone <repo_url>
   ```
2. Pokrenite backend aplikaciju:
   - Otvorite terminal u folderu `BACK` i pokrenite aplikaciju koristeći:
     ```bash
     mvn spring-boot:run
     ```
   - Aplikacija će se pokrenuti na adresi `http://localhost:8080`.
   - Pristupite H2 konzoli na `http://localhost:8080/h2` koristeći:
     ```
     Username: sa
     Password: admin
     ```
3. Pokrenite frontend aplikaciju:
   - Otvorite terminal u folderu `FRONT` i pokrenite server koristeći:
     ```bash
     npm start
     ```
   - Pristupite aplikaciji u pretraživaču na adresi prikazanoj u terminalu.

## Podaci za logovanje

**Administrator:**
- Email: milka123@gmail.com
- Lozinka: milka32

## Autori
- **Nikola Radojčić IN12/2021**
- **Savo Savić IN50/2021**

Projekat izrađen kao deo kursa **Web programiranje (WEB)**.