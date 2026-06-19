# js
JavaScript-da funksiyalar bilan ishlash, parametrlarni uzatish va return operatori yordamida qiymat qaytarishni o'rganish uchun ajoyib vazifa.

Siz so'ragan onlayn do'kon mantiqini hisoblaydigan tayyor kod va uning README.md faylini quyida keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * Loyiha: Onlayn Do'kon Tizimi (Xaridni Hisoblash)
 * Tavsif: Mahsulot narxi va miqdoriga qarab umumiy summani hisoblash
 * hamda ma'lum miqdordan oshganda chegirma qo'llash funksiyalari.
 */

// 1. Umumiy summani hisoblaydigan funksiya
function hisobla(mahsulotNarxi, miqdori) {
    return mahsulotNarxi * miqdori;
}

// 2. Chegirma hisoblaydigan funksiya
function chegirmaBer(umumiySumma) {
    // Agar summa 100 000 so'mdan ko'p bo'lsa, 10% chegirma qilinadi
    if (umumiySumma > 100000) {
        let chegirmaMiqdori = umumiySumma * 0.10; // 10% ni hisoblash
        return umumiySumma - chegirmaMiqdori;    // Yakuniy narx
    } else {
        return umumiySumma; // Chegirmasiz asl narx
    }
}

// 3. Funksiyalarni chaqirish va natijani aniqlash
const narx = 40000;  // 1 ta mahsulot narxi
const soni = 3;      // Olingan mahsulot miqdori

// Birinchi funksiya orqali jami summani topamiz (40000 * 3 = 120000)
const jamiSumma = hisobla(narx, soni);

// Ikkinchi funksiya orqali chegirmani tekshiramiz
const yakuniyToLov = chegirmaBer(jamiSumma);

// 4. Natijani konsolga chiqarish
console.log("================ XARID CHEKI ================");
console.log(`Mahsulot narxi: ${narx} so'm`);
console.log(`Miqdori: ${soni} ta`);
console.log(`Asl jami summa: ${jamiSumma} so'm`);
console.log("--------------------------------------------");
console.log(`Yakuniy to'lov miqdori (Chegirma bilan): ${yakuniyToLov} so'm`);
console.log("============================================");
2. README.md fayli tarkibi
Markdown
# Onlayn Do'kon Xarid Tizimi

Ushbu loyiha JavaScript-da funksiyalar (functions), parametrlardan foydalanish va shartli operatorlar yordamida mantiqiy hisob-kitoblarni bajarishni o'rgatadi.

## ⚙️ Funksiyalar Qanday Ishlaydi?

1. `hisobla(mahsulotNarxi, miqdori)`:
   - Mahsulotning donasini uning narxiga ko'paytirib, umumiy summani chiqaradi.
2. `chegirmaBer(umumiySumma)`:
   - Agar jami summa **100 000 so'mdan** oshsa, xaridorga **10% chegirma** taqdim etadi. Aks holda narx o'zgarmaydi.

## 💻 Ishga tushirish yo'riqnomasi

Dasturni terminal orqali ishga tushirish uchun quyidagi buyruqni yozing:

```bash
node script.js
📊 Hisoblash Ssenariysi
3 ta 40 000 so'mlik mahsulot = 120 000 so'm.

120 000 so'm > 100 000 so'm bo'lgani uchun 10% chegirma chegiriladi (12 000 so'm).

Yakuniy to'lov: 108 000 so'm.
