# 💪 IronZone Gym — Grupni projekt

**Grupa C · 3 učenika · Bootstrap završni projekt**

---

## 📋 O projektu

Izrađujete web stranicu za fiktivni fitnes centar **IronZone** .
Stranica mora izgledati snažno, moderno i motivirajuće — ciljna publika su sportaši i rekreativci.

> ⚠️ **Napomena:** Ovaj projekt koristi isključivo HTML, CSS i Bootstrap.
sve interaktivnosti (modal, hamburger, accordion)
> rade kroz Bootstrap `data-bs-*` atribute.

> **Napomena za grupu od 3:** Svaki učenik dobiva nešto više posla nego u grupama od 4. Lead Developer radi navigaciju, hero i kontakt. Ostala dva člana dijele sadržajne sekcije.

---


Sve interaktivnosti dolaze iz **Bootstrap JS-a** (modal, hamburger, accordion, carousel).  Fokus je na HTML strukturi i Bootstrap klasama.

---

## 👥 Podjela uloga i zadataka

| Uloga | Učenik | Branch(evi) | Zadatak |
|-------|--------|-------------|---------|
| **Lead Developer** | Helena Barać | `feature/hero-navigacija` + `feature/kontakt-footer` | Navbar, Hero, Modal, Kontakt forma, Footer, koordinacija |
| **UI & Content Dev** | Slavica Nikolina Stanić | `feature/programi` | Sekcija programa s 6 kartica + custom CSS za te sekcije |
| **Content Developer** | Andrea Ištuk | `feature/cjenik` + `feature/raspored-faq` | Pricing kartice, Tablica rasporeda, FAQ accordion |

> S 3 člana, konflikti u `index.html` su vjerojatniji jer svi diraju isti fajl.
> **Dogovorite redoslijed sekcija odmah na početku** i unesite ga na dno ovog README-a.

---

## 🚀 Git workflow

### Početak

```bash
# 1. Kloniraj
git clone https://github.com/bozoperic/ironzone-gym.git
cd ironzone-gym

# 2. Napravi branch
git checkout -b feature/tvoj-zadatak

# 3. Provjeri
git branch
```

### Rad i commitovi

```bash
# Commita što češće — svaka sekcija je jedan commit
git add .
git commit -m "Dodana pricing kartica za Standard plan"
git push -u origin feature/tvoj-zadatak
```

### OBAVEZNI sync — svakih 20-30 minuta

```bash
git checkout main
git pull
git checkout feature/tvoj-branch
git merge main
```

Ako nastane conflict:

```bash
# Vidi koji fajlovi imaju conflict
git status

# Otvori fajl u VSC — pojavljuju se markeri:
# <<<<<<< HEAD
# tvoja verzija
# =======
# verzija s maina
# >>>>>>> main

# Odlučite zajedno što zadržati, obrišite markere, zatim:
git add .
git commit -m "Riješen merge conflict u index.html"
git push
```

### Pull Request

1. GitHub → **Compare & pull request**
2. Reviewer: Lead Developer
3. Opis: što si implementirao
4. Čekaj review i approval

---

## ⚠️ Pravila rada

1. **Nikad direktno na main** — uvijek branch → PR → merge
2. **Dogovorite redoslijed sekcija** odmah — upišite ispod u tablicu
3. **Svaka sekcija u `index.html` ima komentar s imenom autora** — ne diraj tuđi dio
4. **Konflikte rješavate zajedno** — ne solo
5. **Min. 6 commitova po osobi** s opisnim porukama
6. **Bez JavaScripta** — sve interaktivnosti kroz Bootstrap klase i atribute

---

## 📁 Struktura projekta

```
ironzone-gym/
├── index.html        ← dijele svi, PAZITE NA KONFLIKTE
├── css/
│   └── style.css     ← svi mogu pisati u dogovorenim sekcijama
├── img/
└── README.md         ← POPUNITE ODMAH
```

---

## ✅ Zahtjevi — što mora biti implementirano

### Obavezno:
- [ ] Navbar (sticky, hamburger na mobitelu, gumb "Postani član")
- [ ] Hero sekcija (min-height 100vh, tamna pozadina)
- [ ] Modal za prijavu (otvara se s min. 2 mjesta — navbar gumb i hero gumb)
- [ ] 6 kartica programa u gridu (`col-md-4`)
- [ ] 3 pricing kartice (srednja vizualno istaknuta — `border`, `badge`, drugačija boja)
- [ ] Tablica rasporeda (Bootstrap `table`, `table-striped` ili `table-dark`)
- [ ] FAQ accordion (min. 5 pitanja, `data-bs-parent` za zatvaranje)
- [ ] Kontakt forma (min. 4 polja)
- [ ] Dismissible `alert` s promocijom na vrhu stranice
- [ ] Footer s logom, linkovima i copyright tekstom
- [ ] Custom CSS — promijenjena primarna boja i font
- [ ] Responzivno na 375px (testirano u DevToolsu)
- [ ] Min. 6 commitova po osobi s opisnim porukama
- [ ] Svi PR-ovi pregledani i mergani kroz Lead Deva

### Bonus (samo Bootstrap, bez JS):
- [ ] `badge` oznake na karticama programa (npr. "Popularno", "Novo", "Za početnike")
- [ ] `list-group` za prednosti u pricing karticama umjesto običnog teksta
- [ ] `card-header` s kategorijom na programskim karticama
- [ ] Sekcija s Bootstrap `progress` barovima (npr. "Intenzitet treninga")
- [ ] Testimoniali — kartice s citatima članova (`blockquote` unutar `card`)
- [ ] `nav-tabs` za prikaz rasporeda po danima

---

## 🗓️ Vremenski okvir

| Faza | Što | Rok |
|------|-----|-----|
| Setup | Clone, branch, dogovor o strukturi i bojama | Prvih 15 min |
| Razvoj | Svaki na svom branchu, sync svakih 20 min | Sat 1 + Sat 2 |
| Integracija | PR-ovi, review, merge | Zadnjih 30 min |
| Prezentacija | Demo pred razredom | Kraj |

---

## 🎨 Smjernice dizajna

- **Paleta:** crna + snažna akcent boja (crvena, narančasta ili neonska zelena)
- **Fontovi:** Oswald (naslovi, uppercase) + Open Sans (tijelo) — već učitani u CSS-u
- **Stil:** snažan, energičan, minimalistički
- **Zaobljenost:** 0 (oštri kutovi) — gym estetika
- **Slike:** `https://picsum.photos/seed/gym1/600/400` itd.

---

## 📌 Dogovor o redoslijedu sekcija — popunite odmah!

| Redoslijed | Sekcija | Radi |
|------------|---------|------|
| 1 | Alert (promo) | ANDREA IŠTUK |
| 2 | Navbar | Lead Dev |
| 3 | Hero + Modal | Lead Dev |
| 4 | Programi | SLAVICA NIKOLINA STANIĆ |
| 5 | Cjenik | SLAVICA NIKOLINA STANIĆ |
| 6 | Raspored | SLAVICA NIKOLINA STANIĆ |
| 7 | FAQ | ANDREA IŠTUK |
| 8 | Kontakt | Lead Dev |
| 9 | Footer | Lead Dev |

---

*Projekt se predaje kao GitHub repo link. README mora biti popunjen s imenima i redoslijedom sekcija.*
