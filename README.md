# 🤖 AI Email Signature Generator (Make.com + OpenAI)

[![Automatyzacja: Make.com](https://img.shields.io/badge/Automatyzacja-Make.com-purple.svg)](#)
[![AI: OpenAI](https://img.shields.io/badge/AI-OpenAI-green.svg)](#)

W pełni zautomatyzowany system do generowania profesjonalnych stopek e-mail w formacie HTML przy użyciu sztucznej inteligencji. Zamiast ręcznie kodować stopki dla każdego pracownika, wystarczy wpisać jego dane do arkusza kalkulacyjnego, a system sam wygeneruje unikalny kod HTML i wyśle gotową stopkę na wskazany adres e-mail.

## ⚙️ Architektura i Workflow (Jak to działa?)

Proces jest całkowicie bezobsługowy i składa się z 4 kroków:
1. Dodanie nowego wiersza z danymi pracownika (Imię, Stanowisko, Uczelnia/Firma, Zdjęcie, Dane kontaktowe) w **Google Sheets**.
2. **Automatyzacja:** Platforma **Make.com**  pobiera dane.
3. **Generowanie AI:** Dane trafiają do **OpenAI API** (Prompt inżynieryjny wymusza wygenerowanie czystego kodu HTML ze stylami inline CSS).
4. **Dostarczenie:** Moduł e-mail w Make.com wysyła wygenerowaną stopkę prosto na skrzynkę pracownika do wklejenia (np. w Gmail lub Outlook).

## 📸 Zrzuty ekranu i Przykłady (Screenshots & Examples)

### 1. Przykładowe stopki wygenerowane przez AI
*Poniżej znajdują się przykłady 3 stopek, które system wygenerował na podstawie danych z arkusza:*

<details>
  <summary><strong>▶️ Zobacz Przykład 1 (Kliknij, aby rozwinąć)</strong></summary>
  <br>
  <img width="411" height="211" alt="Przykładowa stopka 1" src="https://github.com/user-attachments/assets/d6d11759-ea1f-4df0-8042-06503225e810" />
</details>

<br>

<details>
  <summary><strong>▶️ Zobacz Przykład 2 (Kliknij, aby rozwinąć)</strong></summary>
  <br>
  <img width="603" height="220" alt="Przykładowa stopka 2" src="https://github.com/user-attachments/assets/1f9b9aac-c32b-4369-8898-34abbc39fd65" />
</details>

<br>

<details>
  <summary><strong>▶️ Zobacz Przykład 3 (Kliknij, aby rozwinąć)</strong></summary>
  <br>
  <img width="406" height="213" alt="Przykładowa stopka 3" src="https://github.com/user-attachments/assets/3416abf7-7547-4af7-91bc-a61c0af1a737" />
</details>

### 2. Widok automatyzacji w Make.com
*Tak wygląda logika scenariusza, którą zaprojektowałem:*

[Scenariusz Make]
<details>
  <summary><strong>▶️ Zobacz Scenariusz (Kliknij, aby rozwinąć)</strong></summary>
  <br>
  <img width="1483" height="423" alt="Zrzut ekranu 2026-02-25 o 15 45 14" src="https://github.com/user-attachments/assets/5e59c9a5-6710-4b88-a470-31086fa5129a" />
</details>


## 🛠️ Technologie (Tech Stack)
* **Make.com** (Integracja i logika przepływu danych)
* **OpenAI API** (Generowanie kodu HTML/CSS na podstawie naturalnego języka)
* **Google Sheets** (Baza danych / Interfejs wprowadzania danych)
* **Email / SMTP** (Dostarczanie wyników)

## 🚀 Jak wdrożyć to u siebie? (Instrukcja)

Jeśli chcesz uruchomić ten system na swoim koncie Make.com:
1. Pobierz plik `blueprint.json` z tego repozytorium.
2. Zaloguj się do [Make.com](https://www.make.com/) i utwórz nowy scenariusz.
3. Kliknij `...` (More) na dole ekranu i wybierz **Import Blueprint**. Wgraj pobrany plik.
4. Podepnij własne połączenia (Connections):
   * Zaloguj się do swojego konta Google (dla Arkuszy).
   * Podaj swój klucz API z OpenAI.
   * Skonfiguruj moduł wysyłający e-maile (np. Gmail).
5. Uruchom scenariusz i dodaj nowy wiersz w swoim arkuszu!

## 📄 Prompt systemowy (Prompt Engineering)
Wewnątrz modułu OpenAI użyłem specjalnie skonstruowanego promptu, aby wymusić responsywny HTML.

---
**Autor:**
Paweł Zajczyk
📧 pawelzajczyk8@gmail.com
