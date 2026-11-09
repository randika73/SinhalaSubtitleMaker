# Sinhala Subtitle Maker (Android starter project)

මෙය Android Studio/Gradle project source එකකි. ZIP එක APK එකක් නොවේ; build කරලා APK එක සෑදිය යුතුයි.

## ඇතුළත් කර ඇති දේ
- Android video picker
- Gemini API key එක phone එකේ EncryptedSharedPreferences මඟින් save කිරීම
- Gemini Files API වෙත video upload කිරීම
- Sinhala කතාව Sinhala අකුරින්, English කතාව English වලින් subtitles සෑදීමට prompt කිරීම
- Timestamp සහිත SRT file export කිරීම

## සීමාවන්
- මෙම starter project එක MP4 තුළ subtitles burn කරන්නේ නැහැ; SRT export පමණයි. Burn-in export සඳහා Media3 Transformer overlay implementation එක වෙනම එකතු කර build/test කළ යුතුයි.
- Gemini වෙත video upload වන නිසා internet සහ Gemini API quota/billing limits බලපායි. Offline ක්‍රියා නොකරයි.
- දැනට upload limit එක 100 MB ලෙස සීමා කර ඇත.
- Gemini model ID සහ API availability/limits Google විසින් වෙනස් කළ හැක.
- API key එක app එක තුළ encrypt කර local storage කරයි; නමුත් APK එක reverse-engineer කළ හැකි නිසා embedded/client-side key එක සම්පූර්ණයෙන් රහසිගත නොවේ. පෞද්ගලික භාවිතයට පමණක්; key restrictions සහ quota limits දාන්න.

## Build
- JDK 17
- Android SDK Platform 35
- Gradle 8.9+ / Android Gradle Plugin 8.7.3
- Open in Android Studio and Sync Gradle, then Build > Build APK(s).

## Gemini API
Google AI Studio: https://aistudio.google.com/apikey
Gemini Files API and media input documentation:
https://ai.google.dev/gemini-api/docs/file-input-methods
