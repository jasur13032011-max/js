# js
JavaScript-da brauzer xotirasi — localStorage bilan ishlashni o'rganish uchun juda amaliy va muhim vazifa. Bu usul foydalanuvchi ma'lumotlarini sahifa yangilanganda ham saqlab qolish imkonini beradi.

Topshiriq shartlariga to'liq mos keladigan HTML va JavaScript kodlarini hamda README.md qo'llanmasini quyida keltiraman.

1. index.html va script.js kodlari
index.html fayli:
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LocalStorage bilan ishlash</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        button {
            margin: 5px;
            padding: 5px 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <h1 id="ismEkran">Ism kiritilmagan</h1>
    
    <input type="text" id="ismInput" placeholder="Ismingizni yozing...">
    <button id="eslabQolTugma">Eslab qol</button>
    <button id="ochirishTugma">Xotirani o'chirish</button>

    <script src="script.js"></script>
</body>
</html>
script.js fayli:
JavaScript
/**
 * Loyiha: LocalStorage yordamida ismni eslab qolish tizimi
 * Tavsif: Sahifa yuklanganda xotirani tekshirish, yangi ismni xotiraga yozish 
 * va kerak bo'lganda o'chirish amallarini bajarish.
 */

// 2. Elementlarni o'zgaruvchilarga tutib olish
const ismEkran = document.getElementById("ismEkran");
const ismInput = document.getElementById("ismInput");
const eslabQolTugma = document.getElementById("eslabQolTugma");
const ochirishTugma = document.getElementById("ochirishTugma");

// 3. Dastur boshida har doim LocalStorage-ni tekshirish
const saqlanganIsm = localStorage.getItem("foydalanuvchiIsmi");

if (saqlanganIsm) {
    // Agar xotirada ism bo'lsa, uni h1 ichiga yozamiz
    ismEkran.textContent = saqlanganIsm;
}

// 4. "Eslab qol" tugmasi bosilganda
eslabQolTugma.addEventListener("click", function() {
    const kiritilganIsm = ismInput.value.trim();

    if (kiritilganIsm === "") {
        alert("Iltimos, ism kiriting!");
        return;
    }

    // Ismni LocalStorage xotirasiga saqlash
    localStorage.setItem("foydalanuvchiIsmi", kiritilganIsm);

    // h1 ichidagi matnni o'zgartirish
    ismEkran.textContent = kiritilganIsm;

    // Inputni tozalash
    ismInput.value = "";
});

// 5. "O'chirish" tugmasi bosilganda
ochirishTugma.addEventListener("click", function() {
    // Ismni xotiradan o'chirish
    localStorage.removeItem("foydalanuvchiIsmi");

    // h1 matnini dastlabki holatga keltirish
    ismEkran.textContent = "Ism kiritilmagan";
});
2. README.md fayli tarkibi
Markdown
# LocalStorage Eslab Qolish Tizimi

Ushbu loyiha JavaScript-da brauzerning doimiy xotirasi (`localStorage`) bilan ishlash ko'nikmalarini shakllantirish uchun yaratilgan.

## ⚙️ Loyiha qanday ishlaydi?

1. **Xotirani tekshirish (`getItem`):** Sahifa har safar yuklanganda dastur xotirada `foydalanuvchiIsmi` kaliti bor-yo'qligini tekshiradi va topsa, sarlavhaga chiqaradi.
2. **Xotiraga yozish (`setItem`):** "Eslab qol" tugmasi bosilganda kiritilgan matn brauzer xotirasiga saqlanadi. Sahifa yangilansa ham ma'lumot o'chib ketmaydi.
3. **Xotirani o'chirish (`removeItem`):** "Xotirani o'chirish" tugmasi bosilganda kalit xotiradan butkul o'chiriladi va sarlavha eski holiga qaytadi.

## 💻 Ishga tushirish yo'riqnomasi

1. Fayllarni bitta papkaga joylashtiring.
2. `index.html` faylini brauzerda oching.
3. Ismingizni yozib "Eslab qol" tugmasini bosing va sahifani yangilab (`F5`) tekshirib ko'ring.
