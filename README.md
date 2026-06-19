# js
Mana, barcha talablarga javob beradigan JavaScript kodi va uning README.md qo'llanmasi.

1. script.js fayli
JavaScript
/**
 * Dastur tavsifi:
 * Ushbu dastur JavaScript-da o'zgaruvchilarni e'lon qilish (const va let),
 * ularning qiymatlarini o'zgartirish hamda ma'lumotlarni konsolga 
 * turli usullarda chiroyli formatda chiqarishni namoyish etadi.
 */

// 1. O'zgaruvchilarni e'lon qilish
const ism = "Asilbek";
let yosh = 16;
let shahar = "Toshkent";
const pi = 3.14159;

// 2. Konsolga dastlabki ma'lumotlarni chiqarish (Chiroyli formatda)
console.log("================= FOYDALANUVCHI MA'LUMOTLARI =================");
console.log(`Boshlang'ich holat -> Ism: ${ism}, Yosh: ${yosh}, Shahar: ${shahar}`);
console.log(`Matematik konstanta -> PI qiymati: ${pi}`);
console.log("------------------------------------------------------------");

// 3. 'let' yordamida yaratilgan o'zgaruvchini o'zgartirish
yosh = 17; // Yosh 1 taga oshdi

// 4. 'const' ni o'zgartirishga urinish (Xatolik bergani uchun izohga olingan)
// ism = "Eldor"; // TypeError: Assignment to constant variable.
// pi = 3.14;     // TypeError: Assignment to constant variable.

// 5. O'zgartirilgan ma'lumotlarni konsolga chiqarish
console.log(`Yangilangan holat  -> Ism o'zgarmadi: ${ism}, Yangi yosh: ${yosh}`);
console.log("============================================================");
2. README.md fayli
Markdown
# JavaScript O'zgaruvchilar bilan Ishlash Dasturi

Ushbu loyiha JavaScript tilida `const` va `let` kalit so'zlari orqali o'zgaruvchilar yaratish, ularni boshqarish va konsolga formatlangan holatda chiqarishni ko'rsatib beradi.

## Tizim talablari

Dasturni ishga tushirish uchun kompyuteringizda **Node.js** o'rnatilgan bo'lishi lozim.

## Ishga tushirish yo'riqnomasi

1. **Kodni saqlang:**
   Yuqoridagi kodlarni kompyuteringizda bitta papka ichiga `script.js` va `README.md` nomi bilan saqlang.

2. **Terminalni oching:**
   Kodingiz joylashgan papkaga terminal (yoki komandalar satri - CMD) orqali kiring.

3. **Dasturni ishga tushiring:**
   Terminalda quyidagi buyruqni yozing va `Enter` tugmasini bosing:

   ```bash
   node script.js
Kutilayotgan natija
Terminalda quyidagicha chiroyli formatlangan matn paydo bo'ladi:

Plaintext
================= FOYDALANUVCHI MA'LUMOTLARI =================
Boshlang'ich holat -> Ism: Asilbek, Yosh: 16, Shahar: Toshkent
Matematik konstanta -> PI qiymati: 3.14159
------------------------------------------------------------
Yangilangan holat  -> Ism o'zgarmadi: Asilbek, Yangi yosh: 17
============================================================
