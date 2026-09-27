# סוכן תמונות לבירה C'skazza (Hermes Agent)

Skill ל-Hermes שמייצר תמונות לבירה דרך טלגרם.

## התקנה
```bash
cp -r hermes/skills/cskazza-beer-images ~/.hermes/skills/
```
דרוש מפתח ליצירת תמונות (כלי `image_generate` של Hermes, FAL):
```bash
echo "FAL_KEY=your_key" >> ~/.hermes/.env
hermes gateway restart
```

## שימוש בטלגרם
- `/cskazza-beer-images פוסט לאינסטגרם של IPA על חוף הים`
- או פשוט: "תעשה לי תמונה לסטורי של הבירה החדשה"

## אופציונלי: סוכן נפרד (פרופיל)
```bash
hermes profile create beer-images
cp -r hermes/skills/cskazza-beer-images ~/.hermes/profiles/beer-images/skills/
```
וחבר לו בוט טלגרם נפרד (`TELEGRAM_BOT_TOKEN` ב-`.env` של הפרופיל).
