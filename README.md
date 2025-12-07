# Fripy Educational Platform

![Fripy Logo](assets/images/fripy/fripy-main.png)

## 🎉 مرحباً بك في فريبي! / Welcome to Fripy!

فريبي هي منصة تعليمية تفاعلية للأطفال مع شخصية دبدوب لطيفة تشجعهم على التعلم وتطوير المهارات!

Fripy is an interactive educational platform for children with a cute bear mascot that encourages them to learn and develop skills!

---

## ✨ المميزات / Features

- **🐻 شخصية فريبي التفاعلية** - دبدوب كيوت يشجع ويحفز الأطفال
- **⚡ مركز الانعكاسات** - 20 كورس لتطوير سرعة رد الفعل والحركة
- **📚 تعلم العربية** - دروس الحروف، الكلمات، والنطق
- **🌍 تعلم الإنجليزية** - الأبجدية، الأصوات، والكلمات البسيطة
- **🏆 لوحة الإنجازات** - تتبع التقدم والشارات
- **🎮 منطقة اللعب** - ألعاب تفاعلية قادمة قريباً

---

## 📁 هيكل المشروع / Project Structure

```
fripy/
├── index.html                 # الصفحة الرئيسية (Homepage)
├── css/
│   ├── main.css              # تصميم النظام الأساسي (Design system)
│   ├── components.css        # مكونات قابلة لإعادة الاستخدام (Reusable components)
│   └── animations.css        # الرسوم المتحركة (Animations)
├── js/
│   ├── app.js                # المنطق الرئيسي للتطبيق (Main app logic)
│   ├── fripy-character.js    # نظام الشخصية والرسوم المتحركة (Character system)
│   ├── progress-tracker.js   # تتبع التقدم (Progress tracking)
│   └── utils.js              # دوال مساعدة (Utility functions)
├── assets/
│   ├── images/
│   │   ├── fripy/            # صور الشخصية (Character images)
│   │   └── icons/            # أيقونات وشارات (Icons & badges)
│   └── videos/               # الفيديوهات التعليمية (Training videos)
└── pages/
    ├── reflexes/
    │   ├── index.html        # صفحة الانعكاسات الرئيسية (Reflexes hub)
    │   └── course.html       # صفحة الكورس الفردية (Individual course)
    ├── learning/
    │   ├── arabic.html       # تعلم العربية (Learn Arabic)
    │   └── english.html      # تعلم الإنجليزية (Learn English)
    ├── progress.html         # لوحة الإنجازات (Progress board)
    └── play-zone.html        # منطقة اللعب (Play zone)
```

---

## 🚀 كيف تبدأ / How to Start

### الطريقة الأسهل / Easiest Way:

1. افتح ملف `index.html` في أي متصفح (Open `index.html` in any browser)
2. لا تحتاج لتنصيب أي شيء! (No installation needed!)

### فتح الموقع / Opening the Website:

```bash
# انتقل لمجلد المشروع / Navigate to project folder
cd fripy

# افتح index.html في المتصفح / Open index.html in browser
# على ويندوز / On Windows:
start index.html

# على ماك / On Mac:
open index.html

# على لينكس / On Linux:
xdg-open index.html
```

---

## 🎨 التخصيص / Customization

### تغيير الألوان / Changing Colors:

افتح `css/main.css` وعدّل متغيرات CSS:

```css
:root {
  --color-primary: #4F46E5;        /* اللون الأساسي / Primary color */
  --color-secondary: #FBBF24;      /* اللون الثانوي / Secondary color */
  --color-accent-purple: #A855F7;  /* البنفسجي / Purple */
  /* ... المزيد من الألوان / More colors ... */
}
```

### إضافة كورسات جديدة / Adding New Courses:

1. افتح `pages/reflexes/index.html`
2. انسخ بنية بطاقة الكورس (Copy the course card structure)
3. غيّر العنوان والأيقونة والوصف (Change title, icon, description)
4. احفظ الملف (Save the file)

### إضافة فيديوهات / Adding Videos:

في `pages/reflexes/course.html`، استبدل القسم التالي:

```html
<div class="video-container">
  <!-- للفيديو من يوتيوب / For YouTube video: -->
  <iframe width="100%" height="100%" 
    src="https://www.youtube.com/embed/VIDEO_ID" 
    frameborder="0" allowfullscreen>
  </iframe>
  
  <!-- أو للفيديو المحلي / Or for local video: -->
  <video class="video-player" controls>
    <source src="../../assets/videos/your-video.mp4" type="video/mp4">
  </video>
</div>
```

---

## 💾 حفظ التقدم / Saving Progress

التقدم يُحفظ تلقائياً في localStorage في المتصفح. لإعادة تعيين التقدم:

Progress is automatically saved in browser's localStorage. To reset progress:

1. افتح أدوات المطور في المتصفح (Console)
2. أكتب: `progressTracker.reset()`
3. أعد تحميل الصفحة

---

## 🎯 نصائح للتطوير / Development Tips

### إضافة دروس عربية جديدة / Adding New Arabic Lessons:

في `pages/learning/arabic.html`:

```html
<div class="card hover-lift">
  <div class="card-header">
    <div class="card-icon">ج</div>
    <div>
      <h3 class="card-title">حرف الجيم</h3>
    </div>
  </div>
  <div class="card-body">
    <button class="btn btn-primary btn-small btn-complete" 
            data-section="arabic" data-course-id="4">
      ابدأ الدرس
    </button>
  </div>
</div>
```

### تخصيص رسائل فريبي / Customizing Fripy Messages:

في `js/fripy-character.js`، عدّل:

```javascript
this.greetings = {
  morning: [
    'صباح الخير! جاهز لتبدأ يومك بنشاط؟',
    // أضف المزيد من الرسائل هنا / Add more messages here
  ]
};
```

---

## 🏆 نظام الشارات / Badge System

يحصل الأطفال على شارات عند:
- إكمال 5 فيديوهات (🚀 صاروخ التركيز)
- إكمال 10 فيديوهات (🏆 بطل الحركة)
- 7 أيام متتالية (👑 ملك الالتزام)
- إكمال 5 كورسات انعكاسات (⭐ عبقري اليوم)

Children earn badges for:
- Completing 5 videos (🚀 Focus Rocket)
- Completing 10 videos (🏆 Movement Champion)
- 7-day streak (👑 Commitment King)
- Completing 5 reflex courses (⭐ Today's Genius)

---

## 🎨 التصميم / Design

الموقع مصمم بـ:
- ألوان زاهية ومبهجة (Vibrant, cheerful colors)
- خطوط مناسبة للأطفال (Child-friendly fonts: Fredoka & Nunito)
- رسوم متحركة سلسة (Smooth animations)
- تصميم متجاوب (Responsive design)
- واجهة آمنة وودودة (Safe & friendly interface)

---

## 📱 التوافق / Compatibility

- ✅ Chrome / Edge / Firefox / Safari
- ✅ أجهزة الموبايل (Mobile devices)
- ✅ التابلت (Tablets)
- ✅ سطح المكتب (Desktop)

---

## 🛠️ التقنيات المستخدمة / Technologies Used

- **HTML5** - البنية الأساسية / Structure
- **CSS3** - التصميم والرسوم المتحركة / Styling & animations
- **Vanilla JavaScript** - الوظائف التفاعلية / Interactive functionality
- **localStorage** - حفظ التقدم / Save progress
- **Google Fonts** - الخطوط الجميلة / Beautiful fonts

---

## ❓ أسئلة شائعة / FAQ

**س: كيف أغير صورة فريبي؟**
ج: استبدل الصور في مجلد `assets/images/fripy/`

**Q: How do I change Fripy's image?**
A: Replace images in `assets/images/fripy/` folder

**س: كيف أضيف المزيد من الكورسات؟**
ج: انسخ بطاقة الكورس الموجودة وغيّر المحتوى

**Q: How do I add more courses?**
A: Copy an existing course card and modify the content

---

## 💜 مع الحب من فريبي / Made with Love by Fripy

استمتع بالتعلم! 🚀

Enjoy learning! 🚀
