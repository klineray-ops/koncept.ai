# Koncept AI - Premium eBook Studio (Fast Build)

Concept to Publish, KDP, BrOwn, eBookSelf...

## Deploy in 3 minutes
1. Upload this folder to GitHub (or drag to Streamlit Cloud)
2. Main file: `app.py`
3. Requirements auto-installed from `requirements.txt`
4. Streamlit Cloud -> App settings -> Secrets -> paste contents of `.streamlit/secrets.toml.example` with your real values

## Features
- ⚡ Fast boot (lazy imports, cached clients)
- 🔐 Login/Register + 👑 Admin panel (unlimited, user management)
- 💳 Tiers: Free $0 / Pro Std $9 / Pro Dlx $19 / Pro Max $39
- ✍️ Groq AI writer, 📦 PDF/DOCX export (KDP-ready)
- Supabase persistence (optional, falls back to session)

## Supabase table
```sql
create table users (
  email text primary key,
  name text,
  pw_hash text,
  tier text default 'Free',
  books_used int default 0,
  created_at timestamp default now()
);
```
