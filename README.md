# js
JavaScript-da obyektlar (Objects), ularning xususiyatlarini o'zgartirish va ichki metodlarda this kalit so'zidan foydalanishni o'rganish uchun juda qiziqarli vazifa.

Avtosalon tizimi mantiqini to'liq bajaradigan script.js kodi va uning README.md qo'llanmasini quyida keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * Loyiha: Avtosalon Boshqaruv Tizimi
 * Tavsif: Mashina obyektini yaratish, xususiyatlarini tashqaridan yangilash,
 * obyekt metodlari va 'this' operatori yordamida qiymatlarni o'zgartirish.
 */

// 1. Mashina obyektini e'lon qilish
const mashina = {
    brend: "Chevrolet",
    model: "Gentra",
    yil: 2022,
    narx: 13000,
    tanirovka: false,

    // Obyekt haqida ma'lumot beruvchi metod
    malumotBering: function() {
        console.log(`Brend: ${this.brend}, Model: ${this.model}, Narxi: ${this.narx}$`);
    },

    // Tanirovka holatini va narxini yangilovchi metod
    tanirovkaQildir: function() {
        this.tanirovka = true;
        this.narx += 500; // Narxiga 500$ qo'shish
        console.log("\n😎 Tanirovka qilindi! Mashina narxiga 500$ qo'shildi.\n");
    }
};

// 2. Obyektdan tashqarida yangi "rang" xususiyatini qo'shish
mashina.rang = "To'q kulrang";

// 3. Obyektdan tashqarida "narx" xususiyatini yangilash
mashina.narx = 12500;

// 4. Dasturiy qadamlarni ketma-ket bajarish
console.log("================= AVTOSALON TIZIMI =================");

// Dastlab ma'lumotlarni chiqaramiz
mashina.malumotBering();

// Tanirovka qilish metodini ishga tushiramiz
mashina.tanirovkaQildir();

// Yakuniy holatni tekshirish uchun butun obyektni konsolga chiqaramiz
console.log("================= YAKUNIY HOLAT =================");
console.log(mashina);
console.log("=================================================");
2. README.md fayli tarkibi
Markdown
# Avtosalon Boshqaruv Tizimi

Ushbu loyiha JavaScript-da Obyektlar (Objects), ularga dinamik ravishda yangi xususiyatlar qo'shish va obyekt ichidagi metodlarda `this` kalit so'zi bilan ishlashni o'rgatadi.

## 🛠 Obyekt mantiqi va o'zgarishlar

1. **Dinamik o'zgarishlar:** `rang` xususiyati obyektdan tashqarida qo'shildi va boshlang'ich `narx` (13000) tashqaridan `12500` ga tushirildi.
2. `malumotBering()` metodi: `this` orqali obyekt ichidagi joriy ma'lumotlarni konsolga chiroyli formatda chiqaradi.
3. `tanirovkaQildir()` metodi: `tanirovka` qiymatini `true` qiladi va mashina narxini automatic ravishda **500$** ga oshiradi.

## 💻 Ishga tushirish yo'riqnomasi

Dasturni terminal orqali ishga tushirish buyrug'i:

```bash
node script.js
📊 Kutilayotgan Natija
Plaintext
================= AVTOSALON TIZIMI =================
Brend: Chevrolet, Model: Gentra, Narxi: 12500$

😎 Tanirovka qilindi! Mashina narxiga 500$ qo'shildi.

================= YAKUNIY HOLAT =================
{
  brend: 'Chevrolet',
  model: 'Gentra',
  yil: 2022,
  narx: 13000,
  tanirovka: true,
  malumotBering: [Function: malumotBering],
  tanirovkaQildir: [Function: tanirovkaQildir],
  rang: "To'q kulrang"
}
=================================================
