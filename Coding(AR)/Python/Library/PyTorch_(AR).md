# دوال PyTorch حسب مستوى الخبرة

## `المقدمة`
**PyTorch** من أقوى مكتبات تعلم الآلة والتعلم العميق:

- ✅ بناء نماذج الشبكات العصبية
- ✅ حساب تلقائي للتدرجات (Autograd)
- ✅ دعم كامل لـ GPU/TPU

## `المزايا الأساسية`

| الميزة | الشرح |
|--------|-------|
| ⚡ أداء عالي | تسريع العمليات باستخدام GPU |
| 🧠 مرونة عالية | نماذج ديناميكية باستخدام Dynamic Computation Graph |
| 📊 تكامل مع Python | تكامل سلس مع مكتبات Python العلمية |

---
<br><br><br>

## `المستوى المبتدئ`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `torch.tensor(data)` | إنشاء تنسور | `torch.tensor([1, 2, 3])` | تنسور [1, 2, 3] |
| `torch.zeros(size)` | تنسور مملوء بأصفار | `torch.zeros(2, 3)` | تنسور 2x3 بأصفار |
| `torch.ones(size)` | تنسور مملوء بواحدات | `torch.ones(2)` | تنسور [1, 1] |
| `torch.rand(size)` | تنسور بقيم عشوائية | `torch.rand(2, 2)` | تنسور 2x2 بقيم بين 0 و1 |
| `tensor.shape` | شكل التنسور | `x.shape` | الأبعاد (2, 3) |
| `tensor.dtype` | نوع بيانات التنسور | `x.dtype` | torch.float32 |
| `tensor.to(device)` | نقل التنسور لجهاز | `x.to('cuda')` | تنسور على GPU |
| `torch.add(x, y)` | جمع تنسورات | `torch.add(x, y)` | ناتج جمع x و y |
| `torch.mm(x, y)` | ضرب مصفوفات | `torch.mm(x, y)` | نتيجة الضرب |
| `torch.sum(x)` | مجموع التنسور | `torch.sum(x)` | المجموع الكلي |

---
<br><br><br>

## `المستوى المتوسط`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `torch.nn.Linear(in, out)` | طبقة خطية | `nn.Linear(10, 5)` | طبقة 10 → 5 |
| `torch.nn.Conv2d(in, out, k)` | طبقة تلافيفية | `nn.Conv2d(3, 16, 3)` | طبقة تلافيف 3x3 |
| `torch.nn.ReLU()` | دالة تفعيل ReLU | `nn.ReLU()` | دالة التفعيل |
| `torch.optim.SGD()` | محسن SGD | `optim.SGD(model.parameters(), lr=0.01)` | كائن المحسن |
| `nn.CrossEntropyLoss()` | دالة خسارة | `nn.CrossEntropyLoss()` | دالة الخسارة |
| `model.eval()` | وضع التقييم | `model.eval()` | إيقاف Dropout/BatchNorm |
| `torch.save(model, path)` | حفظ النموذج | `torch.save(model, 'model.pth')` | ملف النموذج |
| `torch.load(path)` | تحميل النموذج | `torch.load('model.pth')` | النموذج المحمل |
| `DataLoader(dataset, batch)` | تحميل البيانات | `DataLoader(ds, batch_size=32)` | محمل البيانات |
| `torchvision.transforms` | تحويلات الصور | `transforms.Compose([...])` | تحويلات الصور |

---
<br><br><br>

## `المستوى المتقدم`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `torch.autograd.grad()` | حساب التدرجات | `torch.autograd.grad(output, input)` | تدرجات الإخراج |
| `@torch.jit.script` | تحويل النموذج لـ TorchScript | `@torch.jit.script def foo(x):` | نموذج محسن |
| `torch.distributed` | تدريب موزع | `torch.distributed.init_process_group()` | إعداد التدريب الموزع |
| `torch.nn.Parameter()` | معلمة النموذج | `nn.Parameter(torch.rand(10))` | معلمة قابلة للتعلم |
| `torch.nn.utils.clip_grad_` | قص التدرجات | `clip_grad_norm_(model.parameters(), 1.0)` | تدرجات مقصوصة |
| `torch.onnx.export()` | تصدير لـ ONNX | `torch.onnx.export(model, ...)` | نموذج ONNX |
| `torch.jit.trace()` | تتبع النموذج | `torch.jit.trace(model, example_input)` | نموذج متتبع |
| `torch.nn.DataParallel` | تدريب متوازي | `DataParallel(model)` | نموذج متوازي |
| `torch.cuda.amp` | تدريب مختلط الدقة | `autocast(enabled=True)` | تدريب أسرع |
| `torch.nn.functional` | دوال الشبكات | `F.interpolate(x, scale_factor=2)` | تغيير حجم الصور |

---
<br><br><br>

## `مستوى الخبير`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `torch.autograd.Function` | دالة مخصصة | `class MyFunc(Function): ...` | عملية مخصصة |
| `torch.nn.Module` | بناء نموذج مخصص | `class MyModel(nn.Module): ...` | نموذج مخصص |
| `torch._C` | واجهة C++ | `torch._C._jit_pass_constant_propagation` | وصول منخفض المستوى |
| `torch.utils.benchmark` | قياس الأداء | `Timer(stmt='x + y', ...)` | قياس زمن التنفيذ |
| `torch.profiler` | تحليل الأداء | `torch.profiler.profile(...)` | تحليل الأداء |
| `torch.utils.tensorboard` | تصور التدريب | `SummaryWriter()` | تسجيل نتائج التدريب |
| `torch.distributions` | التوزيعات الاحتمالية | `distributions.Normal(0, 1)` | توزيع احتمالي |
| `torch.sparse` | تنسورات متناثرة | `torch.sparse_coo_tensor(...)` | تنسورات متناثرة |
| `torch.jit.script_if_tracing` | تحسين البرمجة | `@script_if_tracing def foo(x):` | تحسين البرمجة |
| `torch.overrides` | تعديل السلوك | `@overrides.handle_torch_function` | تعديل سلوك PyTorch |