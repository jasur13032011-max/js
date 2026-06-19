# js
JavaScript-da for tsikli va if shart operatori yordamida berilgan orliqdagi juft sonlarni ajratish hamda ularning yig'indisini hisoblash juda oson.

Quyida ushbu vazifa uchun toza yozilgan script.js kodi va uning tushunarli README.md faylini keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * Loyiha: Juft sonlar yig'indisini hisoblash
 * Tavsif: 1 dan 50 gacha bo'lgan sonlar ichidan faqat juftlarini ajratib olib,
 * ularning umumiy yig'indisini for tsikli yordamida hisoblash.
 */

let yigindi = 0; // Yig'indini saqlash uchun o'zgaruvchi

// 1 dan 50 gacha bo'lgan sonlarni aylanish (50 ning o'zi ham kiradi: <=)
for (let i = 1; i <= 50; i++) {
    // Sonni 2 ga bo'lgandagi qoldiq 0 bo'lsa, u juft son hisoblanadi
    if (i % 2 === 0) {
        yigindi += i; // Juft sonni yig'indiga qo'shish
    }
}

// Yakuniy natijani konsolga chiqarish
console.log("================== NATIJA ==================");
console.log(`1 dan 50 gacha bo'lgan juft sonlar yig'indisi: ${yigindi}`);
console.log("============================================");
2. README.md fayli tarkibi
Markdown
# Juft Sonlar Yig'indisini Hisoblash Dasturi

Ushbu mantiqiy dastur JavaScript-da `for` tsikli va qoldikli bo'lish (`%`) operatori yordamida ma'lum bir orliqdagi sonlarni saralashni o'rgatadi.

## 📋 Algoritm Qadamlari

1. Yig'indini hisoblab borish uchun boshlang'ich qiymati `0` bo'lgan `yigindi` o'zgaruvchisi yaratildi.
2. `for` tsikli orqali 1 dan 50 gacha bo'lgan barcha sonlar birma-bir ko'rib chiqiladi.
3. `if (i % 2 === 0)` sharti yordamida har bir sonning juft yoki toqligi tekshiriladi.
4. Agar son juft bo'lsa, u `yigindi` o'zgaruvchisiga qo'shib boriladi.

## 💻 Ishga tushirish yo'riqnomasi

Dasturni terminalda ishga tushirish uchun quyidagi buyruqni yozing:

```bash
node script.js
📊 Matematik Natija
Matematik formulaga ko'ra ham 2 dan 50 gacha bo'lgan juft sonlar yig'indisi 650 ga teng chiqadi.
