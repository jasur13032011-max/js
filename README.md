# js
Ustozning fikridan ko'rinib turibdiki, siz adashib boshqa loyihaning (kutubxona tizimi) kodini yuklab yuborgansiz. Ushbu xatolikni to'g'rilash va loyihani qayta topshirib, yuqori baho olishingiz uchun aynan "Aqlli Svetofor va Yo'l qoidasi" shartlariga mos keladigan JavaScript kodi va mukammal README.md faylini tayyorlab beraman.

Siz bu safar GitHub-da ham script.js (kod uchun), ham README.md (tavsif uchun) fayllarini alohida yaratsangiz, baholash yanada yuqori bo'ladi.

1. script.js fayli kodi
Bu faylga o'qituvchi talab qilgan barcha if, else if va else shartlari to'liq kiritilgan. Sinab ko'rish uchun o'zgaruvchilar qiymatini o'zgartirishingiz mumkin.

JavaScript
/**
 * 1-Loyiha: "Aqlli Svetofor va Yo'l qoidasi"
 * Muallif: [Sizning Ismingiz]
 * Vazifasi: Svetofor rangi va mashina tezligiga qarab haydovchiga ko'rsatma berish
 */

// O'zgaruvchilarni e'lon qilish (Qiymatlarni o'zgartirib tekshirib ko'rishingiz mumkin)
let svetoforRangi = "qizil"; // "qizil", "sariq", "yashil" yoki boshqa qiymat
let mashinaTezligi = 45;      // Mashina tezligi (km/s)

console.log(`=== TIZIM: Svetofor: ${svetoforRangi.toUpperCase()} | Tezlik: ${mashinaTezligi} km/s ===`);

// 1-shart: Qizil chiroq
if (svetoforRangi === "qizil") {
    if (mashinaTezligi === 0) {
        console.log("To'g'ri, to'xtab turibsiz.");
    } else if (mashinaTezligi > 0) {
        console.log("Taqiqlangan! Sizga jarima yozildi!");
    }
} 
// 2-shart: Sariq chiroq
else if (svetoforRangi === "sariq") {
    if (mashinaTezligi > 50) {
        console.log("Tezlikni kamaytiring va to'xtashga tayyorlaning!");
    } else {
        console.log("To'xtab kuting.");
    }
} 
// 3-shart: Yashil chiroq
else if (svetoforRangi === "yashil") {
    console.log("Yo'lingiz ochiq, xavfsiz harakatlaning!");
} 
// 4-shart: Aks holda (Svetofor buzilgan yoki boshqa holat)
else {
    console.log("Svetofor buzilgan, tartibga soluvchiga qarang!");
}
2. README.md fayli tarkibi
Ustozingiz GitHub-da tekshirganda loyiha nima haqidaligini tushunishi va qanday ishga tushirishni ko'rishi uchun ushbu matnni README.md fayliga joylashtiring:

Markdown
# 1-Loyiha: Aqlli Svetofor va Yo'l qoidasi

Ushbu mantiqiy loyiha JavaScript-dagi `if`, `else if` va `else` tarmoqlanish operatorlarini amaliyotda qo'llashni ko'rsatib beradi. Dastur svetofor chirog'i va joriy tezlikka qarab haydovchiga aqlli tavsiyalar yoki ogohlantirishlar beradi.

## 🚀 Loyiha Qoidalari va Shartlari

1. **Qizil chiroq:**
   - Tezlik `0` bo'lsa ➡️ *"To'g'ri, to'xtab turibsiz."*
   - Tezlik `0` dan baland bo'lsa ➡️ *"Taqiqlangan! Sizga jarima yozildi!"*
2. **Sariq chiroq:**
   - Tezlik `50` dan yuqori bo'lsa ➡️ *"Tezlikni kamaytiring va to'xtashga tayyorlaning!"*
   - Tezlik past bo'lsa ➡️ *"To'xtab kuting."*
3. **Yashil chiroq:** - ➡️ *"Yo'lingiz ochiq, xavfsiz harakatlaning!"*
4. **Boshqa holatlar (Noma'lum rang yoki nosozlik):**
   - ➡️ *"Svetofor buzilgan, tartibga soluvchiga qarang!"*

## 🛠 Texnologiyalar
* **Til:** JavaScript (ES6+)
* **Muhit:** Node.js

## 💻 Ishga tushirish yo'riqnomasi

Kompyuteringizda Node.js o'rnatilganligiga ishonch hosil qiling, so'ng terminalda quyidagi buyruqni bajaring:

```bash
node script.js
📈 Tekshirish (Test qilish)
Koddagi svetoforRangi va mashinaTezligi o'zgaruvchilarining qiymatlarini o'zgartirib, dasturning turli vaziyatlarda qanday ishlashini konsolda kuzatishingiz mumkin.


---

### 💡 Ustozga qayta topshirish bo'yicha maslahat:
1. GitHub-dagi eski repositoriyangizga kiring.
2. Ichidagi eski kutubxonaga oid kodlarni o'chirib, yuqoridagi yangi `script.js` va `README.md` fayllarini yuklang (yoki borini tahrirlang).
3. Kamida yana **1-2 ta commit** qiling (masalan, *"feat: svetofor mantiqiy shartlari qo'shildi"* va *"docs: README yangilandi"* deb yozing), shunda o'qituvchi siz xatoni to'g'rilash ustida ishlaganingizni ko'radi.
