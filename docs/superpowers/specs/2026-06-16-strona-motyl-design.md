# Nowa strona — Arek „Motyl" Dembiński (instruktor strzelectwa bojowego)

Data: 2026-06-16

## Cel
Odświeżyć wizualnie istniejącą stronę (wygląd z 2018, dominujące żółto-złote tła)
zachowując całą obecną treść. Nowy klimat: mroczny / taktyczny, pasujący do profesji —
były operator Jednostki Specjalnej GROM, instruktor strzelectwa bojowego.

## Decyzje (zatwierdzone)
- **Technologia:** statyczny HTML/CSS/JS, bez build-stepu, działa z `file://` i z dowolnego serwera.
- **Struktura:** wielostronicowa (jak obecnie).
- **Styl:** mroczny / taktyczny.
- **Zdjęcia:** wykadrowane ze screenów/PDF (źródła: `old_web/*.pdf`).
- **Akcent kolorystyczny:** stonowany bursztyn/złoto (nawiązanie do logo, „medalowy" wydźwięk).
- **Kontakt:** przycisk mailto + komplet danych + social. Bez backendu/formularza (do dodania później).
- **Telefon:** placeholder — numer do podmiany przez właściciela.

## Architektura plików
```
site/
  index.html          # Strona główna
  oferta.html         # Oferta + cenniki
  o-mnie.html         # Bio
  aktualnosci.html    # Aktualności
  kontakt.html        # Kontakt
  css/styles.css
  js/main.js          # menu mobilne, reveal-on-scroll, rok w stopce
  img/                # wykadrowane zdjęcia + logo
```
Wspólny nagłówek i stopka powielone w HTML na każdej stronie (zero zależności runtime,
brak problemów z `fetch`/CORS przy `file://`).

## Treść (przeniesiona 1:1)

### Strona główna (index.html)
- Hero: „Arek „Motyl" Dembiński" / „instruktor strzelectwa bojowego" + CTA.
- Intro: „Arkadiusz „MOTYL" Dembiński — były żołnierz Jednostki Specjalnej GROM, weteran misji
  w Afganistanie i Iraku. Posiadam wieloletnie doświadczenie oraz umiejętności w zakresie
  przygotowania ludzi i zespołów do działań w warunkach bojowych, kryzysowych i zagrażających
  życiu. Prowadzę usługi doradcze i szkoleniowe dla osób prywatnych, firm, służb mundurowych
  oraz instytucji rządowych."
- OFERTA — 3 kafle:
  1. Szkolenia zamknięte — dla instytucji rządowych i służb mundurowych
  2. Szkolenia otwarte — dla firm i osób prywatnych
  3. Usługi doradcze — w zakresie bezpieczeństwa
- AKTUALNOŚCI — 3 wpisy:
  1. „Szkolenie strzeleckie — karabin." — Zapraszam wszystkich w każdy poniedziałek godz. 21.00
     na trening strzelecki — karabin…
  2. „Misja Weteran — historia Motyla" — Historia Arka „Motyla" Dembińskiego…
  3. „Fight and Shooting" — Ruszamy z treningami Fight and Shooting. Treningi będą odbywały się
     cyklicznie raz w miesiącu…
- PARTNERZY: International Association of Krav Maga Warriors; Fundacja Sprzymierzeni z GROM.

### Oferta (oferta.html)
Wstęp: „Prowadzę szkolenia dla firm i osób prywatnych (szkolenia otwarte — w których może
uczestniczyć każdy) w zakresie:" — strzelanie (pistolet/karabin), szkolenia strzeleckie dla
kobiet, szkolenie medyczne, szkolenie wysokościowe, samoobrona (Krav Maga), Fight and Shooting.

Cenniki:
- **Szkolenia strzeleckie — pistolet:** POZIOM I — 1000 zł/os (2 dni, grupa 4–12), POZIOM II —
  1300 zł/os (2 dni, grupa 6–8), POZIOM III — 1800 zł/os (3 dni, grupa 6–8).
- **Szkolenia strzeleckie — karabin:** POZIOM I — 1000 zł/os (2 dni, grupa 6–12), POZIOM II —
  1300 zł/os (2 dni, grupa 6–8), POZIOM III — 1800 zł/os (3 dni, grupa 6–8).

### O mnie (o-mnie.html)
Pełne bio: „Nazywam się Arkadiusz Dembiński, zwany i znany również jako „Motyl". Byłem operatorem
Oddziału Bojowego Jednostki Specjalnej GROM. Przez ponad 17 lat zdobywałem wiedzę i doświadczenie
w zakresie procedur i taktyki działań specjalnych. Wielokrotnie brałem udział w misjach
zagranicznych, walczyłem w Afganistanie i Iraku. Uczestniczyłem między innymi w akcjach uwalniania
zakładników. Podczas jednej z akcji, w trakcie wykonywania zadania bojowego zostałem poważnie
ranny. Za zasługi, wzorową służbę i poświęcenie w czasie walki zostałem odznaczony przez Prezydenta
Rzeczpospolitej Polskiej Krzyżem Kawalerskim Orderu Krzyża Wojskowego. Posiadam tytuł Eksperta Krav
Maga uzyskany w Izraelu. Jestem zdobywcą Pucharu Świata w kick boxingu, wielokrotnym medalistą
Mistrzostw Europy i Polski. W Oddziale Bojowym GROM odpowiadałem za wyszkolenie w zakresie walki
wręcz. Obecnie prowadzę własną firmę szkoleniową."

### Kontakt (kontakt.html)
Nagłówek: „Masz pytania, chcesz skorzystać z moich usług lub poznać warunki współpracy? Zapraszam
do kontaktu:". Dane: Arek Motyl Dembiński · NIP: 8771314077 · REGON: 365541693 ·
e-mail: arek@arekmotyldembinski.pl · telefon: [placeholder] · social: Facebook, Instagram, YouTube.

### Stopka (wszystkie strony)
Logo + „© 2026 Arek „Motyl" Dembiński. Wszelkie prawa zastrzeżone." (rok generowany w JS).

## Język wizualny
- **Paleta:** baza grafit/czerń (`#0d0f10`, `#15181a`), warstwy oliwka/khaki (`#3b4032`,
  `#5c6450`), tekst jasny (`#e7e5df`), akcent bursztyn/złoto (`#c8962f` / `#e0a83d`).
- **Typografia:** nagłówki — Oswald / Saira Condensed (kondensowany, mocny); treść — Inter/Barlow.
  Pełna obsługa polskich znaków (Latin Extended). Fonty z Google Fonts.
- **Detale:** subtelny grain/noise, monospace etykiety sekcji (`01 / OFERTA`), cienkie linie-
  celowniki, ostre rogi (bez zaokrągleń), zdjęcia z ciemnym gradientem/duotone dla spójności.
- **Ruch:** reveal-on-scroll (fade/slide), lekki ken-burns/parallax na hero. Lekko, wydajnie,
  z poszanowaniem `prefers-reduced-motion`.

## Zdjęcia — źródła i kadry
Ekstrakcja `pdfimages -j` z `old_web/*.pdf` (kafle stron @2880px), następnie kadrowanie (sips/magick):
- **Logo** (koło, AREK DEMBIŃSKI MOTYL) — z PDF kontakt (czyste na białym tle).
- **Portret pustynny** (Motyl z karabinem) — hero + sekcja „O mnie".
- **Zdjęcie zespołu** (nocne, GROM) — sekcja „O mnie".
- **Ujęcie w polu z karabinem** — pas teksturowy/parallax (kadr bez wtopionego tekstu).
- **Siatka 8 zdjęć treningowych** — kafle oferty + galeria.
Zdjęcia z bakowanymi nakładkami starej strony pomijane na rzecz czystych źródeł.

## Responsywność i dostępność
- Mobile-first; menu hamburger < 900px; nawigacja „Oferta" jako dropdown na desktopie.
- Kontrast tekstu zgodny z WCAG AA; alt-teksty; focus states; `prefers-reduced-motion`.

## Poza zakresem (YAGNI)
- Backend/CMS, formularz wysyłający e-mail po stronie serwera, panel admina.
- Dynamiczne aktualności (na razie statyczne wpisy w HTML).
- Wielojęzyczność (tylko polski).
```
