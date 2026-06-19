# js
JavaScript-da DOM (Document Object Model) bilan ishlash, elementlarni tanlab olish va tugma bosilganda sahifa uslublarini (CSS) o'zgartirishni o'rganish uchun juda amaliy vazifa. Bu odatda saytlarda "Tungi rejim" (Dark mode) funksiyasini yaratishda qo'llaniladi.

Topshiriq talablariga mos keladigan HTML, JavaScript kodlarini va uning README.md qo'llanmasini quyida keltiraman.

1. index.html va script.js kodlari
Loyihangiz to'g'ri ishlashi uchun bitta papkada index.html va script.js fayllarini yarating.

index.html fayli:
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rangni o'zgartirish tizimi</title>
</head>
<body>

    <h1 id="sarlavha">Xush kelibsiz!</h1>
    <p id="matn">Bu sahifadagi matn. Tugma bosilganda ushbu matn va fon rangi o'zgaradi.</p>
    <button id="rejimTugmasi">Tungi rejimga o'tish</button>

    <script src="script.js"></script>
</body>
</html>
script.js fayli:
JavaScript
/**
 * Loyiha: Sahifa rejimini o'zgartirish (Dark Mode)
 * Tavsif: Tugma bosilganda sahifa foni, matnlar rangi va 
 * tugma matnini dinamik ravishda o'zgartirish.
 */

// 2. Elementlarni o'zgaruvchilarga tutib olish
const sahifaBodi = document.body;
const tugma = document.getElementById("rejimTugmasi");
const sarlavha = document.getElementById("sarlavha");
const matn = document.getElementById("matn");

// 3. Tugmaga 'click' hodisasini biriktirish
tugma.addEventListener("click", function() {
    
    // 4. Sahifaning fon rangini qora qilish
    sahifaBodi.style.backgroundColor = "black";

    // Sarlavha va matnlar rangini oq rangga o'tkazish
    sarlavha.style.color = "white";
    matn.style.color = "white";

    // Tugma ichidagi matnni o'zgartirish
    tugma.textContent = "Kunduzgi rejimga o'tish";
});
2. README.md fayli tarkibi
Markdown
# Sahifa Rejimini O'zgartirish Loyihasi

Ushbu loyiha JavaScript yordamida brauzer darchasidagi HTML elementlarini boshqarish (DOM manipulyatsiyasi) va hodisalarni tinglash (`addEventListener`) ko'nikmasini rivojlantirish uchun yaratilgan.

## 📋 Bajarilgan vazifalar:
1. HTMLda `h1`, `p`, va `button` elementlari yaratilib, tegishli `id`lar biriktirildi.
2. JavaScriptda `document.getElementById` va `document.body` orqali elementlar tutib olindi.
3. `click` hodisasi yordamida tugma bosilganda sahifaning CSS uslublari (`style.backgroundColor`, `style.color`) o'zgartirildi.
4. Tugma matni `textContent` xususiyati orqali yangilandi.

## 💻 Ishga tushirish yo'riqnomasi

1. Kodlarni kompyuteringizda bitta papkaga joylang.
2. `index.html` faylini istalgan brauzerda (Chrome, Firefox, Safari) oching.
3. Sahifadagi "Tungi rejimga o'tish" tugmasini bosing va o'zgarishni kuzating.
