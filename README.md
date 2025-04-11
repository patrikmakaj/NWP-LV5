# Laravel LV5 – Upravljanje završnim i diplomskim radovima

Ovaj projekt je implementacija zadatka LV5 u okviru kolegija **Napredno web programiranje**. Aplikacija je izrađena u Laravelu i omogućuje upravljanje korisnicima, njihovim ulogama, unos i prijavu na završne i diplomske radove.

---

## 🎯 Ključne funkcionalnosti

- 🔐 **Autentikacija** (Laravel Breeze)
- 👤 **Tri uloge korisnika**: admin, nastavnik, student
- 🛠️ **Admin panel**: upravljanje korisnicima i njihovim ulogama
- 📄 **Dodavanje radova** od strane nastavnika (na HR i EN jeziku)
- 🧑‍🎓 **Student** može pregledati radove i prijaviti se na 5 radova (s prioritetima)
- ✅ **Nastavnik** može prihvatiti jednog studenta po radu
- 🌐 **Višejezičnost** (priprema za Laravel Localization)
- ✨ Jednostavno sučelje s podrškom za tamni/svijetli prikaz (po izboru)

---

## ⚙️ Tehnologije

- [Laravel](https://laravel.com/) 10.x
- [Laravel Breeze](https://laravel.com/docs/starter-kits#laravel-breeze)
- [Tailwind CSS](https://tailwindcss.com/)
- PHP 8.x
- MySQL 8.x
- Vite, Alpine.js

---

## 🚀 Instalacija

```bash
git clone https://github.com/patrikmakaj/NWP-LV5.git
cd NWP-LV5

composer install
cp .env.example .env
php artisan key:generate

npm install && npm run dev

# Pokreni MySQL ako treba
php artisan migrate
php artisan serve
```

---

## 🧪 Testni korisnici (ako ih dodaš)

| Uloga     | Email              | Lozinka |
|-----------|--------------------|---------|
| Admin     | admin@mail.hr      | lozinka |
| Nastavnik | nastavnik@mail.hr  | lozinka |
| Student   | student@mail.hr    | lozinka |

> Uloge se ručno postavljaju u bazi preko `role` kolone (`admin`, `nastavnik`, `student`)

---

## 📁 Struktura direktorija

```
routes/web.php                 → Web rute (autentikacija, prijave, admin)
app/Models/                   → User, Task, Application
app/Http/Controllers/         → Auth, AdminController, TaskController, ApplicationController, TeacherPanelController
resources/views/              → Blade prikazi za sve uloge
```

---

## 📌 Napomena

- `.env` datoteka nije uključena u repozitorij (koristi `.env.example`)
- Laravel koristi Breeze, pa su sve osnovne auth rute već postavljene

---

## 👨‍💻 Autor

Patrik Makaj  
**Fakultet elektrotehnike, računarstva i informacijskih tehnologija Osijek**  
Kolegij: Napredno web programiranje – LV5  
2025.
