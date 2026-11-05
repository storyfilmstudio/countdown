COUNTDOWN STUDIO — සම්පූර්ණ සිංහල උපදෙස්
================================================

මෙය HTML, CSS සහ JavaScript භාවිතයෙන් Browser එක තුළම Countdown Video නිර්මාණය කරන වෙබ් යෙදුමකි. Countdown එක සැකසීම සහ වීඩියෝව Render කිරීම ඔබගේ Browser එක තුළ සිදු වේ. වීඩියෝවක් සෑදීමට වෙනම AI සේවාවක් හෝ Backend Server එකක් අවශ්‍ය නොවේ.

1. ZIP එක Extract කළ පසු ලැබෙන Folder ව්‍යුහය
------------------------------------------------

countdown-studio/
├── index.html
├── favicon.svg
├── README.md
├── README_SI.txt
├── css/
│   └── style.css
└── js/
    └── app.js

වැදගත්: index.html, css සහ js ගොනු වෙන වෙනම තැන්වලට දමන්න එපා. ඉහත Folder ව්‍යුහය ඒ ආකාරයෙන්ම තබාගන්න.

2. පරිගණකයේ Run කිරීම
----------------------

1. countdown-studio ZIP එක Extract කරන්න.
2. Extract කළ countdown-studio Folder එක විවෘත කරන්න.
3. එම Folder එක තුළ Terminal හෝ Command Prompt එකක් විවෘත කරන්න.
4. Python තිබේ නම් පහත Command එක Run කරන්න:

   python -m http.server 8080

5. Browser එකෙන් http://localhost:8080 වෙත යන්න.

Node.js තිබේ නම් `npx serve .` යන Command එකත් භාවිත කළ හැක.

index.html එක Double-click කිරීමෙන් UI එක පෙන්විය හැකි වුවත්, `file://` ක්‍රමයේදී Browser එක අනුව Video Recording සහ Audio පහසුකම් සීමා විය හැක. ඒ නිසා localhost හෝ HTTPS භාවිත කිරීම වඩාත් සුදුසුය.

3. GitHub Pages වෙත Upload කිරීම
--------------------------------

1. GitHub හි අලුත් Repository එකක් සාදන්න.
2. countdown-studio Folder එකේ ඇතුළත තිබෙන සියලුම ගොනු සහ Folders Repository එකේ Root එකට Upload කරන්න.
3. `css` සහ `js` Folders නම් වෙනස් නොකර තබාගන්න.
4. Repository එකේ Settings → Pages වෙත යන්න.
5. Build and deployment යටතේ Deploy from a branch තෝරන්න.
6. Branch ලෙස `main` සහ Folder ලෙස `/ (root)` තෝරා Save කරන්න.
7. GitHub Pages URL එක ලබාගත් පසු එය Browser එකෙන් විවෘත කරන්න.

මෙම Project එකේ CSS සහ JavaScript paths relative ලෙස සකසා ඇත. ඒ නිසා GitHub Pages project URL එකක් යටතේද නිවැරදිව load විය යුතුය.

4. Countdown Video එකක් සාදාගැනීම
----------------------------------

1. Starting Countdown Time එකට `MM:SS` හෝ `HH:MM:SS` ආකෘතියෙන් කාලය දෙන්න. උදා: `03:00`, `01:00:00`.
2. Real-Time (1:1) හෝ Compressed / Custom Duration තෝරන්න.
3. කැමති Visual Template එකක් තෝරන්න.
4. Background Color එක තෝරන්න. Green Screen සඳහා `#00FF00` භාවිත කරන්න.
5. Font, Size, Frame, Glow සහ Position සැකසීම් වෙනස් කරන්න.
6. Sound Effects On/Off කර Sound Style සහ Volume තෝරන්න.
7. Resolution සහ FPS තෝරන්න.
8. Generate Countdown Video බොත්තම ඔබන්න.
9. Render එක අවසන් වූ පසු Video Player එකෙන් බලලා Download Video තෝරන්න.

5. Modes
--------

Real-Time (1:1):
Countdown එකේ කාලය හා Video එකේ කාලය එක සමාන වේ. උදාහරණයක් ලෙස මිනිත්තු 3ක Countdown එකක් මිනිත්තු 3ක Video එකක් ලෙස සාදයි.

Compressed / Custom:
දිගු Countdown එකක් තෝරාගත් කෙටි Video කාලයකට සකස් කරයි. උදාහරණයක් ලෙස මිනිත්තු 3ක Countdown එක තත්පර 10ක Video එකක් ලෙස නිර්මාණය කළ හැක.

6. Sound Effects
----------------

- Classic Clock Tick
- Digital Beep
- Soft Click
- Cinematic Pulse
- Final Countdown Beep
- Silent

Sound එක Browser එකේ Web Audio API හරහා නිර්මාණය වේ. Sound playback සඳහා Browser එක මුලින්ම User interaction එකක් ඉල්ලා සිටිය හැක.

7. Resolution
-------------

- 1920 × 1080 — Full HD Landscape (16:9)
- 1280 × 720 — HD Landscape (16:9)
- 1080 × 1920 — Vertical (9:16), Shorts / Reels
- 1080 × 1080 — Square (1:1)

Mobile දුරකථනයක Export කරන විට 1920×1080 හෝ 1080×1920 සහ 60 FPS නිසා Memory/CPU භාවිතය වැඩි විය හැක. එවැනි අවස්ථාවක 1280×720 සහ 30 FPS භාවිත කර බලන්න.

8. Video Format ගැන වැදගත් කරුණු
---------------------------------

Browser එක සහ Device එක අනුව MP4 හෝ WebM Format එකක් ලබාදේ. Export අවසන් වූ විට සැබෑ File Extension එක UI එකේ පෙන්වයි. සියලුම Browser වල MP4 export සහතික කළ නොහැක.

Canvas captureStream සහ MediaRecorder සහාය ඇති නවීන Chrome, Edge හෝ Firefox Browser එකක් භාවිත කරන්න. HTTPS හෝ localhost හරහා වෙබ් අඩවිය විවෘත කිරීම වඩාත් සුදුසුය.

9. Source ZIP Download
----------------------

Website එකේ ඉහළ ඇති `Download Source Code (.ZIP)` බොත්තමෙන් සම්පූර්ණ Project Source එක ZIP ලෙස ලබාගත හැක. ZIP එක සෑදීමට app එක ඇතුළතම ඇති කුඩා ZIP writer එක භාවිත කරන බැවින් වෙනම JSZip CDN එකක් අවශ්‍ය නොවේ.

10. Privacy
-----------

Countdown එක සැකසීම සහ Video Rendering Browser එක තුළ සිදු වේ. මෙම Project එකට Backend එකක් නොමැති අතර ඔබ සාදන Video එක Server එකකට Upload නොකරයි. අන්තර්ජාලය තිබේ නම් Google Fonts වෙතින් අකුරු Load විය හැක; එසේ නොමැති විට Browser එකේ තිබෙන default fonts භාවිත වේ.
