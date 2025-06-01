# 🌓 Szablon automatyzacji: Wyłączenie światła po braku ruchu lub czasie

Ten blueprint dla Home Assistant automatycznie **wyłącza jedno lub więcej świateł** po określonym czasie braku ruchu – lub po czasie, nawet jeśli czujników ruchu nie ma. Zapewnia **elastyczne sterowanie** światłem w pomieszczeniach z różną liczbą źródeł światła i czujników.

## ✅ Funkcje

- Obsługa do **3 źródeł światła**
- Obsługa **0–2 czujników ruchu**
- **Warunek włączenia światła** – światła nie wyłączają się, jeśli są już zgaszone
- **Opcjonalne powiadomienia** na jedno lub dwa urządzenia `notify.*`
- **Zabezpieczenia przed błędami**: brakujące czujniki nie powodują awarii

## ⚙️ Wymagane dane wejściowe

| Nazwa | Opis |
|------|------|
| `light_1` | Główne światło do wyłączenia |
| `delay_minutes` | Czas w minutach do wyłączenia światła |

## 🧩 Opcjonalne dane wejściowe

| Nazwa | Opis |
|------|------|
| `motion_sensor_1`, `motion_sensor_2` | Czujniki ruchu |
| `light_2`, `light_3` | Dodatkowe światła do wyłączenia |
| `send_notification` | Czy wysyłać powiadomienia |
| `notify_target`, `notify_target_2` | Nazwy usług `notify.*` |

## 🔍 Działanie

### Scenariusz 1: Pomieszczenie z 1 czujnikiem ruchu

- Światło wyłącza się po `X minutach`, jeśli czujnik nie wykrywał ruchu przez ten czas.

### Scenariusz 2: Pomieszczenie z 2 czujnikami

- Światło wyłącza się po `X minutach`, **jeśli oba czujniki były wyłączone przez ten czas**.

### Scenariusz 3: Brak czujników ruchu

- Światło wyłącza się **tylko na podstawie czasu** – niezależnie od obecności.

## 📦 Instalacja

1. Przejdź do `Automations & Scenes > Blueprints > Import Blueprint`
2. Wklej link do `blueprint.yaml` z tego repozytorium
3. Skonfiguruj instancję automatyzacji

## 📝 Przykładowe użycie

- Pokój z 1 czujnikiem: zgaś światło po 10 minutach bezruchu
- Korytarz z 2 czujnikami: wyłącz po 5 minutach, gdy żaden nie wykrywa ruchu
- WC bez czujnika: wyłącz po 8 minutach (np. po wejściu zapalono ręcznie)

---

## 👤 Autor

Blueprint opracowany przez **SZA**  
Dostosowany do platformy **Home Assistant**

---

**Licencja:** MIT
