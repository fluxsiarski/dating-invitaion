# Instrukcja zrzutów ekranu

Umieść gotowe pliki w folderze `docs/media/screenshots/`. Nazwy plików muszą być **dokładnie** takie jak poniżej — README na GitHubie podlinkuje je automatycznie.

**Jak robić screeny**
- Otwórz stronę przez lokalny serwer: `python3 -m http.server 8000` → `http://localhost:8000`
- Desktop: pełna szerokość przeglądarki (~1200–1440 px) lub wbudowane narzędzia dev (responsive)
- Mobile: tryb urządzenia w Chrome/Edge (np. iPhone 14) albo prawdziwy telefon
- Format: **PNG** lub **JPG**, proporcje naturalne (bez przycinania UI)

---

## Lista zrzutów (kolejność w README)

| Plik | Co pokazać | Jak dojść do tego ekranu | Wskazówki |
|------|------------|--------------------------|-----------|
| `01-intro-desktop.png` | Pełnoekranowe intro z animacją Lottie (palec + przycisk) | Odśwież stronę — intro jest na starcie | Desktop, szeroki ekran. Widoczna podpowiedź „kliknij, aby wejść” (na dole). Opcjonalnie najedź myszką bliżej przycisku, żeby palec był w połowie drogi. |
| `02-intro-mobile.png` | To samo intro na telefonie | Jak wyżej, widok mobile | Podpowiedź „dotknij ekranu 👆”. Pionowy screenshot. |
| `03-ask-desktop.png` | Pierwszy krok: „Kiedy kolejne spotkanie?” z Tak / Nie | Kliknij intro (lub „pomiń intro”) | Widoczne oba przyciski i serce na karcie. Hint „PS: Spróbuj kliknąć Nie” w lewym dolnym rogu — warto złapać. |
| `04-no-button-desktop.png` | Uciekający przycisk „Nie” + emoji | Na kroku „Tak/Nie” kliknij kilka razy **Nie** | Zrób screen w momencie, gdy „Nie” jest w innym miejscu i widać lecące emoji (😂🤣). |
| `05-activities-desktop.png` | Wybór aktywności + koszyk | Kliknij **Tak!** | Zaznacz 2–3 kafelki (fioletowe) + koszyk z liczbą w prawym górnym rogu. Animacja lotu emoji do koszyka — opcjonalny krótki GIF zamiast PNG. |
| `06-wish-modal-desktop.png` | Modal „Twoje specjalne życzenie” | Na kroku aktywności kliknij kafelek **✨ Twoje specjalne życzenie** | Modal na środku, lekko wpisz przykładowy tekst w pole. |
| `07-pick-desktop.png` | Wybór dnia i godziny | Wybierz aktywności → **Dalej 🌸** | Otwarty dropdown (dzień lub godzina) wygląda najlepiej na screenie. |
| `08-thanks-desktop.png` | Ekran podziękowania + paragon | Uzupełnij formularz → **Potwierdzam 🌸** | Paragon z dniem, godziną i listą aktywności. Konfetti na screenie — złap moment zaraz po potwierdzeniu. |
| `09-thanks-mobile.png` | Paragon na mobile | Jak wyżej, widok telefonu | Cały paragon czytelny w pionie. |

---

## Opcjonalne (dla README „Features”)

| Plik | Co pokazać |
|------|------------|
| `10-hover-intro-desktop.png` | Intro z palecem blisko przycisku (efekt hover myszką) |
| `11-palette.png` | Zrzut fragmentu UI z wyraźnymi kolorami (karta + przyciski) — do sekcji designu |

---

## Po dodaniu plików

1. Sprawdź, że nazwy plików są identyczne jak w tabeli.
2. Commit: `git add docs/media/screenshots/ && git commit -m "Dodaj zrzuty ekranu do README"`
3. Push na GitHub — obrazy pojawią się w README automatycznie.
