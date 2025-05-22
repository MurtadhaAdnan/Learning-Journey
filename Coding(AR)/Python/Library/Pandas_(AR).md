# دوال pandas حسب مستوى الخبرة

## `المقدمة`
**pandas** من أقوى مكتبات تحليل البيانات:

- ✅ معالجة وتنظيف البيانات
- ✅ التعامل مع البيانات المنظمة (DataFrames/Series)
- ✅ تكامل مع مكتبات التصور والذكاء الاصطناعي

## `المزايا الأساسية`

| الميزة | الشرح |
|--------|-------|
| ⚡ عمليات سريعة | محسنة للأداء باستخدام محرك C |
| 🧠 هياكل بيانات مرنة | DataFrames و Series لأنواع البيانات المختلفة |
| 📊 تصور مدمج | إنشاء رسوم بيانية سريعة باستخدام .plot() |

---
<br><br><br>

## `المستوى المبتدئ`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `pd.Series(data)` | إنشاء سلسلة | `pd.Series([1, 2, 3])` | `0:1, 1:2, 2:3` |
| `pd.DataFrame(data)` | إنشاء إطار بيانات | `pd.DataFrame({'A':[1,2]})` | إطار بيانات بعمود 'A' |
| `df.head(n)` | عرض أول n صف | `df.head(3)` | أول 3 صفوف |
| `df.tail(n)` | عرض آخر n صف | `df.tail(2)` | آخر صفين |
| `df.shape` | الحصول على الأبعاد | `df.shape` | `(صفوف، أعمدة)` |
| `df.describe()` | إحصائيات ملخصة | `df.describe()` | العدد/المتوسط/الانحراف المعياري |
| `df['col'].value_counts()` | عد القيم الفريدة | `df['A'].value_counts()` | توزيع القيم |
| `df.sort_values('col')` | ترتيب حسب العمود | `df.sort_values('A')` | إطار بيانات مرتب |
| `df.dropna()` | إزالة القيم المفقودة | `df.dropna()` | إطار بيانات نظيف |
| `df.fillna(value)` | تعبئة القيم المفقودة | `df.fillna(0)` | إطار بيانات مكتمل |

---
<br><br><br>

## `المستوى المتوسط`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `pd.read_csv(file)` | قراءة ملف CSV | `pd.read_csv('data.csv')` | إطار بيانات محمل |
| `df.groupby('col')` | عمليات التجميع | `df.groupby('A').mean()` | تجميعات البيانات |
| `df.merge(df2, on='col')` | دمج إطارات البيانات | `df1.merge(df2, on='ID')` | إطار بيانات مدمج |
| `df.pivot_table()` | إنشاء جدول محوري | `df.pivot_table(values='B', index='A')` | جدول محوري |
| `df.apply(func)` | تطبيق دالة | `df['A'].apply(lambda x: x*2)` | عمود محوّل |
| `pd.get_dummies(df)` | الترميز الأحادي | `pd.get_dummies(df['A'])` | إطار بيانات مشفر |
| `df.corr()` | مصفوفة الارتباط | `df.corr()` | قيم الارتباط |
| `df.plot()` | رسم بياني سريع | `df['A'].plot()` | رسم بياني |
| `df.to_csv(file)` | حفظ كملف CSV | `df.to_csv('out.csv')` | ملف محفوظ |
| `df.isna().sum()` | عد القيم المفقودة | `df.isna().sum()` | عدد القيم المفقودة |

---
<br><br><br>

## `المستوى المتقدم`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `pd.melt(df)` | تفكيك إطار البيانات | `pd.melt(df, id_vars='A')` | إطار بيانات معاد تشكيله |
| `df.pipe(func)` | سلسلة العمليات | `df.pipe(clean).pipe(transform)` | إطار بيانات معالج |
| `df.rolling(n).mean()` | حسابات متحركة | `df['A'].rolling(3).mean()` | متوسطات متحركة |
| `pd.qcut(df['col'], q)` | تقسيم إلى شرائح | `pd.qcut(df['A'], 4)` | فئات مقسمة |
| `df.style` | تنسيق المخرجات | `df.style.background_gradient()` | إطار بيانات منسق |
| `pd.IntervalIndex` | فهرسة الفواصل | `pd.IntervalIndex.from_breaks([1,2,3])` | فهرس الفواصل |
| `pd.api.extensions` | توسيع pandas | أنواع مخصصة | وظائف ممتدة |
| `pd.eval()` | تقييم التعابير | `pd.eval("df.A + df.B")` | نتيجة التقييم |
| `df.explode('col')` | توسيع العناصر | `df.explode('list_col')` | صفوف ممتدة |
| `df.to_parquet()` | حفظ كملف Parquet | `df.to_parquet('data.parquet')` | ملف ثنائي |

---
<br><br><br>

## `مستوى الخبير`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `pd.DataFrame.sparse` | إطارات البيانات المتناثرة | `df.sparse.from_spmatrix(matrix)` | إطار بيانات موفر للذاكرة |
| `pd.io.formats.style` | تنسيق مخصص | تنسيق HTML/CSS مخصص | جداول جاهزة للنشر |
| `pd.testing` | أدوات الاختبار | `pd.testing.assert_frame_equal()` | مساعدات اختبار الوحدات |
| `pd.Grouper` | تجميع متقدم | `df.groupby(pd.Grouper(key='date', freq='M'))` | تجميع زمني |
| `pd.DataFrame.attrs` | تخزين البيانات الوصفية | `df.attrs['desc'] = "..."` | بيانات وصفية مرفقة |
| `pd.core.groupby.DataFrameGroupBy.__iter__` | تكرار المجموعات | معالجة مجموعات مخصصة | تحكم دقيق |
| `pd.api.types` | أدوات الأنواع | `pd.api.types.is_numeric_dtype()` | فحص الأنواع |
| `pd.io.sql` | تكامل SQL | `pd.read_sql(query, conn)` | عمليات قاعدة البيانات |
| `pd.json_normalize()` | تسطيح JSON | `pd.json_normalize(nested_json)` | إطار بيانات مسطح |
| `pd.set_eng_float_format()` | تنسيق العرض | `pd.set_eng_float_format(accuracy=2)` | ترميز هندسي |