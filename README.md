# js
JavaScript-da obyektlar va uning ichidagi xususiyatlarni this kalit so'zi yordamida o'zgartirishni o'rganish uchun ajoyib topshiriq.

Talab qilingan shartlar asosida tayyorlangan script.js kodi va uning README.md faylini quyida keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * Loyiha: O'yinchi ballarini boshqarish tizimi
 * Tavsif: O'yinchi obyekti ichida ochko xususiyatini yaratish va
 * metod yordamida 'this' orqali ochkoni 10 taga oshirish.
 */

// 1. O'yinchi obyektini yaratish
const oyinchi = {
    ism: "Shaxzod",
    ochko: 0, // Boshlang'ich ochko

    // Ochkoni 10 taga oshiruvchi metod
    ochkoOshir: function() {
        this.ochko += 10; // 'this' obyektning o'ziga (oyinchi) ishora qiladi
    }
};

// 2. Dasturni ishga tushirish va tekshirish
console.log("================= O'YIN BOSHLANDI =================");
console.log(`O'yinchi: ${oyinchi.ism} | Boshlang'ich ochko: ${oyinchi.ochko}`);

// Metodni birinchi marta chaqiramiz (0 + 10 = 10)
oyinchi.ochkoOshir();
console.log(`➕ Birinchi muvaffaqiyat! Joriy ochko: ${oyinchi.ochko}`);

// Metodni ikkinchi marta chaqiramiz (10 + 10 = 20)
oyinchi.ochkoOshir();
console.log(`➕ Ikkinchi muvaffaqiyat! Joriy ochko: ${oyinchi.ochko}`);

console.log("===================================================");
2. README.md fayli tarkibi
Markdown
# O'yinchi Ochkosini Oshirish Dasturi

Ushbu kichik loyiha JavaScript tilida obyektlar (Objects) va obyekt metodlari ichida `this` kalit so'zining qanday ishlashini tushuntirib beradi.

## ⚙️ Mantiqiy qism

* `oyinchi` obyektida `ism` va `ochko` xususiyatlari saqlanadi.
* `ochkoOshir` metodi chaqirilganda, `this.ochko` yozuvi orqali aynan shu obyektning ichidagi `ochko` o'zgaruvchisiga kiriladi va uning qiymati **10 taga** oshiriladi (`+= 10`).

## 💻 Ishga tushirish yo'riqnomasi

Dasturni kompyuteringiz terminalida ishga tushirish uchun quyidagi buyruqni yozing:

```bash
node script.js
📊 Kutilayotgan Natija
Plaintext
================= O'YIN BOSHLANDI =================
O'yinchi: Shaxzod | Boshlang'ich ochko: 0
➕ Birinchi muvaffaqiyat! Joriy ochko: 10
➕ Ikkinchi muvaffaqiyat! Joriy ochko: 20
===================================================
