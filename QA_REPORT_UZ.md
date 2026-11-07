# Stage 35.0 — Yakuniy QA hisoboti

**Release:** 35.0.0  
**Sana:** 7 November 2026  
**Bosqich:** Academic Content & Assessment Excellence

## 1. Stage 35 o‘zgarishlari

| Moduli / qatlam | O‘zgarish |
|---|---|
| Reading Power Lab | Aniq passage quote + reasoning; NOT GIVEN uchun absence rationale |
| Listening Power Lab | Kun MP3’i to‘liq tinglangan bo‘lishi + script bilan mos evidence |
| Writing Power Lab | Task 1 Task Achievement / Task 2 Task Response ajratildi; 4 mezonning har biri uchun alohida evidence |
| Speaking Power Lab | 4 mezon uchun rating/evidence; haqiqiy audio va replay checkbox talab qilinadi |
| Vocabulary | Source-backed local Glossary Curator; JSON export/import; CEFR uchun alohida manba |
| Power Labs hub | Academic content audit ko‘rsatkichlari va rasmiy manba havolalari |

10 ta modul, 100 ta rejim va 4 core studio saqlab qolindi. Yangi mini-o‘yin yoki qo‘shimcha modul qo‘shilmadi.

## 2. Kontent ma’lumotlari — mustaqil qayta hisob

| Audit | Natija |
|---|---:|
| Academic IELTS kunlari | 84 |
| Majburiy Reading/Listening/Writing/Speaking sessiyalari | 336 |
| Reading passage / savollar | 84 / 840 |
| Reading evidence: aniq passage quote | 812 / 840 |
| NOT GIVEN absence cases | 28 |
| Reading invalid answer index / missing explanation | 0 / 0 |
| Listening script / savollar | 84 / 420 |
| Listening evidence: exact script match | 420 / 420 |
| Listening invalid answer index / missing explanation | 0 / 0 |
| Task 2 prompt | 84, barchasi noyob |
| Task 1 visual | 84: 14 tadan 6 tur |
| Speaking Part 1 / Part 2 / Part 3 | 252 / 84 / 252 |
| Vocabulary normalized unique entries | 19,000 / 19,000 |
| To‘liq bundled glossary | 677 |
| 84 kunlik Recall glossary birliklari | 672 |
| Pronunciation-index-only | 4,000 |
| Manual enrichment, English definition yetishmaydi | 14,323 |
| MP3 files | 84 |

Reading passage uzunligi 722–879 so‘z; Listening script uzunligi 446–493 so‘z.

## 3. Writing va Speaking assessment

**Writing:** Task 1 va Task 2 mezon nomlari ajratildi. Task 1’da Task Achievement, Task 2’da Task Response qo‘llanadi. Coherence & Cohesion, Lexical Resource, Grammatical Range & Accuracy ikkalasiga umumiy. Har bir mezon bo‘yicha internal 0–10 rating va alohida matn dalili talab qilinadi. Task 1 uchun 150+, Task 2 uchun 250+ so‘z.

**Speaking:** Fluency & Coherence, Lexical Resource, Grammatical Range & Accuracy, Pronunciation. Har biriga alohida self-rating va dalil talab qilinadi. Saved audio va uni qayta tinglash tasdig‘i shart. Pronunciation transcriptdan taxmin qilinmaydi.

Band 5–9 ko‘rsatkichlari official public IELTS descriptors mazmunidan qisqa parafraza. To‘liq descriptor nusxasi ilovaga ko‘chirilmagan; rasmiy sahifaga link berilgan. Ichki 0–10 qiymatlar IELTS band emas; avtomatik examiner score yo‘q.

## 4. Vocabulary quality disclosure

19,000 noyob indeks — to‘liq glossary degani emas. Strict complete gloss 677; 672 kundalik Recall entry’lari to‘liq. 4,000 CMUdict manbali qo‘shimcha entry faqat US pronunciation index beradi. 14,323 manual-enrichment yozuvida inglizcha ta’rif yetishmaydi. Eski B2/C1 label’lar estimate; sense-level Oxford/English Profile tekshiruvisiz verified CEFR deb ko‘rsatilmaydi.

Stage 35 Glossary Curator foydalanuvchiga Oxford/Cambridge/English Profile manbasidan foydalanib, definition, Uzbek sense, original example, POS, sense note va source URL kiritish imkonini beradi. CEFR manbasi alohida qayd qilinadi. Bu local learner-review; markaziy ekspert tasdig‘i emas.

## 5. Stage 35 logic harness

| Tekshiruv | Natija |
|---|---|
| Stage 35 audit hisoblari | PASS |
| Power Labs panel render string | PASS |
| Writing four-criterion UI | PASS |
| Task 2 Task Response label + anchors | PASS |
| Speaking audio replay review UI | PASS |
| Reading noto‘g‘ri iqtibosni rad etadi | PASS |
| Reading exact quote qabul qilinadi | PASS |
| NOT GIVEN absence rationale qabul qilinadi | PASS |
| Listening noto‘g‘ri evidence’ni rad etadi | PASS |
| Listening exact script phrase qabul qilinadi | PASS |
| Writing 149 so‘zni rad etadi | PASS |
| Writing 150+ so‘z va 4 evidence bilan saqlaydi | PASS |
| Speaking audio + 4 evidence self-review’ni saqlaydi | PASS |
| Source-backed local glossary override | PASS |
| Curated glossary JSON import / export | PASS |
| Curated glossary filtered results display local overrides | PASS |
| CEFR level requires a separate HTTPS source | PASS |
| Invalid CEFR source downgrades to Not assessed | PASS |
| JSON / script syntax | PASS |

**Stage 35 Node logic harness: 21/21 checks passed; including CEFR source gating and curated glossary JSON import/export.**

## 6. Build / asset QA

- Embedded `appData` JSON parse: PASS.
- Main application JS `node --check`: PASS.
- Service Worker `node --check`: PASS.
- `manifest.webmanifest`, `APP_DATA_AUDIT.json`, `AUDIO_MANIFEST.json`: JSON parse PASS.
- MP3 full decode: 84/84 PASS; 84 distinct MD5 hashes.
- Original Task 1 visual renderer audit from Stage 33.2: 84/84; Stage 35 does not modify those data assets.
- PWA cache bumped to Stage 35 shell/audio cache names.

## 7. Ochiq qabul sinovlari

Quyidagilar hali real hosted/browser/device acceptance’ni talab qiladi va bu release hisobotida bajarildi deb ko‘rsatilmaydi:

- GitHub Pages’da haqiqiy published navigation va asset path’lar;
- Samsung/Android microphone permission, MediaRecorder start/stop;
- IndexedDB audio blob reload va alohida audio download;
- PWA install, Service Worker activation va offline reopen;
- real user interaction bilan accessibility, keyboard navigation va touch target tekshiruvi.

Chromium headless sinovi katta embedded HTML yuklanishida time-out bo‘ldi. Shuning uchun real browser acceptance holati **OPEN**, PASS emas.

## 8. Yakuniy qaror

**Stage 35.0: STATIC / DATA / LOGIC / AUDIO ASSET QA — PASS.**  
**Hosted browser / Android / offline acceptance — OPEN.**

Mazkur release Stage 34 real qurilma tekshiruviga tayyor; uning natijalari Stage 36 uchun asos bo‘lishi kerak.
