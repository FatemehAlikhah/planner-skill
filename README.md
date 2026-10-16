# Planner Skill for Claude

**Life OS for Claude: capacity-aware planning, expected outcomes you can check, and scheduling that actually gets done. Persian (Jalali) and English.**

اسکیل برنامه‌ریزی برای Claude: از سال تا روز، با دستاوردهای قابل‌سنجش و یادآوری خودکار. پشتیبانی از تقویم شمسی.

[English](#english) · [فارسی](#فارسی)

Version 1.0.0 · License: MIT · Repo: https://github.com/FatemehAlikhah/planner-skill

---

## English

### What it does

Planner turns vision into daily execution. Every plan lives in a hierarchy (Year → Season → Month → Week → Day), and every layer inherits context from the one above. It plans for realistic capacity, not the ideal self, and stays non-judgmental: rescheduling is normal, never a failure.

What makes it different:

- **Starts with two short questions.** Where should the plan come from (Claude's data, your own input, or both), and which timeframe (week, month or season).
- **Every plan ends with Expected Outcomes.** A headline result, a small table (what changes, why it matters, how you will know), and an honest core vs. stretch split.
- **Readable layout.** Priorities as a numbered list with a reason, tables for distribution and risks, capacity shown as a simple ratio, one concrete first step.
- **Offers to schedule it.** After the plan, it asks whether to schedule and remind you. If you say yes, it asks how (reminders, calendar time blocks, both, or only part of the plan), shows a proposed schedule and creates it only after your clear yes.
- **Persian and English.** Jalali dates and week boundaries (Saturday to Friday), RTL-friendly tables.

It also covers goals, projects, tasks, habits, reviews, a light finance layer and content planning.

### Install

**Claude.ai** (Free, Pro, Max, Team, Enterprise)

1. Download `dist/planner.skill` from this repo (or zip the `planner/` folder yourself).
2. Open Customize > Skills and upload the file.
3. Start a chat and say "plan my week" or «برنامه‌ریزی کن».

**Claude Code**

```bash
git clone https://github.com/FatemehAlikhah/planner-skill.git
cp -r planner-skill/planner ~/.claude/skills/planner
```

Updates do not arrive automatically. Pull the repo and copy the folder again (or re-upload the file) when a new version is released.

### Example

> **You:** plan my week
> **Planner:** Where should the plan come from? Which timeframe?
> **You:** my own input, week. Project: build a verify agent. Class on Sunday 7 to 9 pm.
> **Planner:** a week at a glance with the headline outcome, priorities, a day-by-day table, risks, Expected Outcomes, and an offer to schedule it.

### Repository layout

```
planner-skill/
├── README.md
├── LICENSE
├── dist/planner.skill          ready-to-upload package
└── planner/
    ├── SKILL.md                workflow, capacity rules, scheduling
    └── references/
        └── presentation.md     outcomes, lists and layout guide
```

### Customize

Edit `planner/SKILL.md` for behavior and `planner/references/presentation.md` for how plans look. Keep `SKILL.md` lean and put detail in `references/`.

### License

MIT. See [LICENSE](LICENSE).

---

## فارسی

### چه کار می‌کند

Planner چشم‌انداز را به اجرای روزانه تبدیل می‌کند. هر برنامه در یک سلسله‌مراتب است (سال ← فصل ← ماه ← هفته ← روز) و هر سطح از سطح بالاترش زمینه می‌گیرد. بر اساس ظرفیت واقعی برنامه می‌چیند، نه نسخه‌ی ایده‌آل آدم، و قضاوت‌گر نیست: جابه‌جایی برنامه عادی است و شکست حساب نمی‌شود.

تفاوت‌ها:

- **با دو سؤال کوتاه شروع می‌کند.** برنامه از روی چه چیزی ساخته شود (داده‌های Claude، ورودی خودت یا هر دو) و برای چه بازه‌ای (هفته، ماه یا فصل).
- **هر برنامه با «دستاوردهای مورد انتظار» تمام می‌شود.** یک جمله‌ی تیتر، یک جدول کوچک (چه چیزی تغییر می‌کند، چرا مهم است، از کجا می‌فهمی) و تفکیک صادقانه‌ی اصلی و اضافه.
- **چیدمان خوانا.** اولویت‌ها به‌صورت لیست شماره‌دار با دلیل، جدول برای توزیع و ریسک‌ها، ظرفیت به‌صورت نسبت ساده و یک قدم اول مشخص.
- **پیشنهاد زمان‌بندی.** بعد از برنامه می‌پرسد زمان‌بندی و یادآوری بگذارد یا نه. اگر بله، می‌پرسد چطور (یادآوری، بلاک تقویم، هر دو یا فقط بخشی از برنامه)، پیشنهادش را نشان می‌دهد و فقط بعد از تأیید صریح تو می‌سازد.
- **فارسی و انگلیسی.** تاریخ و مرز هفته‌ی شمسی (شنبه تا جمعه) و جدول‌های مناسب راست‌به‌چپ.

اهداف، پروژه‌ها، تسک‌ها، عادت‌ها، مرورها، لایه‌ی سبک مالی و برنامه‌ریزی محتوا را هم پوشش می‌دهد.

### نصب

**در Claude.ai** (Free، Pro، Max، Team، Enterprise)

۱. فایل `dist/planner.skill` را از همین ریپو دانلود کن (یا پوشه‌ی `planner/` را خودت zip کن).
۲. به Customize > Skills برو و فایل را آپلود کن.
۳. در یک گفت‌وگو بنویس «برنامه‌ریزی کن» یا "plan my week".

**در Claude Code**

```bash
git clone https://github.com/FatemehAlikhah/planner-skill.git
cp -r planner-skill/planner ~/.claude/skills/planner
```

آپدیت‌ها خودکار نمی‌رسند. وقتی نسخه‌ی جدید آمد، ریپو را pull کن و پوشه را دوباره کپی کن (یا فایل را دوباره آپلود کن).

### مثال

> **تو:** برنامه‌ریزی کن
> **Planner:** برنامه از روی چه چیزی ساخته شود؟ کدام بازه؟
> **تو:** خودم وارد می‌کنم، هفته. پروژه: ساخت ایجنت وریفای. کلاس یکشنبه ۷ تا ۹ عصر.
> **Planner:** هفته در یک نگاه با دستاورد اصلی، اولویت‌ها، جدول روزبه‌روز، ریسک‌ها، دستاوردهای مورد انتظار و پیشنهاد زمان‌بندی.

### شخصی‌سازی

برای تغییر رفتار، `planner/SKILL.md` و برای ظاهر برنامه‌ها `planner/references/presentation.md` را ویرایش کن. فایل `SKILL.md` را کوتاه نگه دار و جزئیات را در `references/` بگذار.

### لایسنس

MIT. فایل [LICENSE](LICENSE) را ببین.
