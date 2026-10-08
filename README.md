# reem.bi YouTube

אתר סטטי בשני דפים:

- **`index.html`** — דף כניסה מעוצב עם סרטוני YouTube מושתקים שמתחלפים ברקע, וכפתור "כניסה לצפייה".
- **`watch.html`** — דף צפייה שכולו `iframe` של YouTube (המשתמש נשאר באתר, לא עובר ליוטיוב).
  בראש הדף יש סרגל צף שנעלם לבד, עם קישור חזרה ושדה להדבקת קישור YouTube.
  אפשר גם לקשר ישירות: `watch.html?v=VIDEO_ID` או `watch.html?list=PLAYLIST_ID`.

## הגדרות

ב-`assets/config.js`:

- `backgroundVideos` — מזהי הסרטונים שרצים ברקע של דף הכניסה.
- `defaultVideo` — הסרטון שנפתח בדף הצפייה כברירת מחדל.

## הרצה מקומית

```sh
python3 -m http.server 8000
# http://localhost:8000
```

אפשר להעלות כמו שהוא ל-GitHub Pages, Netlify, Cloudflare Pages וכו'.

> הערה: יוטיוב לא מאפשר להטמיע את דף הבית של youtube.com בתוך iframe, רק סרטונים ופלייליסטים (`/embed/...`).
