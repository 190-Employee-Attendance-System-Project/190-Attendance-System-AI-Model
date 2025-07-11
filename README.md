# نظام الحضور باستخدام التعرف على الوجه

## النشر على Vercel

### المتطلبات المسبقة

- حساب على Vercel
- Git repository

### خطوات النشر

1. **تأكد من وجود الملفات التالية:**

   - `Face-API.py` - التطبيق الرئيسي
   - `api/index.py` - نقطة الدخول لـ Vercel
   - `vercel.json` - تكوين Vercel
   - `requirements.txt` - التبعيات
   - `runtime.txt` - إصدار Python

2. **إعداد متغيرات البيئة في Vercel:**

   - اذهب إلى لوحة تحكم Vercel
   - اختر مشروعك
   - اذهب إلى Settings > Environment Variables
   - أضف المتغيرات التالية:
     - `CLOUDINARY_NAME`
     - `CLOUDINARY_API_KEY`
     - `CLOUDINARY_API_SECRET`
     - `MONGODB_URI`

3. **النشر:**

   ```bash
   # تثبيت Vercel CLI
   npm i -g vercel

   # تسجيل الدخول
   vercel login

   # النشر
   vercel
   ```

### ملاحظات مهمة

- تأكد من أن جميع المتغيرات البيئية مضبوطة في Vercel
- قد يستغرق البناء الأول وقتاً أطول بسبب تثبيت مكتبة dlib
- تأكد من أن قاعدة البيانات MongoDB متاحة من الإنترنت

### API Endpoints

- `POST /recognize` - التعرف على الوجه
