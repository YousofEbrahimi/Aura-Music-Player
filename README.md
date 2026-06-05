<div align="center">

<img src="https://img.shields.io/badge/Version-2.0.0-a78bfa?style=for-the-badge" alt="Version">
<img src="https://img.shields.io/badge/Status-Live-22c55e?style=for-the-badge" alt="Status">

<br><br>

# Aura Music Player

### A sleek, modern music player built entirely with vanilla web technologies.

### یک موزیک پلیر مدرن و زیبا ساخته شده با تکنولوژی‌های خالص وب

<br>

[![Live Demo](https://img.shields.io/badge/Live_Demo-a78bfa?style=for-the-badge&logo=github&logoColor=white)](https://yousofebrahimi.github.io/Aura-Music-Player/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)]()
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)]()

<br>

<img src="https://img.shields.io/badge/%F0%9F%87%AA%F0%9F%87%B8_English-blue?style=flat-square" alt="English"> &nbsp;
<img src="https://img.shields.io/badge/%F0%9F%87%AE%F0%9F%87%B7_%D9%81%D8%A7%D8%B1%D8%B3%DB%8C-green?style=flat-square" alt="فارسی">

<br><br>

---

</div>

<br>

## Table of Contents | فهرست مطالب

<br>

| # | English | فارسی |
|---|---------|-------|
| 1 | [Features](#-features) | [ویژگی‌ها](#-ویژگی‌ها) |
| 2 | [Live Demo](#-live-demo) | [دموی زنده](#-دموی-زنده) |
| 3 | [Keyboard Shortcuts](#️-keyboard-shortcuts) | [شورتکات‌ها](#️-شورتکات‌های-کیبورد) |
| 4 | [Tech Stack](#️-tech-stack) | [تکنولوژی‌ها](#️-تکنولوژی‌ها) |
| 5 | [Project Structure](#-project-structure) | [ساختار پروژه](#-ساختار-پروژه) |
| 6 | [Getting Started](#-getting-started) | [شروع کار](#-شروع-کار) |
| 7 | [How It Works](#️-how-it-works) | [چطور کار می‌کنه](#️-چطور-کار-می‌کنه) |
| 8 | [Contributing](#-contributing) | [مشارکت](#-مشارکت) |
| 9 | [License](#-license) | [لایسنس](#-لایسنس) |

<br>

---

<br>

## 🇬🇧 English

<br>

### ✨ Features

<br>

- **Real-time Audio Visualizer** — Frequency bars rendered on Canvas using Web Audio API
- **Spinning Vinyl Animation** — Classic vinyl record that rotates while music plays
- **Drag & Drop Support** — Drop your MP3, WAV, OGG, or FLAC files directly into the player
- **4 Built-in Demo Tracks** — Procedurally generated with Web Audio API, zero external files
- **Shuffle & Repeat** — Shuffle mode and repeat (all tracks / single track)
- **Smart Volume Control** — Mute toggle with adaptive icon that changes with volume level
- **Keyboard Shortcuts** — Full control without touching the mouse
- **Dynamic Album Art** — Generated gradient artwork for each track
- **Ambient Background** — Blurred album art backdrop that shifts per track
- **Responsive Design** — Optimized for desktop and mobile screens
- **Dark Glassmorphism UI** — Modern frosted-glass aesthetic with grain texture overlay

<br>

### 🌐 Live Demo

<br>

**[▶ Listen Now](https://yousofebrahimi.github.io/Aura-Music-Player/)**

<br>

### ⌨️ Keyboard Shortcuts

<br>

| Key | Action |
|-----|--------|
| `Space` | Play / Pause |
| `←` | Seek backward 5 seconds |
| `→` | Seek forward 5 seconds |
| `↑` | Volume up |
| `↓` | Volume down |
| `N` | Next track |
| `P` | Previous track |

<br>

### 🛠️ Tech Stack

<br>

| Technology | Purpose |
|------------|---------|
| HTML5 | Page structure and semantics |
| CSS3 | Styling, animations, glassmorphism effects |
| JavaScript (ES6+) | Player logic, state management, audio engine |
| Web Audio API | Demo track synthesis and real-time frequency analysis |
| Canvas API | Audio visualizer rendering |
| Google Fonts | Syne (display) + DM Mono (monospace) |

<br>

> **No frameworks. No libraries. No build tools. Pure vanilla.**

<br>

### 📁 Project Structure

<br>

```
Aura-Music-Player/
│
├── index.html        # Complete application (HTML + CSS + JS)
├── README.md         # Project documentation (EN + FA)
└── LICENSE           # MIT License
```

<br>

### 🚀 Getting Started

<br>

#### Option 1: Live Version (Recommended)

Visit **[the live demo](https://yousofebrahimi.github.io/Aura-Music-Player/)** — ready to play immediately.

#### Option 2: Run Locally

```bash
# 1. Clone the repository
git clone https://github.com/YousofEbrahimi/Aura-Music-Player.git

# 2. Navigate to the project
cd Aura-Music-Player

# 3. Open in your browser
# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

#### Option 3: Add Your Own Music

1. Open the application
2. Click **+ Add Files** button in the playlist panel
3. Or simply **drag and drop** audio files anywhere on the page
4. Supported formats: **MP3, WAV, OGG, FLAC, AAC**

<br>

### ⚙️ How It Works

<br>

#### Demo Track Generation

The 4 built-in demo tracks are generated entirely in the browser using the **Web Audio API**:

- Each track uses different oscillator types: `sine`, `triangle`, `sawtooth`
- Chord progressions and bass lines are scheduled using `OfflineAudioContext`
- Arpeggiated melodies are layered on top of the harmonic foundation
- The rendered audio buffer is converted to WAV format and served as a blob URL
- No network requests — everything is synthesized in real-time

#### Audio Visualizer

- An `AnalyserNode` extracts frequency data from the audio stream in real-time
- Data is rendered as gradient bars on a `<canvas>` element
- Colors shift from deep purple to warm gold for an immersive aesthetic

#### Vinyl Record Animation

- A CSS `conic-gradient` creates the realistic vinyl disc texture
- `repeating-radial-gradient` adds authentic groove lines
- Slides out and rotates when playback begins
- Slides back and pauses when music stops

#### Ambient Background

- The current track's color palette is applied as a full-screen gradient
- CSS `filter: blur()` creates a soft, atmospheric backdrop
- Smooth transitions between tracks

<br>

### 🤝 Contributing

<br>

Contributions are welcome and appreciated!

1. **Fork** the repository
2. **Create** your feature branch

   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Commit** your changes

   ```bash
   git commit -m 'Add amazing feature'
   ```

4. **Push** to the branch

   ```bash
   git push origin feature/amazing-feature
   ```

5. **Open** a Pull Request

<br>

### 📄 License

<br>

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

<br>

---

<br>

## 🇮🇷 فارسی

<br>

### ✨ ویژگی‌ها

<br>

- **ویژوالایزر صوتی زنده** — نمایش فرکانس‌ها روی Canvas با Web Audio API
- **انیمیشن وینیل چرخان** — صفحه گرامافون کلاسیک که هنگام پخش موسیقی می‌چرخد
- **پشتیبانی از Drag & Drop** — فایل‌های MP3، WAV، OGG یا FLAC رو مستقیم بنداز تو پلیر
- **۴ ترک دمو داخلی** — ساخته شده با Web Audio API، بدون هیچ فایل خارجی
- **Shuffle و Repeat** — حالت شافل و تکرار (همه ترک‌ها / تک ترک)
- **کنترل ولوم هوشمند** — قطع صدا با آیکون تطبیقی که با سطح صدا تغییر می‌کنه
- **شورتکات‌های کیبورد** — کنترل کامل بدون نیاز به موس
- **آرت پویا** — گرادیانت هنری تولید شده برای هر ترک
- **بکگراند محیطی** — پس‌زمینه بلور شده از آرت آلبوم که با هر ترک عوض میشه
- **طراحی ریسپانسیو** — بهینه‌شده برای دسکتاپ و موبایل
- **رابط کاربری Glassmorphism تاریک** — زیبایی شیشه‌ای مدرن با بافت دانه‌دانه

<br>

### 🌐 دموی زنده

<br>

**[▶ همین الان گوش بده](https://yousofebrahimi.github.io/Aura-Music-Player/)**

<br>

### ⌨️ شورتکات‌های کیبورد

<br>

| کلید | عملکرد |
|------|--------|
| `Space` | پخش / توقف |
| `←` | عقب رفتن ۵ ثانیه |
| `→` | جلو رفتن ۵ ثانیه |
| `↑` | زیاد کردن صدا |
| `↓` | کم کردن صدا |
| `N` | ترک بعدی |
| `P` | ترک قبلی |

<br>

### 🛠️ تکنولوژی‌ها

<br>

| تکنولوژی | کاربرد |
|----------|--------|
| HTML5 | ساختار صفحه |
| CSS3 | استایل، انیمیشن، افکت‌های شیشه‌ای |
| JavaScript (ES6+) | منطق پلیر، مدیریت state، موتور صوتی |
| Web Audio API | ساخت ترک‌های دمو و تحلیل فرکانس بلادرنگ |
| Canvas API | رندر ویژوالایزر صوتی |
| Google Fonts | فونت‌های Syne و DM Mono |

<br>

> **بدون فریمورک. بدون کتابخانه. بدون ابزار بیلد. کاملاً خالص.**

<br>

### 📁 ساختار پروژه

<br>

```
Aura-Music-Player/
│
├── index.html        # کل برنامه (HTML + CSS + JS)
├── README.md         # مستندات پروژه (انگلیسی + فارسی)
└── LICENSE           # لایسنس MIT
```

<br>

### 🚀 شروع کار

<br>

#### روش ۱: نسخه آنلاین (پیشنهادی)

به **[دموی زنده](https://yousofebrahimi.github.io/Aura-Music-Player/)** سر بزنید — آماده پخش.

#### روش ۲: اجرای محلی

```bash
# ۱. کلون کردن ریپازیتوری
git clone https://github.com/YousofEbrahimi/Aura-Music-Player.git

# ۲. رفتن به پوشه پروژه
cd Aura-Music-Player

# ۳. باز کردن در مرورگر
# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

#### روش ۳: اضافه کردن موسیقی خودتان

1. برنامه رو باز کنید
2. دکمه **+ Add Files** رو در پنل پلی‌لیست بزنید
3. یا فایل‌های صوتی رو مستقیم **درگ و دراپ** کنید روی صفحه
4. فرمت‌های پشتیبانی‌شده: **MP3، WAV، OGG، FLAC، AAC**

<br>

### ⚙️ چطور کار می‌کنه

<br>

#### ساخت ترک‌های دمو

ترک‌های دمو کاملاً داخل مرورگر و با **Web Audio API** ساخته میشن:

- هر ترک از نوع اسیلاتور متفاوتی استفاده می‌کنه: `sine`، `triangle`، `sawtooth`
- آکوردها و خطوط بیس با `OfflineAudioContext` زمان‌بندی میشن
- ملودی آرپجیو روی پایه هارمونیک لایه‌بندی میشه
- بافر صوتی رندر شده به فرمت WAV تبدیل و به صورت Blob URL ارائه میشه
- هیچ درخواست شبکه‌ای ارسال نمیشه — همه چیز بلادرنگ ساخته میشه

#### ویژوالایزر صوتی

- یک `AnalyserNode` داده‌های فرکانس رو بلادرنگ از جریان صوتی استخراج می‌کنه
- داده‌ها به صورت میله‌های گرادیانت روی عنصر `<canvas>` رندر میشن
- رنگ‌ها از بنفش تیره به طلایی گرم تغییر می‌کنن

#### انیمیشن وینیل

- `conic-gradient` در CSS بافت واقعی صفحه وینیل رو می‌سازه
- `repeating-radial-gradient` خطوط شیار رو اضافه می‌کنه
- وینیل هنگام پخش بیرون میاد و شروع به چرخیدن می‌کنه
- هنگام توقف، برمی‌گرده و چرخش متوقف میشه

#### بکگراند محیطی

- پالت رنگی ترک فعلی استخراج و به صورت گرادیانت تمام‌صفحه اعمال میشه
- `filter: blur()` در CSS یک پس‌زمینه نرم و جذاب می‌سازه
- انتقال نرم بین ترک‌ها با CSS Transitions

<br>

### 🤝 مشارکت

<br>

مشارکت‌ها با آغوش باز پذیرفته میشن!

1. **فورک** کردن ریپازیتوری
2. **ساختن** شاخه ویژگی جدید

   ```bash
   git checkout -b feature/ویژگی-جدید
   ```

3. **کامیت** کردن تغییرات

   ```bash
   git commit -m 'اضافه کردن ویژگی جدید'
   ```

4. **پوش** کردن به شاخه

   ```bash
   git push origin feature/ویژگی-جدید
   ```

5. **باز کردن** یک Pull Request

<br>

### 📄 لایسنس

<br>

این پروژه تحت **لایسنس MIT** منتشر شده — برای جزئیات کامل فایل [LICENSE](LICENSE) رو ببینید.

<br>

---

<br>

<div align="center">

### Built with passion | ساخته شده با عشق

**[Yousof Ebrahimi](https://github.com/YousofEbrahimi)**

<br>

If you like this project, give it a ⭐

اگه این پروژه رو دوست داشتی، بهش ستاره بده ⭐

</div>
