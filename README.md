# js
Kutubxona tizimi vazifasini JavaScript massiv metodlari (push, shift) va for tsikli yordamida to'liq va xatosiz bajaramiz.

Loyihangiz xuddi avvalgi topshiriqlardek chiroyli tartibda bo'lishi uchun quyidagi ikki faylni yarating.

1. script.js fayli kodi
JavaScript
/**
 * Loyiha: Kutubxona Tizimi
 * Tavsif: Massiv metodlari yordamida kitoblar omborini yangilash,
 * elementlarni qo'shish, o'chirish va ularni tartib bilan konsolga chiqarish.
 */

// 1. Dastlabki 3 ta kitobdan iborat massiv yaratamiz
const kitoblar = ["Dunyoning ishlari", "Sariq devni minib", "Yulduzli tunlar"];

// 2. Yangi kitoblarni massivning OXIRIGA qo'shamiz
kitoblar.push("O'tkan kunlar", "Kichik shahzoda");

// 3. Eng BIRINCHI turgan kitobni massiv boshidan o'chirib tashlaymiz
const olibKetilganKitob = kitoblar.shift();

// Qo'shimcha: Qaysi kitob olib ketilganini konsolda ko'rsatish
console.log(`🔔 Bildirishnoma: "${olibKetilganKitob}" kitobi o'quvchi tomonidan olib ketildi.\n`);

// 4. Qolgan barcha kitoblarni for tsikli yordamida tartib raqami bilan chiqaramiz
console.log("================ KUTUBXONADA QOLGAN KITOBLAR ================");

for (let i = 0; i < kitoblar.length; i++) {
    // i o'zgaruvchisi 0 dan boshlangani uchun foydalanuvchiga 1, 2, 3... ko'rinishida ko'rsatamiz
    console.log(`${i + 1}. ${kitoblar[i]}`);
}

console.log("============================================================");
2. README.md fayli tarkibi
Markdown
# Kutubxona Boshqaruv Tizimi

Ushbu amaliy loyiha JavaScript tilida massivlar (Array) va ularning asosiy metodlari bilan ishlashni ko'rsatib beradi.

## 📋 Bajarilgan Qadamlar

1. `kitoblar` nomli boshlang'ich massiv e'lon qilindi.
2. `push()` metodi orqali massiv oxiriga yangi kitoblar muvaffaqiyatli qo'shildi.
3. `shift()` metodi yordamida eng birinchi element (kitob) ro'yxatdan o'chirildi.
4. `for` tsikli yordamida omborda qolgan kitoblar tartib raqami (`1, 2, 3...`) bilan konsolga chiqarildi.

## 💻 Ishga tushirish yo'riqnomasi

Dasturni kompyuteringizda ishga tushirish uchun quyidagi buyruqni terminalda bajaring:

```bash
node script.js
📊 Kutilayotgan Natija
Plaintext
🔔 Bildirishnoma: "Dunyoning ishlari" kitobi o'quvchi tomonidan olib ketildi.

================ KUTUBXONADA QOLGAN KITOBLAR ================
1. Sariq devni minib
2. Yulduzli tunlar
3. O'tkan kunlar
4. Kichik shahzoda
============================================================
