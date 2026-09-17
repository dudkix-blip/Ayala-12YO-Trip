# האתר החי – טיול בת המצווה של איילה

הקבצים מוכנים ל-Firebase Hosting + Cloud Firestore.

## הגדרה חד-פעמית
1. היכנס ל-Firebase Console וצור Project חדש.
2. הוסף Web App (סמל </>) והעתק את `firebaseConfig`.
3. פתח `public/index.html` והחלף את הערכים `PASTE_...` בפרטי ה-config שקיבלת.
4. ב-Firebase Console:
   - Build > Firestore Database > Create database.
   - Authentication > Sign-in method > Anonymous > Enable.
5. התקן Firebase CLI:
   `npm install -g firebase-tools`
6. מתוך תיקיית הפרויקט:
   `firebase login`
   `firebase use --add`
7. פרוס גם את האתר וגם את כללי האבטחה:
   `firebase deploy --only hosting,firestore:rules`

בסיום תקבל כתובת בסגנון:
`https://PROJECT_ID.web.app`

## מה קורה באתר
- כל מי שפותח את הקישור נכנס אנונימית.
- סימון Checkbox נכתב ל-Cloud Firestore.
- כל המכשירים הפתוחים מתעדכנים בזמן אמת.
- מד ההתקדמות משותף לכולם.
- כפתור "איפוס סימונים" מאפס לכולם.

## אבטחה
הכללים המצורפים מאפשרים קריאה/כתיבה רק למשתמש שעבר Anonymous Authentication.
כל מי שמקבל את קישור האתר יכול בפועל להיכנס אנונימית ולערוך את הצ'ק-ליסט, ולכן שתף את הקישור רק עם מי שאתה רוצה שיערוך.
