# js
Mana, so'ralgan ikkala vazifani ham o'z ichiga olgan toza va tushunarli JavaScript kodi hamda loyiha uchun README.md fayli.

Ushbu kodda brauzer muhitida foydalanuvchidan ma'lumot olish uchun prompt() funksiyasidan foydalanildi (agar Node.js-da ishlatmoqchi bo'lsangiz, o'zgaruvchiga to'g'ridan-to'g'ri qiymat berib sinashingiz mumkin).

1. script.js fayli kodi
JavaScript
/**
 * 4-Loyiha: "Parol Tekshirish va Mahsulotlar Ro'yxati"
 * Vazifasi: 
 * 1. while tsikli yordamida parolni 3 marta tekshirish va bloklash.
 * 2. for tsikli yordamida massivdagi mahsulotlarni konsolga chiqarish.
 */

// ==========================================
// 1-QISM: While tsikli bilan parol tekshirish
// ==========================================
console.log("================= TIZIMGA KIRISH =================");

const TO_GRI_PAROL = "Admin123";
let urinishlarSoni = 0;
let tizimgaKirdi = false;

while (urinishlarSoni < 3) {
    let kiritilganParol = prompt("Iltimos, parolni kiriting:");
    urinishlarSoni++;

    if (kiritilganParol === TO_GRI_PAROL) {
        console.log("✅ Xush kelibsiz! Tizimga muvaffaqiyatli kirdingiz.");
        tizimgaKirdi = true;
        break; // Parol to'g'ri bo'lsa, tsikl darhol to'xtatiladi
    } else {
        // Agar urinishlar tugamagan bo'lsa, ogohlantirish beramiz
        if (urinishlarSoni < 3) {
            console.log(`❌ Parol noto'g'ri. Qolgan urinishlar: ${3 - urinishlarSoni}`);
        }
    }
}

// 3 ta urinishdan keyin ham parol topilmasa
if (!tizimgaKirdi) {
    console.log("🚨 Karta bloklandi! Bankka murojaat qiling.");
}

console.log("==================================================\n");


// ==========================================
// 2-QISM: For tsikli bilan massivni aylanish
// ==========================================
console.log("================ MAHSULOTLAR DO'KONI ================");

// Mahsulotlar ob'ektlaridan iborat massiv (Array)
const mahsulotlar = [
    { nom: "Noutbuk", narx: 8000000 },
    { nom: "Smartfon", narx: 4500000 },
    { nom: "Simsiz quloqchin", narx: 600000 },
    { nom: "Aqlli soat", narx: 1200000 },
    { nom: "Klaviatura", narx: 350000 }
];

// For tsikli yordamida ketma-ket chiqarish
for (let i = 0; i < mahsulotlar.length; i++) {
    let joriyMahsulot = mahsulotlar[i];
    console.log(`${i + 1}. ${joriyMahsulot.nom} - Narxi: ${joriyMahsulot.narx} so'm`);
}

console.log("====================================================");
2. README.md fayli tarkibi
Markdown
# 4-Loyiha: Parol Tekshirish va Do'kon Tizimi

Ushbu loyiha JavaScript tilidagi tsikllar (`while`, `for`) va o'tish operatorlari (`break`) bilan ishlashni mustahkamlashga xizmat qiladi.

## 📝 Loyiha Qismlari

1. **Parol Nazorati (`while` tsikli):**
   - Foydalanuvchiga to'g'ri parolni kiritish uchun **3 ta imkoniyat** beriladi.
   - Parol to'g'ri topilsa, `break` operatori orqali tsikl to'xtatiladi va xush kelibsiz xabari chiqadi.
   - 3 ta urinish muvaffaqiyatsiz tugasa, *"Karta bloklandi"* xabari ko'rsatiladi.

2. **Mahsulotlar Ro'yxati (`for` tsikli):**
   - Ichida kamida 5 ta mahsulot (nomi va narxi) bo'lgan massiv yaratilgan.
   - `for` tsikli massivning har bir elementini ketma-ket konsolga tartib raqami bilan chiroyli ko'rinishda chiqaradi.

## 🛠 Texnologiyalar
* **Til:** JavaScript (ES6+)
* **Ishga tushirish muhiti:** Brauzer (DevTools konsoli) yoki Node.js

## 💻 Ishga tushirish qadamlari

Dasturda `prompt()` funksiyasi ishlatilgani sababli, uni **brauzer konsolida** ishga tushirish tavsiya etiladi:
1. `index.html` fayli ochib, unga `script.js` faylini ulang.
2. Sahifani brauzerda oching va `F12` (Konsol) tugmasini bosing.
3. Ekranga chiqqan oynaga parolni kiriting (To'g'ri parol: `Admin123`).
