# دوال PyQt5 حسب مستوى الخبرة

## `المقدمة`
**PyQt5** هي مكتبة شاملة لإنشاء تطبيقات واجهة المستخدم الرسومية:

- ✅ بناء تطبيقات سطح المكتب
- ✅ توافق عبر الأنظمة
- ✅ مكتبة واسعة من الأدوات

## `المزايا الأساسية`

| الميزة | الشرح |
|--------|-------|
| ⚡ أداء أصلي | وصول مباشر إلى مكتبة Qt |
| 🧠 تكامل مع بايثون | كل إمكانيات Qt متاحة في بايثون |
| 📊 أدوات التصور | رسوم بيانية وعرض بيانات |

---
<br><br><br>

## `المستوى المبتدئ`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `QApplication(sys.argv)` | إنشاء تطبيق | `app = QApplication(sys.argv)` | كائن التطبيق |
| `QWidget()` | أداة أساسية | `window = QWidget()` | نافذة فارغة |
| `QPushButton(text)` | إنشاء زر | `btn = QPushButton('انقر')` | أداة زر |
| `QLabel(text)` | إنشاء تسمية | `label = QLabel('مرحبا')` | تسمية نصية |
| `QVBoxLayout()` | تخطيط عمودي | `layout = QVBoxLayout()` | مدير تخطيط |
| `QHBoxLayout()` | تخطيط أفقي | `layout = QHBoxLayout()` | مدير تخطيط |
| `QLineEdit()` | حقل إدخال | `input = QLineEdit()` | حقل نصي |
| `show()` | عرض الأداة | `window.show()` | نافذة مرئية |
| `exec_()` | بدء الحلقة | `app.exec_()` | تطبيق يعمل |
| `setWindowTitle(text)` | تعيين عنوان | `window.setWindowTitle('تطبيق')` | نافذة بعنوان |

---
<br><br><br>

## `المستوى المتوسط`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `QMainWindow()` | النافذة الرئيسية | `window = QMainWindow()` | نافذة التطبيق |
| `QMessageBox` | نوافذ حوار | `QMessageBox.information(None, 'عنوان', 'نص')` | نافذة منبثقة |
| `QTabWidget()` | واجهة تبويب | `tabs = QTabWidget()` | واجهة متعددة |
| `QMenuBar()` | شريط القوائم | `menubar = window.menuBar()` | قوائم النافذة |
| `QStatusBar()` | شريط الحالة | `status = window.statusBar()` | عرض الحالة |
| `QAction(text)` | إجراء قائمة | `action = QAction('فتح')` | عنصر قائمة |
| `QFileDialog` | نوافذ ملفات | `QFileDialog.getOpenFileName()` | محدد ملفات |
| `QTimer()` | مؤقت | `timer = QTimer()` | أحداث زمنية |
| `QThread()` | خيوط تنفيذ | `thread = QThread()` | تنفيذ خلفي |
| `signal.connect(slot)` | معالجة الأحداث | `btn.clicked.connect(func)` | رد فعل الزر |

---
<br><br><br>

## `المستوى المتقدم`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `QGraphicsView()` | عرض رسومي | `view = QGraphicsView()` | لوحة رسم |
| `QGraphicsScene()` | مشهد رسومي | `scene = QGraphicsScene()` | حاوية رسومية |
| `QPainter()` | رسم مخصص | `painter = QPainter()` | واجهة رسم |
| `QStyledItemDelegate()` | مفوض مخصص | `class MyDelegate(QStyledItemDelegate)` | عرض عناصر مخصص |
| `QAbstractItemModel()` | نماذج بيانات | `class MyModel(QAbstractItemModel)` | نموذج بيانات مخصص |
| `QPropertyAnimation()` | تحريك | `anim = QPropertyAnimation(widget, b'pos')` | تحريك أداة |
| `QWebEngineView()` | متصفح ويب | `web = QWebEngineView()` | متصفح مدمج |
| `QSplashScreen()` | شاشة بداية | `splash = QSplashScreen(pixmap)` | شاشة ترحيب |
| `QSystemTrayIcon()` | أيقونة النظام | `tray = QSystemTrayIcon()` | أيقونة في شريط المهام |
| `QDataWidgetMapper()` | ربط بيانات | `mapper = QDataWidgetMapper()` | ربط واجهة بالبيانات |

---
<br><br><br>

## `مستوى الخبير`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `QOpenGLWidget()` | أداة OpenGL | `gl = QOpenGLWidget()` | عرض ثلاثي الأبعاد |
| `QPluginLoader()` | نظام ملحقات | `loader = QPluginLoader('plugin.so')` | ملحق محمل |
| `QDBus` | اتصال بين عمليات | `QDBusConnection.sessionBus()` | اتصال D-Bus |
| `QStyleFactory` | تخصيص واجهة | `app.setStyle(QStyleFactory.create('Fusion'))` | تنسيق واجهة |
| `QAbstractNativeEventFilter` | أحداث نظام | `class MyFilter(QAbstractNativeEventFilter)` | معالجة أحدث نظام |
| `QWinTaskbarButton` (ويندوز) | شريط مهام | `taskbtn = QWinTaskbarButton()` | شريط مهام ويندوز |
| `QMacToolBar` (ماك) | شريط أدوات | `toolbar = QMacToolBar()` | شريط أدوات ماك |
| `QtWin` (ويندوز) | خصائص ويندوز | `QtWin.setWindowExcludedFromPeek(winId(), True)` | إعدادات خاصة |
| `QGenericArgument` | كائنات ديناميكية | `QGenericArgument("int", 42)` | استدعاء ديناميكي |
| `QMetaObject` | انعكاس | `metaobj = widget.metaObject()` | فحص الكائنات |