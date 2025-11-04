---
title: Opanowanie Diagnostyki NOx
description: Wykorzystanie Danych Z Czujników Wlotowych i Wylotowych dla Oceny Wydajności SCR
breadcrumbs: true
date: "2023-12-10T00:35:28+08:00"
draft: false
---

### **Opanowanie Diagnostyki NOx: Wykorzystanie Danych Z Czujników Wlotowych i Wylotowych dla Oceny Wydajności SCR**

Podstawową funkcją dwóch czujników NOx w układzie wydechowym pojazdu jest umożliwienie Jednostce Sterującej Silnika (ECU) obliczenia w czasie rzeczywistym **wydajności konwersji** Selektywnej Redukcji Katalitycznej (SCR). Ten obliczony wskaźnik wydajności jest kluczową metryką zarówno dla kontroli emisji, jak i diagnostyki pokładowej (OBD).

### **Główne Obliczenie: Wydajność Konwersji SCR**

Wydajność systemu SCR jest określana przez to, ile NOx jest przekształcane w nieszkodliwy N2 (Azot) i H2O (Woda). ECU używa prostego stosunku odczytów z dwóch czujników do monitorowania tego procesu:

> **Wydajność Konwersji SCR (%) = ((NOx Wlotowe - NOx Wylotowe) / NOx Wlotowe) x 100**

### **Interpretacja Scenariuszy Danych na Żywo**

Analiza zależności między odczytami NOx **Przedniego (Wlotowego)** a **Tylnego (Wylotowego)** pomaga ustalić pierwotną przyczynę usterki związanej z emisją:

| Odczyt NOx Wlotowego | Odczyt NOx Wylotowego | Wydajność SCR | Diagnoza |
| :--- | :--- | :--- | :--- |
| **Wysoki (~800 ppm)** | **Niski (~100 ppm)** | **Wysoka (~87% - 90%)** | **System Sprawny:** Prawidłowe dozowanie DEF, a katalizator SCR jest aktywny. |
| **Wysoki** | **Wysoki (≈ Wlotowy)** | **Niska (~0% - 30%)** | **Awaria Katalizatora lub Dozowania:** SCR nie redukuje NOx. Sprawdzić najpierw system DEF, następnie podejrzewać degradację katalizatora. |
| **Nieprawdopodobny/Zablokowany** | **Normalny** | **Nieprawidłowa** | **Awaria Czujnika Wlotowego:** ECU nie może ufać odczytowi Wlotowemu, co prowadzi do nieprawidłowego dozowania (często opartego na modelu zapasowym). **Wymienić Czujnik Wlotowy.** |
| **Normalny** | **Nieprawdopodobny/Zablokowany** | **Nieprawidłowa** | **Awaria Czujnika Wylotowego:** ECU nie może zweryfikować zgodności. **Wymienić Czujnik Wylotowy.** |

### **Monitor OBD i Progi Awaryjne**

ECU stale monitoruje ten stosunek wydajności. Jeśli obliczona wydajność SCR spadnie poniżej prawnie wymaganego progu OBD (np. 80%) przez określony okres jazdy, ECU rejestruje kod usterki wydajności (odpowiednik P420 lub P20EE).

Co kluczowe, nieprawidłowy odczyt z **któregokolwiek** czujnika NOx (Wlotowego lub Wylotowego) zakłóci to obliczenie, prowadząc ECU do błędnego zgłoszenia awarii katalizatora lub dozowania, co skutkuje niepotrzebnymi kosztami napraw.

Nasze czujniki zapewniają zweryfikowane, stabilne i synchroniczne odczyty, zapewniając, że obliczenia wydajności ECU są zawsze oparte na wiarygodnych danych, co pozwala technikom ufać wnioskom diagnostycznym systemu.
