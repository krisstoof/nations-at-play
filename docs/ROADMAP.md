# Roadmap — Nations at Play

## Założenia
Celem jest geopolityczna strategia na **prawdziwej Ziemi w administracyjnym widoku 2D**. Mieszkańcy i siły zbrojne reprezentowani są liczbami, a rozkazy wykonują systemy symulacji i autonomiczne instytucje / dowódcy.

### Reguły produktu
- Gracz podejmuje decyzje na poziomie regionów, a nie pojedynczych osób.
- Wysoka czytelność mapy, szybkie przesuwanie i płynne przełączanie poziomów szczegółowości.
- Faktyczna geografia oraz podział administracyjny jako **stan początkowy**; data odniesienia danych musi być jawna.
- Własność, kontrola i granice polityczne mogą ulegać zmianie w trakcie symulacji.
- Bez kopiowania map Google i bez obciążania publicznych serwerów kafelków w grze.

## M0 — Fundament (pierwsze kroki)
- [ ] Sprecyzować MVP i dokument modelu regionu, czasu, populacji i decyzji.
- [ ] Wybrać granice administracyjne Polski (województwa), rok i licencję.
- [ ] Przygotować pipeline GeoJSON → dane gry.
- [ ] Skonfigurować prosty test uruchomienia projektu.

**Gotowe, gdy:** dane wejściowe i format mapy są powtarzalne, a projekt otwiera się w Godot 4.

## M1 — Mapa Polski (pierwszy demonstrator)
- [ ] Renderować 16 województw, rzeczywiste linie graniczne.
- [ ] Kamera: zoom, przesuwanie, ograniczenia.
- [ ] Hit testing i zaznaczenie województwa.
- [ ] Nazwy / etykiety zależne od zoomu.
- [ ] Panel regionu: nazwa, populacja, liczba mieszkańców.
- [ ] Tryby widoku: administracyjny i ludność.
- [ ] Umożliwić dodanie powiatów bez przebudowy rendererów.

**Gotowe, gdy:** można płynnie obejrzeć Polskę, kliknąć dowolne województwo i odczytać zagregowaną liczbę mieszkańców z jawnie opisanej wersji danych.

## M2 — Pierwsza grywalna pętla
- [ ] Model symulacji oddzielony od GUI.
- [ ] Pauza, prędkości i dzienny/miesięczny krok symulacji.
- [ ] Zlecenie inwestycji w regionie z kosztem, czasem wykonania i efektem.
- [ ] Zmiany populacji / migracje w prostym modelu.
- [ ] Podstawowe zależności gospodarcze.
- [ ] Zapis i wczytanie stanu gry.

**Gotowe, gdy:** gracz może wydać decyzję w wybranym województwie, uruchomić czas, zaobserwować skutek i zapisać rozgrywkę.

## M3 — Skalowanie na prawdziwy świat
- [ ] Państwa świata, podziały ADM1, opcjonalnie ADM2.
- [ ] Wielopoziomowy renderer (LOD, pamięć, wydajność).
- [ ] Model własności / kontroli terenu niezależny od pierwotnych granic.
- [ ] System polityczny i dyplomacja.
- [ ] AI państw, delegowanie zadań i reagowanie na świat.
- [ ] Wojna operacyjna bez mikrozarządzania jednostkami.

**Gotowe, gdy:** system działa na większej skali niż Polska bez fundamentalnego przeprojektowania modelu.

## Zasoby / ryzyka
- Nierówna jakość i szczegółowość granic między państwami, różne daty danych.
- Populacja wg granic administracyjnych ≠ populacja w siatce (odmienne lata i niepewność).
- Duże zbiory wymagają preprocessing, uproszczeń geometrii i streamingu.
- Licencje / atrybucje źródeł (szczególnie OSM ODbL, WorldPop i inne warunki specyficzne dla zbioru).
- Nie zakładać dostępności ani automatycznej redystrybucji zewnętrznych danych w repo.

Szczegóły i kryteria akceptacji: [GitHub Issues](../issues).
