# Date Invite 💌

Interaktywna, jednostronicowa strona-zaproszenie na randkę / spotkanie. Zamiast suchego „kiedy masz czas?” — animowane intro, zabawny przycisk „Nie”, wybor aktywności z koszykiem i „paragon” podsumowujący plan.

> **Status zrzutów:** Placeholdery poniżej — dodaj obrazy według [instrukcji w `docs/media/SCREENSHOTS.md`](docs/media/SCREENSHOTS.md).

---

## Zrzuty ekranu

### Intro (animacja Lottie)

| Desktop | Mobile |
|---------|--------|
| ![Intro — desktop](docs/media/screenshots/01-intro-desktop.png) | ![Intro — mobile](docs/media/screenshots/02-intro-mobile.png) |

Pełnoekranowa animacja `hand.json`: kliknij / dotknij przycisk → animacja kliku → wejście na stronę. Na desktopie palec reaguje na ruch myszy (hover).

### Główny flow

![Pytanie Tak/Nie](docs/media/screenshots/03-ask-desktop.png)

![Uciekający przycisk „Nie”](docs/media/screenshots/04-no-button-desktop.png)

![Wybór aktywności i koszyk](docs/media/screenshots/05-activities-desktop.png)

![Modal specjalnego życzenia](docs/media/screenshots/06-wish-modal-desktop.png)

![Wybór dnia i godziny](docs/media/screenshots/07-pick-desktop.png)

### Podziękowanie

| Desktop | Mobile |
|---------|--------|
| ![Paragon — desktop](docs/media/screenshots/08-thanks-desktop.png) | ![Paragon — mobile](docs/media/screenshots/09-thanks-mobile.png) |

---

## Co robi ta strona?

1. **Intro** — animacja Lottie na pełny ekran; użytkownik musi kliknąć, żeby wejść dalej.
2. **Pytanie** — „Kiedy kolejne spotkanie?” z przyciskami Tak / Nie (przycisk „Nie” ucieka i pojawiają się emoji).
3. **Aktywności** — wielokrotny wybor kafelków (spacer, jedzonko, piknik, planszówki, zoo, sport, ogród japoński) + opcjonalne **specjalne życzenie**.
4. **Koszyk** — licznik wybranych pozycji; emoji „wlatuje” do koszyka w rogu.
5. **Termin** — customowe dropdowny: dzień (od dziś do końca miesiąca) i godzina (10:00–22:00).
6. **Potwierdzenie** — paragon z podsumowaniem + opcjonalna wysyłka na Formspree + deszcz konfetti 🎉

Bez backendu — działa jako statyczna strona (GitHub Pages, Netlify, dowolny hosting plików).

---

## Design

UI w palecie **„party keyboard”** (pastelowy błękit, lawenda, krem, fiolet, akcenty konfetti). Fonty: Cormorant Garamond + Caveat (Google Fonts).

Opcjonalny zrzut palety: ![Paleta UI](docs/media/screenshots/11-palette.png)

---

## Uruchomienie lokalnie

```bash
cd date-invite
python3 -m http.server 8000
```

Otwórz [http://localhost:8000](http://localhost:8000).  
**Nie otwieraj `index.html` przez `file://`** — animacja Lottie i `hand.json` wymagają serwera.

---

## Konfiguracja

W `index.html` na początku skryptu:

```javascript
const FORMSPREE_ENDPOINT = "";  // URL formularza Formspree
const TWOJE_IMIE = "Wiktor";    // Twoje imię w powiadomieniu mailowym
```

Aktywności edytujesz w tablicy `ACTIVITIES` w tym samym pliku.

---

## Struktura projektu

```
date-invite/
├── index.html          # Cała aplikacja (HTML + CSS + JS)
├── hand.json           # Animacja Lottie (intro)
├── wroclaw.jpg         # Asset (opcjonalny / legacy)
├── README.md
└── docs/
    └── media/
        ├── SCREENSHOTS.md    # Instrukcja: co i gdzie zeskreenować
        └── screenshots/      # Tu wrzucasz PNG/JPG do README
```

---

## Technologie

- Czysty HTML / CSS / JavaScript (bez frameworka)
- [lottie-player](https://github.com/LottieFiles/lottie-player) (CDN) — intro
- [Formspree](https://formspree.io/) — opcjonalne powiadomienie e-mail
- Responsywny layout (mobile-first, `dvh`, safe area)

---

## Licencja

Projekt osobisty — użyj i zmieniaj według uznania. Animacja `hand.json` — sprawdź prawa użytkowania, jeśli pochodzi z zewnętrznego źródła.
