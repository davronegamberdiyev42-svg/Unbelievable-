# IELTS Boost — Stage 35.0 Academic Content & Assessment Excellence

**Release:** 35.0.0 · **Sana:** 7 November 2026  
**Deploy:** GitHub Pages · `main` branch · `/(root)`

Stage 35 yangi mini-o‘yin qo‘shmaydi. U 10 ta Power Lab va 100 ta mashq rejimini saqlab, javob dalili, Writing/Speaking self-review va Vocabulary sifatini kuchaytiradi.

## Stage 35 nimalarni yaxshiladi?

### 1. Reading Evidence Check

Power Lab’dagi Reading challenge endi faqat variant belgilashni emas, javobning asosini ham tekshiradi. Oddiy savollarda passage ichidan kamida 8 belgili aynan olingan dalil va reasoning talab qilinadi. NOT GIVEN javobida esa matnda kerakli ma’lumot yo‘qligini asoslash va tashqi bilimga tayanmaslik talab qilinadi.

Content audit: 840 savoldan 812 tasida to‘g‘ridan-to‘g‘ri passage evidence bor; 28 tasi NOT GIVEN holati sifatida qurilgan. Answer index xatolari — 0; izohsiz savollar — 0. Passage uzunligi 722–879 so‘z.

### 2. Listening Evidence Check

Power Lab’dagi Listening javobini topshirish uchun avval o‘sha kun MP3’i oxirigacha tinglangan bo‘lishi, keyin skript ichidagi eshitilgan ibora dalil sifatida kiritilishi kerak. Ixtiro qilingan yoki manbada yo‘q ibora o‘tmaydi.

Content audit: 420/420 savol dalili tegishli listening script bilan mos. 84 ta MP3 mavjud va Stage 35 buildida 84/84 to‘liq decode sinovidan o‘tdi. Ular original IELTS Boost scriptlaridan yaratilgan **sintetik practice audio**; rasmiy IELTS, Cambridge yoki British Council recording emas.

### 3. Writing Rubric 2.0

Writing Power Lab’ning review rejimi to‘rtta mezonni alohida baholaydi. Task 1 uchun **Task Achievement**, Task 2 uchun esa **Task Response** nomi va tavsifi alohida. Har bir mezonga 0–10 internal practice rating va aniq matn dalili kiritiladi. Har bir draft to‘liq bo‘lishi uchun Task 1’da kamida 150, Task 2’da kamida 250 so‘z talab qilinadi.

Band 5–9 ko‘rsatmalari IELTS’ning ochiq band descriptor’lari mazmunidan qisqa parafraza. Ular to‘liq rasmiy descriptor o‘rnini bosmaydi. 0–10 qiymatlar IELTS band score emas; hech qanday avtomatik examiner bahosi berilmaydi.

### 4. Speaking Rubric 2.0

Fluency & Coherence, Lexical Resource, Grammatical Range & Accuracy va Pronunciation alohida tekshiriladi. Review saqlanishidan oldin kun uchun haqiqiy audio yozuvi bo‘lishi, uni qayta tinglash checkbox’i belgilanishi, Part 1/2/3 transcripti va har bir mezon bo‘yicha alohida audio/matn dalili kiritilishi kerak.

**Pronunciation transcriptdan aniqlanmaydi.** Platforma talaffuzni avtomatik examiner darajasida baholamaydi. Bu dalilga asoslangan learner self-review.

### 5. Vocabulary Glossary Curator

19,000 so‘z/ibora indeksida qidirib, yetishmayotgan entry’ni manba bilan to‘ldirish mumkin: English definition, Uzbek sense, original example, part of speech, sense/register note, optional US/UK IPA, definition source URL va alohida CEFR source URL.

CEFR darajasi faqat Oxford/English Profile kabi sense-level manbaning alohida HTTPS URL’i kiritilib tekshirilganda learner-verified sifatida saqlanadi; manba yo‘q yoki yaroqsiz bo‘lsa avtomatik ravishda “Not assessed” bo‘ladi. O‘zgarishlar shu qurilmaning local app state’ida saqlanadi; curated glossary JSON export/import ham mavjud. Umumiy JSON progress backup ham `stage35` state’ini saqlaydi.

**Lug‘at sifati bo‘yicha aniq raqamlar:** 19,000 noyob indeks yozuvi; 677 ta to‘liq bundled gloss; 672 ta kundalik Recall yo‘li uchun to‘liq birlik; 4,000 ta pronunciation-index-only yozuv; 14,323 ta English definition maydoni bo‘sh manual-enrichment yozuvi. 19,000 ta to‘liq tarjima qilingan so‘z deb talqin qilinmasin.

## Baholash qo‘llanmasi

Batafsil criterion-by-criterion self-review tartibi uchun `STAGE35_RUBRIC_GUIDE_UZ.md` faylini och. U Writing Task 1/Task 2, Speaking 4 criteria va Vocabulary source-check amaliyotini tushuntiradi.

## Platformaning umumiy tuzilishi saqlanadi

- 84 kunlik Academic IELTS rejasi va 336 skill sessiyasi.
- 4 core studio: Reading, Listening, Writing, Speaking.
- 6 language lab: Collocation, Pronunciation, Paraphrase, Grammar, Vocabulary Recall, Academic Fluency.
- 10 modul × 10 rejim = 100 mashq rejimi.
- 84 Reading passage / 840 savol; 84 Listening script / 420 savol.
- 84 Task 1 visual: 14 line graph, 14 bar chart, 14 pie chart, 14 table, 14 process, 14 map.
- 84 Speaking cue-card day pack; jami 252 Part 1 va 252 Part 3 prompt.

## GitHub Pages’ga joylash

1. `IELTS_Boost_Stage35_Final_Quality_Release_Deploy.zip` arxivini yuklab olib, och.
2. Ichidagi **barcha fayl va papkalarni** GitHub repository’ning `main` branchidagi root papkaga joyla. `index.html`, `audio/`, `icons/`, `sw.js`, `manifest.webmanifest`, `favicon.svg` va `.nojekyll` joylashuvi saqlansin.
3. GitHub repository → **Settings → Pages**.
4. **Deploy from a branch** → `main` → `/(root)` → **Save**.
5. Saytni HTTPS orqali och. Birinchi yuklanishdan so‘ng PWA shell keshlanadi. MP3’lar faqat birinchi online so‘ralganda bittalab cache’lanadi; 54.87 MiB audio paketi birdaniga install vaqtida yuklanmaydi.

Faqat `index.html` faylini yuklash yetarli emas. Audio va PWA papkalari ham birga joylanishi shart.

## Saqlash va maxfiylik

Platforma local-first: progress, draftlar va Stage 35 glossary override’lari shu browser/device’dagi local state’da turadi. Cloud sync da’vo qilinmaydi. JSON backup IndexedDB audio blob’larini ichiga olmaydi; Speaking yozuvlarini alohida saqlab ol.

## Tekshiruv chegaralari

Stage 35’da JavaScript sintaksisi, JSON ma’lumotlar, dalil tekshiruvlari, Writing/Speaking workflow va glossary saqlash/import/export logikasi Node harness’da tekshirildi. Biroq GitHub Pages hosting, haqiqiy Samsung/Android mikrofon ruxsati, MediaRecorder, IndexedDB audio blob restore va offline/PWA qabul sinovi hali real qurilmada tasdiqlanishi kerak. Chrome headless acceptance sinovi vaqt tugashi sababli yakunlanmadi; bu hisobotda PASS deb ko‘rsatilmaydi.
