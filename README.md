# 🤖 WebMaster Bot - أفضل بوت تنزيل المواقع في تيليجرام

<div align="center">

![WebMaster Bot](https://img.shields.io/badge/WebMaster-Bot-blue?style=for-the-badge&logo=telegram)
![Python](https://img.shields.io/badge/Python-3.8+-green?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**بوت تيليجرام متقدم لتنزيل المواقع الكاملة مع دعم JavaScript الكامل**

[🚀 البدء السريع](#-البدء-السريع) • [📋 المميزات](#-المميزات) • [⚙️ التثبيت](#️-التثبيت) • [📖 الاستخدام](#-الاستخدام) • [🤝 المساهمة](#-المساهمة)

</div>

---

## 🌟 المميزات الرئيسية

### 🚀 **تنزيل متقدم**
- ✅ تنزيل مواقع كاملة مع جميع الملفات (HTML, CSS, JS, صور)
- ✅ دعم كامل للمواقع التفاعلية والجافاسكريبت
- ✅ تنزيل متوازي فائق السرعة
- ✅ حفظ التصميم الأصلي 100%

### 🎯 **سهولة الاستخدام**
- ✅ واجهة عربية بالكامل
- ✅ أوامر بسيطة وواضحة
- ✅ ضغط تلقائي في ملفات ZIP
- ✅ معاينة قبل التنزيل

### 📊 **إدارة ذكية**
- ✅ حفظ تاريخ جميع التنزيلات
- ✅ إحصائيات مفصلة للاستخدام
- ✅ نظام حدود ذكي للمستخدمين
- ✅ لوحة إدارة متقدمة للمشرفين

### 🔒 **أمان وموثوقية**
- ✅ تنظيف تلقائي للملفات المؤقتة
- ✅ حماية من التحميل الزائد
- ✅ نظام سجلات شامل
- ✅ معالجة أخطاء متقدمة

---

## 🛠️ التقنيات المستخدمة

| التقنية | الإصدار | الوصف |
|---------|---------|--------|
| **Python** | 3.8+ | لغة البرمجة الأساسية |
| **python-telegram-bot** | 20.7 | مكتبة بوت تيليجرام |
| **Playwright** | 1.40.0 | محرك المتصفح للجافاسكريبت |
| **SQLAlchemy** | 2.0.23 | قاعدة البيانات |
| **aiohttp** | 3.9.1 | طلبات HTTP غير متزامنة |
| **BeautifulSoup** | 4.12.2 | تحليل HTML |

---

## ⚙️ التثبيت والإعداد

### 📋 المتطلبات الأساسية

```bash
# تأكد من وجود Python 3.8 أو أحدث
python --version

# تأكد من وجود pip
pip --version
```

### 🔧 خطوات التثبيت

1. **استنساخ المشروع**
```bash
git clone https://github.com/yourusername/web-bot-main.git
cd web-bot-main
```

2. **إنشاء بيئة افتراضية**
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# أو
venv\Scripts\activate     # Windows
```

3. **تثبيت المتطلبات**
```bash
pip install -r requirements.txt
```

4. **إعداد متغيرات البيئة**
```bash
cp .env.example .env
nano .env  # أو أي محرر نصوص
```

5. **تعديل ملف .env**
```env
# إعدادات البوت الأساسية
BOT_TOKEN=your_bot_token_here
ADMIN_ID=your_telegram_id_here

# إعدادات التنزيل
MAX_CONCURRENT_DOWNLOADS=3
MAX_FILE_SIZE=52428800
DOWNLOAD_TIMEOUT=300

# إعدادات قاعدة البيانات
DATABASE_URL=sqlite:///data/database.db

# إعدادات الأمان
RATE_LIMIT_PER_HOUR=10
MAX_WEBSITE_SIZE=104857600
```

### 🚀 تشغيل البوت

```bash
python main.py
```

---

## 📖 دليل الاستخدام

### 👤 للمستخدمين العاديين

#### 🌐 تنزيل موقع
1. ابدأ محادثة مع البوت: `/start`
2. أرسل رابط الموقع المراد تنزيله
3. انتظر حتى انتهاء المعالجة
4. احصل على ملف ZIP يحتوي على الموقع كاملاً

#### 📊 عرض الإحصائيات
```
/stats - عرض إحصائياتك الشخصية
/history - تاريخ التنزيلات السابقة
/settings - إعدادات التنزيل
```

### 👑 للمشرفين

#### 🔧 لوحة الإدارة
```
/admin - الوصول للوحة الإدارة
/broadcast - إرسال رسالة جماعية
/cleanup - تنظيف فوري للنظام
```

#### 📊 إحصائيات النظام
- عدد المستخدمين الكلي
- التنزيلات الناجحة والفاشلة
- استهلاك التخزين
- حالة النظام

---

## 🏗️ هيكل المشروع

```
web-bot-main/
├── 📁 bot/                    # معالجات البوت
│   ├── handlers.py           # معالجات الرسائل
│   ├── keyboards.py          # لوحات المفاتيح
│   └── __init__.py
├── 📁 services/              # الخدمات الأساسية
│   ├── downloader.py         # محرك التنزيل
│   ├── file_manager.py       # إدارة الملفات
│   └── __init__.py
├── 📁 utils/                 # الأدوات المساعدة
│   ├── helpers.py            # دوال مساعدة
│   ├── logger.py             # نظام السجلات
│   └── __init__.py
├── 📁 data/                  # البيانات والملفات
│   ├── downloads/            # التنزيلات
│   ├── temp/                 # ملفات مؤقتة
│   └── logs/                 # ملفات السجلات
├── 📄 main.py                # الملف الرئيسي
├── 📄 config.py              # إعدادات التطبيق
├── 📄 database.py            # قاعدة البيانات
├── 📄 requirements.txt       # المتطلبات
├── 📄 .env.example           # مثال متغيرات البيئة
├── 📄 Dockerfile             # حاوي Docker
└── 📄 README.md              # هذا الملف
```

---

## 🔧 التخصيص والتطوير

### 🎨 تخصيص الرسائل
يمكنك تعديل الرسائل في ملف `bot/handlers.py`:

```python
welcome_text = f"""🌍 **أهلاً وسهلاً {user.first_name}!**
# يمكنك تخصيص هذه الرسالة حسب احتياجاتك
"""
```

### ⚙️ تعديل الإعدادات
في ملف `config.py`:

```python
class Config:
    # تعديل الحدود والإعدادات
    MAX_CONCURRENT_DOWNLOADS = 5  # زيادة التنزيلات المتوازية
    RATE_LIMIT_PER_HOUR = 20      # زيادة حد المعدل
```

### 🔌 إضافة مميزات جديدة
1. أنشئ معالج جديد في `bot/handlers.py`
2. أضف الأزرار المطلوبة في `bot/keyboards.py`
3. سجل المعالج في `main.py`

---

## 🐳 النشر باستخدام Docker

### 🏗️ بناء الحاوي
```bash
docker build -t webmaster-bot .
```

### 🚀 تشغيل الحاوي
```bash
docker run -d \
  --name webmaster-bot \
  -v $(pwd)/data:/app/data \
  --env-file .env \
  webmaster-bot
```

### 📊 مراقبة الحاوي
```bash
# عرض السجلات
docker logs -f webmaster-bot

# الدخول للحاوي
docker exec -it webmaster-bot bash
```

---

## 🔍 استكشاف الأخطاء

### ❌ مشاكل شائعة وحلولها

#### 🚫 البوت لا يستجيب
```bash
# تحقق من صحة التوكن
echo $BOT_TOKEN

# تحقق من الاتصال
curl -s "https://api.telegram.org/bot$BOT_TOKEN/getMe"
```

#### 💾 مشاكل قاعدة البيانات
```bash
# إعادة إنشاء قاعدة البيانات
rm data/database.db
python -c "from database import Base, engine; Base.metadata.create_all(engine)"
```

#### 🌐 فشل في التنزيل
- تأكد من صحة الرابط
- تحقق من اتصال الإنترنت
- راجع سجلات الأخطاء في `data/logs/`

---

## 📈 الأداء والتحسين

### ⚡ نصائح لتحسين الأداء
- استخدم SSD للتخزين
- زد من ذاكرة الخادم
- استخدم CDN للملفات الكبيرة
- فعل ضغط gzip

### 📊 مراقبة الأداء
```bash
# مراقبة استهلاك الموارد
htop

# مراقبة مساحة التخزين
df -h

# مراقبة سجلات البوت
tail -f data/logs/bot_*.log
```

---

## 🤝 المساهمة في المشروع

نرحب بمساهماتكم! إليكم كيفية المساهمة:

### 🔧 خطوات المساهمة
1. **Fork المشروع**
2. **أنشئ فرع جديد** (`git checkout -b feature/amazing-feature`)
3. **اكتب التغييرات** (`git commit -m 'Add amazing feature'`)
4. **ادفع للفرع** (`git push origin feature/amazing-feature`)
5. **افتح Pull Request**

### 📋 إرشادات المساهمة
- اتبع نمط الكود الموجود
- أضف تعليقات باللغة العربية
- اختبر التغييرات قبل الإرسال
- حدث الوثائق عند الحاجة

---

## 📄 الترخيص

هذا المشروع مرخص تحت رخصة MIT - راجع ملف [LICENSE](LICENSE) للتفاصيل.

---

## 🙏 شكر وتقدير

- **فريق Telegram Bot API** - للواجهة الرائعة
- **مطوري Playwright** - لمحرك المتصفح القوي
- **مجتمع Python** - للمكتبات المذهلة
- **جميع المساهمين** - لجعل هذا المشروع أفضل

---

## 📞 التواصل والدعم

- 📧 **البريد الإلكتروني**: support@webmaster-bot.com
- 💬 **تيليجرام**: [@WebMasterBotSupport](https://t.me/WebMasterBotSupport)
- 🐛 **الإبلاغ عن الأخطاء**: [GitHub Issues](https://github.com/yourusername/web-bot-main/issues)
- 💡 **اقتراح مميزات**: [GitHub Discussions](https://github.com/yourusername/web-bot-main/discussions)

---

<div align="center">

**⭐ إذا أعجبك المشروع، لا تنس إعطاؤه نجمة على GitHub! ⭐**

**صنع بـ ❤️ للمجتمع العربي**

</div>