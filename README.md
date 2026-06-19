# js
Ushbu topshiriq mantiqiy && (VA) operatorini qo'llashga juda yaxshi misol bo'ladi. Bu operator ikkala shart ham bir vaqtda to'g'ri (true) bo'lgandagina ishlaydi.

O'qituvchingizga topshirish uchun tayyor kod va README.md faylini quyida keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * 3-Loyiha: "Kino zaliga kirish nazorati"
 * Vazifasi: Foydalanuvchining yoshi va puliga qarab kinoga ruxsat berish yoki rad etish
 */

// 1. O'zgaruvchilarni e'lon qilish (Qiymatlarni o'zgartirib tekshirib ko'rishingiz mumkin)
let yoshi = 18;       // Foydalanuvchi yoshi
let puli = 25000;     // Foydalanuvchi puli (so'mda)

console.log(`=== KINO NAZORATI: Yoshi: ${yoshi} | Puli: ${puli} so'm ===`);

// 2. Mantiqiy operator (&&) yordamida shartni tekshirish
if (yoshi > 16 && puli > 20000) {
    console.log("Kinoga kirishingiz mumkin");
} else {
    console.log("Kirish taqiqlanadi");
}
2. README.md fayli tarkibi
Markdown
# 3-Loyiha: Kino zaliga kirish nazorati

Ushbu kichik dastur JavaScript-da `if-else` shartli operatori va `&&` (VA) mantiqiy operatoridan foydalanishni namoyish etadi.

## 📋 Qoidalar

Dastur foydalanuvchiga kinoga kirishga ruxsat berishi uchun quyidagi **ikkala shart ham** bir vaqtda bajarilishi shart:
1. Foydalanuvchi yoshi **16 dan katta** bo'lishi kerak.
2. Foydalanuvchi puli **20 000 so'mdan ko'p** bo'lishi kerak.

Agar ushbu shartlardan aqalli bittasi bajarilmay qolsa, tizim kirishni taqiqlaydi.

## 💻 Ishga tushirish

Terminalda quyidagi buyruq orqali dasturni ishga tushiring:
```bash
node script.js
