# js
JavaScript-da localStorage yordamida oddiy hisoblagich (Counter) qiymatini saqlab qolish tizimini tuzamiz. Bu sahifa yangilanganda ham ma'lumotlar yo'qolmasligini ta'minlaydi.

Topshiriq shartlariga mos keladigan kodlar va uning README.md faylini quyida keltiraman.

1. index.html va script.js kodlari
index.html fayli:
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LocalStorage Hisoblagich</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #hisobEkran {
            font-size: 48px;
            margin-bottom: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <div id="hisobEkran">0</div>
    <button id="oshirishTugmasi">Oshirish (+1)</button>

    <script src="script.js"></script>
</body>
</html>
script.js fayli:
JavaScript
/**
 * Loyiha: LocalStorage Hisoblagich Tizimi
 * Tavsif: Tugma bosilganda sonni oshirish va uni xotiraga saqlash.
 * Sahifa yangilanganda xotiradagi qiymatni tiklash.
 */

// 2. Elementlarni o'zgaruvchilarga tutib olish
const hisobEkran = document.getElementById("hisobEkran");
const oshirishTugmasi = document.getElementById("oshirishTugmasi");

// 3. Dastur boshida LocalStorage-dan eski qiymatni tekshirib olish
// LocalStorage ma'lumotni string (matn) ko'rinishida saqlagani uchun uni Number() bilan songa o'giramiz
let joriyHisob = Number(localStorage.getItem("hisoblagichQiymati")) || 0;

// Ekranga boshlang'ich yoki xotiradan olingan qiymatni chiqarish
hisobEkran.textContent = joriyHisob;

// 4. Tugmaga click hodisasini biriktirish
oshirishTugmasi.addEventListener("click", function() {
    // Sonni 1 taga oshirish
    joriyHisob++;

    // Yangi qiymatni ekranda ko'rsatish
    hisobEkran.textContent = joriyHisob;

    // Yangi qiymatni LocalStorage xotirasiga yozib qo'yish
    localStorage.setItem("hisoblagichQiymati", joriyHisob);
});
2. README.md fayli tarkibi
Markdown
# LocalStorage Hisoblagich Loyihasi

Ushbu loyiha JavaScript-da sonli ma'lumotlar bilan ishlash hamda `localStorage` yordamida ularni brauzer xotirasida saqlab qolishni o'rgatadi.

## ⚙️ Loyiha qanday ishlaydi?

1. **Xotirani tekshirish va tiklash:** Dastur ishga tushganda `localStorage.getItem("hisoblagichQiymati")` buyrug'i orqali xotira tekshiriladi. Agar u yerda son bo'lsa, hisoblagich o'sha sondan davom etadi. Agar xotira bo'sh bo'lsa, `|| 0` mantiqiy operatori tufayli hisob `0` dan boshlanadi.
2. **Ma'lumot turini o'girish:** Xotiradan olingan matn ko'rinishidagi ma'lumot matematik amallar to'g'ri bajarilishi uchun `Number()` funksiyasi orqali songa o'tkaziladi.
3. **Xotirani yangilash:** Tugma har bosilganda qiymat bittaga oshadi va `localStorage.setItem` yordamida xotiradagi eski qiymat ustiga yangisi yoziladi.

## 💻 Ishga tushirish yo'riqnomasi

1. Kodlarni bitta papkaga `index.html` va `script.js` nomlari bilan saqlang.
2. `index.html` faylini istalgan brauzerda oching.
3. Tugmani bir nechta mantiqan bosing, so'ng sahifani yangilab (`F5` yoki `Refresh`) hisob nolga qaytmaganini kuzating.
