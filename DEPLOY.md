# העלאת דף הנחיתה של אבינתן אור ל־GitHub Pages (או אירוח HTTPS מהיר)

תיקייה זו (`D:\Documents\hostage_workshop\site\avinatan_or_alternative`) מכילה קובץ `index.html` עצמאי לחלוטין שנועד לשמש **דף נחיתה יחיד וישיר** (ללא דף שער של שלושה חדרים). כל קטעי הווידאו נטענים ישירות מ־Google Drive.

---

## אפשרות א׳ (המומלצת): הפיכה למאגר GitHub עצמאי ודף נחיתה ב־GitHub Pages

כדי שהדף ייפתח ישירות כדף הבית של מאגר חדש ב־GitHub (למשל `https://<username>.github.io/avinatan-or/`):

### דרך 1 — העלאה מהירה דרך הדפדפן (ללא פקודות טרמינל, כדקה)
1. היכנסו ל־[GitHub — Create a new repository](https://github.com/new).
2. תנו שם למאגר (למשל `avinatan-or`), סמנו **Public**, ולחצו **Create repository**.
3. בעמוד שנפתח לחצו על **uploading an existing file**, גררו פנימה את הקובץ `index.html` מתוך התיקייה `avinatan_or_alternative`, ולחצו **Commit changes**.
4. במאגר פתחו **Settings → Pages**, תחת **Build and deployment** בחרו `Deploy from a branch`, סמנו את הענף `main` ואת התיקייה `/(root)`, ולחצו **Save**.
5. תוך כדקה יופיע בראש מסך `Pages` הקישור החי שלכם ב־HTTPS.

### דרך 2 — דרך הטרמינל (Git / GitHub CLI)
*(הערה: תיקיית האב `site` מחוברת כעת למאגר של שלושת החדרים. כדי ליצור מאגר נפרד ועצמאי רק לדף הזה, העתיקו את התיקייה למיקום עצמאי או אתחלו בה מאגר נפרד):*

```powershell
# העתקה לתיקיית מאגר עצמאית נקייה והעלאה ל-GitHub
Copy-Item -Recurse "D:\Documents\hostage_workshop\site\avinatan_or_alternative" "D:\Documents\avinatan_or_landing"
Set-Location "D:\Documents\avinatan_or_landing"
git init -b main
git add index.html DEPLOY.md
git commit -m "Initial landing page for Avinatan Or workshop"
# החליפו בכתובת המאגר החדש שיצרתם ב-GitHub:
git remote add origin https://github.com/<YOUR_USERNAME>/<NEW_REPO_NAME>.git
git push -u origin main
```
לאחר הדחיפה הפעילו **Settings → Pages → Branch: `main` / `(root)` → Save**.

---

## אפשרות ב׳: העלאה של 30 שניות בגרירה (ללא Git)

- **Netlify Drop:** פתחו את [app.netlify.com/drop](https://app.netlify.com/drop), גררו את התיקייה `avinatan_or_alternative` לחלון הדפדפן, וקבלו מיד קישור `https://...netlify.app`.
- **Cloudflare Pages:** בלוח הבקרה פתחו **Workers & Pages → Create application → Pages → Upload assets**, גררו את התיקייה `avinatan_or_alternative` ולחצו **Deploy site**.

---

## בדיקת מוכנות קצרה לפני המפגש בזום

1. פתחו את קישור ה־HTTPS החי ב**חלון גלישה בסתר (Incognito)** במחשב ובטלפון נייד.
2. פתחו כרטיסיית וידאו אחת ובדקו שהנגן מתנגן ללא דרישת התחברות לחשבון Google, ושהכפתור **״פתיחה בחלון חדש (Drive)״** פועל.
3. בדקו את כפתור **״א+ תצוגת קריאה מוגדלת״** בסרגל העליון (נוח מאוד לשיתוף מסך בזום) ואת כפתור **״📋 העתק סיכום לצ׳אט של זום״** בתחתית הדף.
4. בתחילת שיתוף המסך בזום — סמנו **״שתף שמע״ (`Share Sound`)**.
