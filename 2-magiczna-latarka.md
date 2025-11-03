---
title: Magiczna latarka
layout: default
nav_order: 2          # Kolejność lekcji w obrębie Modułu 1
description: Zadanie Praktyczne - Budujemy Wieżę Wyzwań!
---
# 🔦 Karta Zadania: Magiczna Latarka Rozświetlająca Mrok

## 🚀 Wprowadzenie
Witajcie w naszym mrocznym świecie! Wszędzie jest ciemno, a jedynym sposobem na przetrwanie jest stworzenie własnego źródła światła. W tym zadaniu przećwiczymy najważniejsze umiejętności z Fazy 1: tworzenie narzędzi typu **Tool** i prawidłowe zarządzanie hierarchią gry.

## ✅ Cel Zadania
Stworzenie w pełni funkcjonalnej Latarki, którą gracz automatycznie otrzyma na start, oraz wbudowanie w nią efektu świetlnego.

---

## ETAP 1: Przygotowanie Mrocznej Sceny (5 minut)

Musimy stworzyć noc, aby nasza latarka była potrzebna!

1.  **Lokalizacja Oświetlenia:** W panelu **Explorer** (Przeglądarka obiektów) znajdź obiekt **`Lighting`**.
2.  **Pora Dnia:** W panelu **Properties** (Właściwości) ustaw:
    * `TimeOfDay` (Pora Dnia) na wartość: **`0:00:00`** (środek nocy).
3.  **Światło Otoczenia:** Upewnij się, że kolory **`Ambient`** i **`OutdoorAmbient`** są ustawione na bardzo ciemne odcienie (bliskie czerni), aby usunąć wszelkie cienie i źródła światła z otoczenia.

## ETAP 2: Budowa Fizycznej Latarki (15 minut)

Teraz stworzymy uchwyt i wbudujemy w niego żarówkę.

1.  **Uchwyt (Handle):**
    * W zakładce **Home** (Główna) dodaj nową część: **Part**.
    * **NAZWA:** Zmień nazwę tej części w Explorerze na **`Handle`**.
    * **WŁAŚCIWOŚCI:** Zmień kolor na czarny lub szary.
    * **FIZYKA:** Właściwość **`Anchored`** (Zakotwiczenie) musi być **WYŁĄCZONA**.
2.  **Źródło Światła (PointLight):**
    * Kliknij prawym przyciskiem myszy na **`Handle`** w Explorerze.
    * Wybierz **Insert Object** (Wstaw Obiekt) -> **`PointLight`** (Światło Punktowe).
    * Wybierz teraz obiekt **`PointLight`** i w panelu Properties ustaw:
        * `Range` (Zasięg) na co najmniej **`20`** (duży zasięg).
        * `Color` na **żółty** lub **biały** (kolor światła).

## ETAP 3: Złożenie Narzędzia i StarterGear (10 minut)

Musimy przekształcić nasz fizyczny obiekt w narzędzie do noszenia.

1.  **Kontener Tool:**
    * W Explorerze znajdź obiekt **`StarterPlayer`**.
    * Kliknij prawym przyciskiem myszy na **`StarterPlayer`** i wstaw obiekt **`Tool`** (Narzędzie).
    * Zmień nazwę nowego obiektu na **`MojaLatarka`**.
2.  **Prawidłowa Hierarchia:**
    * Przeciągnij część **`Handle`** (wraz z wbudowanym `PointLight`) i upuść ją **do wewnątrz** obiektu **`MojaLatarka`**.

    * *Sprawdzenie Hierarchii:* Upewnij się, że Twój układ wygląda tak: `MojaLatarka (Tool) > Handle (Part) > PointLight`.

3.  **Umieszczenie w Plecaku:**
    * Przeciągnij cały obiekt **`MojaLatarka`** i umieść go w folderze **`StarterPlayer > StarterGear`**. (Jeśli folder `StarterGear` jest niewidoczny, musisz go najpierw wstawić ręcznie: Prawym przyciskiem myszy na `StarterPlayer` -> Insert Object -> `StarterGear`).

## ETAP 4: Testowanie i Weryfikacja (5 minut)

1.  **Uruchom Grę:** Kliknij przycisk **Play** (Graj).
2.  **Weryfikacja Narzędzia:** Czy w prawym dolnym rogu ekranu pojawiła się ikona latarki?
3.  **Weryfikacja Światła:** Użyj latarki (kliknij na jej ikonę lub wciśnij **klawisz 1**).
    * Czy trzymasz ją w ręku?
    * Czy światło rozświetla ciemną mapę?

---

### Wyzwanie Dodatkowe (Dla Szybkich Uczniów)

Zmień właściwości latarki, aby stworzyć **upiorne światło** idealne na Halloween!

1.  Zmień kolor obiektu **`PointLight`** na **ciemny fiolet** lub **jaskrawozielony**.
2.  Właściwość **`Brightness`** (Jasność) ustaw na **3** lub **4**, aby nadać upiorny blask.