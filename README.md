# js
Bu topshiriq JavaScript-dagi switch-case va murakkab mantiqiy operatorlarni (&&, ||, !) birgalikda ishlatishni o'rganish uchun juda yaxshi namuna hisoblanadi.

O'qituvchingizga topshirish uchun tayyor script.js kodi va uning README.md qo'llanmasini quyida keltiraman.

1. script.js fayli kodi
JavaScript
/**
 * 2-Loyiha: "Virtual Kafedra Yordamchisi"
 * Vazifasi: Haftaning kuni va talabaning holatiga qarab kun tartibini belgilash
 */

// 1. O'zgaruvchilarni e'lon qilish (Sinash uchun qiymatlarni o'zgartirishingiz mumkin)
let haftaningKuni = "Dushanba"; // Dushanba - Yakshanba oralig'ida
let imtihonBor = false;
let vazifaBajarildi = true;

console.log(`=== VIRTUAL YORDAMCHI: Kun: ${haftaningKuni} | Imtihon: ${imtihonBor} | Vazifa: ${vazifaBajarildi} ===\n`);

// Yordamchi mantiqiy bayroqlar (Flag) shartlarni tekshirishni osonlashtiradi
let darsKuni = false;
let damOlishKuni = false;

// 2-qism: Switch-case yordamida kun turini aniqlash
switch (haftaningKuni) {
    case "Dushanba":
    case "Chorshanba":
    case "Juma":
        console.log("1-Qism Natijasi: Bugun asosiy dars kunlari.");
        darsKuni = true;
        break;
        
    case "Seshanba":
    case "Payshanba":
        console.log("1-Qism Natijasi: Bugun amaliyot va laboratoriya kuni.");
        darsKuni = true;
        break;
        
    case "Shanba":
    case "Yakshanba":
        console.log("1-Qism Natijasi: Dam olish kuni.");
        damOlishKuni = true;
        break;
        
    default:
        console.log("Xatolik: Bunday kun mavjud emas!");
}

// 3-qism: Mantiqiy operatorlar (&&, ||, !) yordamida qaror qabul qilish
console.log("------------------------------------------------------------");
console.log("2-Qism (Tavsiya):");

if (darsKuni && imtihonBor) {
    console.log("🚨 Darhol imtihon zaliga kiring!");
} 
else if (!imtihonBor && vazifaBajarildi && darsKuni) {
    console.log("✅ Siz darsga tayyorsiz, kirishingiz mumkin.");
} 
else if (darsKuni && !imtihonBor && !vazifaBajarildi) {
    console.log("❌ Vazifani bajarmaganingiz uchun darsga kiritilmaysiz!");
} 
else if (damOlishKuni) {
    console.log("🎉 Miriqib dam oling!");
}
2. README.md fayli tarkibi
Markdown
# 2-Loyiha: Virtual Kafedra Yordamchisi

Ushbu loyiha JavaScript-da `switch-case` strukturasi va mantiqiy operatorlar (`&&` - VA, `||` - YOKI, `!` - EMAS) bilan ishlash ko'nikmalarini mustahkamlash uchun yaratilgan. Dastur talabaning kunlik holatini tekshirib, unga mos ko'rsatmalar beradi.

## 📋 Loyiha Algoritmi

1. **Switch-case qismi:**
   - Dushanba, Chorshanba, Juma ➡️ *Asosiy dars kunlari*
   - Seshanba, Payshanba ➡️ *Amaliyot va laboratoriya kuni*
   - Shanba, Yakshanba ➡️ *Dam olish kuni*

2. **Mantiqiy shartlar qismi:**
   - Dars kuni bo'lsa **VA** imtihon bo'lsa ➡️ *"Darhol imtihon zaliga kiring!"*
   - Imtihon bo'lmasa **VA** vazifa bajarilgan bo'lsa ➡️ *"Siz darsga tayyorsiz, kirishingiz mumkin."*
   - Dars kuni bo'lsa-yu, lekin imtihon ham, vazifa ham bo'lmasa ➡️ *"Vazifani bajarmaganingiz uchun darsga kiritilmaysiz!"*
   - Dam olish kuni bo'lsa ➡️ *"Miriqib dam oling!"*

## 🛠 Texnologiyalar
* **Til:** JavaScript (ES6+)
* **Ishga tushirish muhiti:** Node.js

## 💻 Ishga tushirish qadadamlari

1. Loyiha papkasida terminalni oching.
2. Dasturni ishga tushirish uchun quyidagi buyruqni bosing:
   ```bash
   node script.js
🧪 Testlash (Tekshirish)
Koddagi haftaningKuni, imtihonBor va vazifaBajarildi o'zgaruvchilari qiymatlarini almashtirib, turli xil ssenariylarni konsolda sinab ko'rishingiz mumkin.


### 💡 Maslahat:
GitHub-ga yuklayotganda har bir loyihani alohida papkada (masalan, `Loyiha-1` va `Loyiha-2`) joylashtirsangiz yoki alohida repositoriya ochsangiz, ustozingiz adashib ketmaydi va kodni tekshirish oson bo'ladi.
