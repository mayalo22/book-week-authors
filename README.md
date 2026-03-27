# מערכת רישום סופרות לשבוע הספר

פרויקט React + Vite שמוכן להעלאה ל-Netlify.

## מה צריך לפני העלאה

1. לפתוח פרויקט ב-Supabase
2. להריץ את הקובץ `supabase-authors-table.sql` בתוך SQL Editor
3. לקחת מ-Supabase את:
   - Project URL
   - anon public key
4. להגדיר ב-Netlify את משתני הסביבה:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
   - `VITE_ADMIN_PASSWORD`

## התקנה מקומית

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

## העלאה ל-Netlify

### אפשרות 1: דרך GitHub
- מעלים את כל הקבצים ל-repository ב-GitHub
- ב-Netlify בוחרים Add new site -> Import from Git
- בוחרים את הפרויקט
- Build command: `npm run build`
- Publish directory: `dist`
- מגדירים את משתני הסביבה
- Deploy

### אפשרות 2: העלאה ידנית
- מתקינים מקומית: `npm install`
- מריצים build: `npm run build`
- מעלים את תיקיית `dist` ל-Netlify

## הערה חשובה

מסך המנהלים מוגן בסיסמה בצד הלקוח דרך `VITE_ADMIN_PASSWORD`.
אם בעתיד תרצי אבטחה אמיתית יותר, כדאי להוסיף התחברות משתמשים ב-Supabase Auth.
