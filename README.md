# js
JavaScript-da massivlar bilan ishlashda eng ko'p qo'llaniladigan va eng muhim hisoblangan filter, find va map metodlarini qo'llash bo'yicha ajoyib amaliy vazifa.

Berilgan mahsulotlar massivi ustida ushbu 3 ta vazifani to'liq bajaruvchi script.js kodi va uning README.md qo'llanmasini quyida keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * Loyiha: Onlayn Do'kon Mahsulotlarini Saralash va Yangilash
 * Tavsif: ES6 massiv metodlari (filter, find, map) yordamida 
 * mahsulotlarni saralash, qidirish va narxlarini aksiya asosida yangilash.
 */

let mahsulotlar = [
    { id: 1, nomi: "Telefon", narxi: 4000000, kategoriya: "Elektronika" },
    { id: 2, nomi: "Ko'ylak", narxi: 300000, kategoriya: "Kiyim" },
    { id: 3, nomi: "Noutbuk", narxi: 8000000, kategoriya: "Elektronika" },
    { id: 4, nomi: "Tufli", narxi: 500000, kategoriya: "Kiyim" }
];

console.log("================= DO'KON TIZIMI =================");

// 1. Saralash (filter yordamida): Faqat "Kiyim" kategoriyasini ajratish
const kiyimlar = mahsulotlar.filter(mahsulot => mahsulot.kategoriya === "Kiyim");

console.log("👕 1-Vazifa: 'Kiyim' kategoriyasidagi mahsulotlar:");
console.log(kiyimlar);
console.log("-------------------------------------------------");


// 2. Qidirish (find yordamida): ID raqami 3 ga teng mahsulotni topish va nomini chiqarish
const topilganMahsulot = mahsulotlar.find(mahsulot => mahsulot.id === 3);

console.log("🔍 2-Vazifa: ID-si 3 ga teng bo'lgan mahsulot nomi:");
if (topilganMahsulot) {
    console.log(`Nomi: ${topilganMahsulot.nomi}`);
} else {
    console.log("Mahsulot topilmadi.");
}
console.log("-------------------------------------------------");


// 3. O'zgartirish (map yordamida): Narxlarni 20% ga arzonlashtirish (Asl narx * 0.8)
const arzonlashganMahsulotlar = mahsulotlar.map(mahsulot => {
    return {
        ...mahsulot,               // Obyektning eski xususiyatlarini saqlab qolamiz
        narxi: mahsulot.narxi * 0.8 // Faqat narxini yangilaymiz
    };
});

console.log("🎉 3-Vazifa: 20% Lik Aksiya! Yangilangan mahsulotlar ro'yxati:");
console.log(arzonlashganMahsulotlar);
console.log("=================================================");
2. README.md fayli tarkibi
Markdown
# Mahsulotlar Massivi bilan Ishlash (ES6+)

Ushbu loyiha JavaScript-da zamonaviy massiv metodlari (`filter`, `find`, `map`) bilan ishlash ko'nikmalarini amaliy tushuntirish uchun yaratilgan.

## 🛠 Ishlatilgan Metodlar va Vazifalari

1. `filter()` — Berilgan shartga mos keluvchi barcha elementlarni ajratib, **yangi massiv** qaytaradi (Bizda faqat "Kiyim" kategoriyasidagilarni ajratish uchun ishlatildi).
2. `find()` — Massiv ichidan shartga mos keladigan **eng birinchi elementning o'zini** qaytaradi (Bizda ID raqami 3 bo'lgan noutbukni topishda qo'llanildi).
3. `map()` — Massivning har bir elementini aylanib chiqib, ularni o'zgartirgan holda xuddi shu hajmdagi **yangi massiv** qaytaradi (Barcha mahsulotlar narxini 20% ga kamaytirishda foydalanildi).

## 💻 Ishga tushirish yo'riqnomasi

Dasturni kompyuteringiz terminalida sinab ko'rish uchun quyidagi buyruqni bosing:

```bash
node script.js
