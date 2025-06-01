
# 🌓 Proste wyłączenie oświetlenia po bezruchu (1–3 źródła, 1–2 czujniki)

Blueprint do Home Assistant, który automatycznie wyłącza jedno, dwa lub trzy światła po upływie określonego czasu bezruchu, wykrytego przez maksymalnie dwa czujniki ruchu.

## 🔧 Funkcje

- Obsługa **1–3 świateł** (`light`)
- Obsługa **1–2 czujników ruchu** (`binary_sensor`)
- Konfigurowalny **czas bezruchu (w minutach)**
- Wyłącza tylko te światła, które były włączone
- Loguje wyłączenia do **Logbooka**
- W pełni konfigurowalny przez UI Home Assistant

## 📥 Import do Home Assistant

Kliknij link poniżej lub skopiuj adres do formularza „Import blueprint”:

[📎 Importuj blueprint](https://my.home-assistant.io/redirect/blueprint_import/?url=https://raw.githubusercontent.com/sza86/BluePrints/main/szablon_wylaczenia_swiatla.yaml)

---

## ⚙️ Wejścia

| Nazwa                | Opis                                                   | Wymagane |
|---------------------|--------------------------------------------------------|----------|
| `motion_sensor_1`   | Główny czujnik ruchu                                    | ✅       |
| `motion_sensor_2`   | Drugi czujnik ruchu (opcjonalny)                        | ❌       |
| `light_target_1`    | Główne światło                                          | ✅       |
| `light_target_2`    | Dodatkowe światło #1 (opcjonalne)                       | ❌       |
| `light_target_3`    | Dodatkowe światło #2 (opcjonalne)                       | ❌       |
| `delay_time`        | Czas bezruchu w minutach (np. 1–60)                     | ✅       |

---

## 🧠 Zasada działania

1. Czujnik lub czujniki przestają wykrywać ruch.
2. Po zadanym czasie (np. 3 minuty) uruchamiane są warunki.
3. Jeśli nadal jest brak ruchu – każde włączone światło zostaje wyłączone.
4. Informacja o wyłączeniu trafia do `Logbook`.

---

## 📝 Autor

- 👤 Autor: [szpila86](https://github.com/sza86)
- 📄 Licencja: [MIT](LICENSE)

---

## 📂 Plik YAML

Blueprint znajduje się w pliku [`szablon_wylaczenia_swiatla.yaml`](./szablon_wylaczenia_swiatla.yaml)
