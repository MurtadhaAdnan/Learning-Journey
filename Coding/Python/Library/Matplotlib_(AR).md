# دوال Matplotlib حسب مستوى الخبرة

## `المقدمة`
**Matplotlib** هي مكتبة الرسم الأساسية في بايثون:

- ✅ إنشاء رسومات احترافية للنشر
- ✅ دعم لأنواع متعددة من الرسومات (خطية، أعمدة، مبعثرة، إلخ)
- ✅ قابلة للتخصيص بدرجة عالية وقابلة للتوسيع

## `المزايا الأساسية`

| الميزة | الشرح |
|--------|-------|
| ⚡ رسومات متعددة الاستخدامات | تدعم الرسومات ثنائية وثلاثية الأبعاد |
| 🧠 تكامل مع بايثون | تعمل بتناغم مع NumPy وPandas |
| 📊 تخصيص متقدم | تحكم دقيق في كل عنصر من عناصر الرسم |

---
<br><br><br>

## `المستوى المبتدئ`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `plt.plot(x, y)` | رسم خطي أساسي | `plt.plot([1,2,3], [1,4,9])` | رسم بياني خطي بسيط |
| `plt.scatter(x, y)` | رسم مبعثر | `plt.scatter(x, y)` | رسم بالنقاط |
| `plt.bar(x, height)` | رسم أعمدة | `plt.bar(['أ','ب'], [3,5])` | أعمدة رأسية |
| `plt.hist(data)` | رسم توزيع | `plt.hist(np.random.randn(100))` | رسم توزيع البيانات |
| `plt.title(text)` | إضافة عنوان | `plt.title('رسمي البياني')` | رسم بعنوان |
| `plt.xlabel(text)` | تسمية محور السينات | `plt.xlabel('قيم س')` | محور سينات مسمى |
| `plt.ylabel(text)` | تسمية محور الصادات | `plt.ylabel('قيم ص')` | محور صادات مسمى |
| `plt.show()` | عرض الرسم | `plt.show()` | عرض الرسم البياني |
| `plt.savefig(path)` | حفظ الرسم | `plt.savefig('رسم.png')` | حفظ كصورة |
| `plt.legend()` | إضافة وسيلة إيضاح | `plt.legend(['الخط1'])` | رسم مع وسيلة إيضاح |

---
<br><br><br>

## `المستوى المتوسط`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `plt.subplots(nrows, ncols)` | رسومات متعددة | `fig, ax = plt.subplots(2,2)` | رسم متعدد الأجزاء |
| `ax.plot()` | رسم على محور معين | `ax[0,0].plot(x,y)` | رسم خطي في جزء معين |
| `plt.style.use(style)` | تحديد النمط | `plt.style.use('ggplot')` | رسم بأسلوب معين |
| `plt.figure(figsize)` | تحديد حجم الرسم | `plt.figure(figsize=(10,5))` | رسم بحجم مخصص |
| `plt.grid()` | إضافة شبكة | `plt.grid(True)` | رسم بشبكة توجيهية |
| `plt.tight_layout()` | ضبط المسافات | `plt.tight_layout()` | تحسين المسافات بين الرسومات |
| `plt.colorbar()` | إضافة مقياس ألوان | `plt.colorbar()` | شريط ألوان |
| `plt.xticks(ticks)` | تخصيص علامات المحور | `plt.xticks([0,1,2])` | محور سينات معدل |
| `plt.ylim(min, max)` | تحديد حدود المحور | `plt.ylim(0,10)` | نطاق ثابت لمحور الصادات |
| `plt.annotate(text, xy)` | إضافة تعليق | `plt.annotate('قمة', (2,4))` | رسم مع تعليق نصي |

---
<br><br><br>

## `المستوى المتقدم`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `fig.add_subplot(projection)` | رسومات ثلاثية الأبعاد | `ax = fig.add_subplot(111, projection='3d')` | رسم ثلاثي الأبعاد |
| `plt.contour(X,Y,Z)` | رسم خطوط الكنتور | `plt.contour(X,Y,Z)` | رسم خطوط متساوية |
| `plt.imshow(data)` | عرض صورة | `plt.imshow(np.random.rand(10,10))` | عرض مصفوفة كصورة |
| `plt.fill_between(x,y1,y2)` | تعبئة المساحة | `plt.fill_between(x,y1,y2)` | مساحة مملوءة |
| `plt.errorbar(x,y,yerr)` | أشرطة الخطأ | `plt.errorbar(x,y,yerr=0.2)` | رسم مع أشرطة خطأ |
| `plt.pcolormesh(X,Y,Z)` | رسم شبكة ملونة | `plt.pcolormesh(X,Y,Z)` | شبكة بألوان متدرجة |
| `plt.stem(x,y)` | رسم الساق والورقة | `plt.stem(x,y)` | رسم قيم منفصلة |
| `plt.boxplot(data)` | رسم الصندوق | `plt.boxplot([data1,data2])` | رسم توزيعات |
| `plt.pie(sizes)` | رسم دائري | `plt.pie([30,70])` | رسم بياني دائري |
| `plt.quiver(X,Y,U,V)` | رسم حقل متجهي | `plt.quiver(X,Y,U,V)` | رسم بالسهام |

---
<br><br><br>

## `مستوى الخبير`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `matplotlib.animation` | رسوم متحركة | `animation.FuncAnimation(...)` | رسوم متحركة |
| `mpl_toolkits` | رسومات متخصصة | `from mpl_toolkits.mplot3d import Axes3D` | رسومات ثلاثية الأبعاد متقدمة |
| `plt.rcParams.update()` | تخصيص عام | `plt.rcParams.update({'font.size':12})` | إعدادات افتراضية مخصصة |
| `matplotlib.widgets` | أدوات تفاعلية | `widgets.Slider(...)` | رسم تفاعلي |
| `plt.gca()` | المحور الحالي | `ax = plt.gca()` | كائن المحور |
| `plt.gcf()` | الرسم الحالي | `fig = plt.gcf()` | كائن الرسم |
| `matplotlib.patches` | أشكال مخصصة | `patches.Circle((0,0),1)` | أشكال هندسية |
| `plt.text()` | نص مخصص | `plt.text(0.5,0.5,'نص')` | إضافة نص |
| `plt.xscale('log')` | مقياس لوغاريتمي | `plt.xscale('log')` | محور لوغاريتمي |
| `matplotlib.gridspec` | تخطيطات معقدة | `gridspec.GridSpec(2,2)` | تخطيطات متقدمة للرسومات |