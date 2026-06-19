# js
JavaScript-da DOM manipulyatsiyasi yordamida elementlarni dinamik ravishda yaratish, ularga hodisalar biriktirish va o'chirish (to-do list yoki ro'yxat shakllantirish) bo'yicha juda muhim va amaliy vazifa.

Topshiriq shartlariga to'liq mos keladigan HTML va JavaScript kodlarini hamda README.md qo'llanmasini quyida keltiraman.

1. index.html va script.js kodlari
index.html fayli:
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dinamik Ro'yxat Tizimi</title>
    <style>
        /* Ro'yxat chiroyli ko'rinishi uchun biroz uslub beramiz */
        li {
            margin: 5px 0;
            font-size: 18px;
        }
        .ochirish-tugmasi {
            margin-left: 10px;
            color: red;
            cursor: pointer;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h2>Foydalanuvchilar Ro'yxati</h2>
    <input type="text" id="ismInput" placeholder="Ism kiriting...">
    <button id="qoshishTugmasi">Qo'shish</button>
    
    <ul id="ismRo'yxati"></ul>

    <script src="script.js"></script>
</body>
</html>
script.js fayli:
JavaScript
/**
 * Loyiha: Dinamik Ismlar Ro'yxati
 * Tavsif: Inputga yozilgan ismni tugma bosilganda ro'yxatga (ul) qo'shish,
 * har bir element yonida o'chirish (X) tugmasini yaratish va inputni tozalash.
 */

// 2. Elementlarni o'zgaruvchilarga tutib olish
const ismInput = document.getElementById("ismInput");
const qoshishTugmasi = document.getElementById("qoshishTugmasi");
const ismRoyxati = document.getElementById("ismRo'yxati");

// 3. Qo'shish tugmasiga click hodisasini biriktirish
qoshishTugmasi.addEventListener("click", function() {
    // Input ichidagi matnni olish va bo'sh joylarni qirqish (.trim())
    const kiritilganIsm = ismInput.value.trim();

    // Foydalanuvchi bo'sh matn kiritishini oldini olish
    if (kiritilganIsm === "") {
        alert("Iltimos, ism kiriting!");
        return;
    }

    // Yangi <li> elementi yaratish va matnni yozish
    const yangiLi = document.createElement("li");
    yangiLi.textContent = kiritilganIsm;

    // Yangi o'chirish tugmasi (X) yaratish
    const ochirishTugmasi = document.createElement("button");
    ochirishTugmasi.textContent = "X";
    ochirishTugmasi.className = "ochirish-tugmasi";

    // O'chirish tugmasi bosilganda <li> elementini o'chirish
    ochirishTugmasi.addEventListener("click", function() {
        yangiLi.remove();
    });

    // "X" tugmasini <li> ichiga joylashtirish
    yangiLi.appendChild(ochirishTugmasi);

    // <li> ni <ul> ro'yxatining ichiga qo'shish
    ismRoyxati.appendChild(yangiLi);

    // Oxirida input ichini bo'shatib qo'yish
    ismInput.value = "";
    
    // Kursorni yana input ichiga qaytarish (qulaylik uchun)
    ismInput.focus();
});
2. README.md fayli tarkibi
Markdown
# Dinamik Ro'yxat Yaratishtiruvchi Dastur

Ushbu loyiha JavaScript-da elementlarni havoda (dinamik) yaratish (`document.createElement`), ularga xususiyat hamda hodisalar yuklash va DOM-dan o'chirish (`.remove()`) amallarini o'rgatadi.

## 📋 Algoritm Qadamlari

1. HTML-da kiritish maydoni (`<input>`), tugma va bo'sh ro'yxat (`<ul>`) tayyorlandi.
2. JavaScript-da qo'shish tugmasi bosilganda inputdagi qiymat tekshirib olindi.
3. Yangi `<li>` elementi yaratilib, uning ichiga matn joylashtirildi.
4. Har bir element uchun alohida o'chirish tugmasi yaratilib, unga o'zining otasi bo'lgan `<li>`ni o'chirib tashlash vazifasi (`.remove()`) yuklandi.
5. `appendChild` yordamida elementlar iyerarxiyasi yig'ildi va input qiymati tozalab qo'yildi.

## 💻 Ishga tushirish yo'riqnomasi

1. Kodlarni bitta papkaga `index.html` va `script.js` nomlari bilan saqlang.
2. `index.html` faylini istalgan brauzerda ishga tushiring.
3. Ism yozib "Qo'shish" tugmasini bosing, so'ng o'chirish uchun "X" tugmasidan foydalaning.
