# Nations at Play

Gra strategiczna (grand strategy / symulator geopolityczny) rozgrywająca się na **rzeczywistej mapie świata w widoku administracyjnym**.

Gracz zarządza terytoriami, ludnością i instytucjami poprzez decyzje strategiczne. Nie kontroluje pojedynczych postaci ani żołnierzy: ludność jest reprezentowana jako **zagregowane dane liczbowe**, a administracja i dowódcy realizują zlecone cele w granicach swoich możliwości.

> **Status:** koncepcja i wczesny prototyp. Prezentowane wartości i zasady są robocze.

## Wizja
- Mapa 2D rzeczywistej Ziemi: państwa → regiony pierwszego poziomu → powiaty / jednostki lokalne (tam, gdzie dane są dostępne).
- Płynny zoom i przesuwanie mapy; wybór obszaru i podgląd liczby mieszkańców oraz statystyk.
- Warstwy tematyczne: administracyjna, ludność, gospodarka, infrastruktura, polityka, dyplomacja, wojna.
- Polecenia dla regionów: rozwój infrastruktury, inwestycje, usługi publiczne, mobilizacja i inne.
- Symulacja świata: migracje, gospodarka, polityka, konflikty i reakcje społeczne.
- Walka na poziomie operacyjnym/strategicznym: wydawanie celów dowódcom, bez mikrozarządzania oddziałami.

## Zakres pierwszego prototypu (MVP)
1. Uruchamialny projekt **Godot 4**.
2. Mapa Polski z prawdziwymi granicami województw (w kolejnym kroku powiaty).
3. Przesuwanie mapy, zoom, wybór jednostki administracyjnej.
4. Panel wybranego obszaru z ludnością; podstawowa warstwa tematyczna.
5. Prosty kalendarz symulacji i jedna decyzja z widocznym efektem (np. inwestycja infrastrukturalna).
6. Zapis i odczyt stanu rozgrywki.

**Poza MVP:** cały świat w wysokiej szczegółowości, zaawansowana wojna, wybory, rozbudowana AI państw, symulacja jednostkowych ludzi.

## Technologia (propozycja)
- Godot 4; początkowo GDScript dla interfejsu i prototypu, możliwość wydzielenia intensywnych obliczeń do C# lub GDExtension później.
- Dane geograficzne wstępnie z Natural Earth / geoBoundaries oraz, opcjonalnie, OpenStreetMap.
- Dane populacji: oficjalne statystyki lub źródła siatkowe (np. WorldPop), z datą i informacją o metodzie agregacji.
- Granice wejściowe: GeoJSON; w grze format zoptymalizowany do renderowania, selekcji i poziomów szczegółowości.

## Zasady architektury
- **Geografia ≠ administracja ≠ stan gry.** Historyczne/aktualne granice administracyjne są danymi początkowymi; w grze własność i kontrola terytorium mogą się zmieniać.
- Symulacja oddzielona od prezentacji; nie tworzymy obiektu dla każdego mieszkańca.
- Działania gracza odbywają się na poziomie regionu / grupy, a nie jednostek fizycznych.
- Traktujemy dane geograficzne i demograficzne jako **przybliżenia z konkretnego roku**, nie jako aktualną „prawdę na żywo”.
- Nie wykorzystujemy bez zezwolenia kafelków, oznaczeń ani interfejsu Google Maps. Respektujemy licencje danych oraz zasady atrybucji.
- Dane mapowe i kod rozdzielone: repozytorium nie musi zawierać dużych plików źródłowych.

## Plan
Zobacz [docs/ROADMAP.md](docs/ROADMAP.md) oraz [GitHub Issues](../../issues) — zadania zawierają kryteria akceptacji.

## Uruchamianie
Otwórz katalog repozytorium jako projekt w edytorze Godot 4 i uruchom scenę główną. Prototyp nie zawiera jeszcze prawdziwych danych mapowych.

## Nazwa
„Nations at Play” jest roboczą nazwą projektu.
