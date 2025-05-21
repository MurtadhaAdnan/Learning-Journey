# دوال Gymnasium حسب مستوى الخبرة

## `المقدمة`
**Gymnasium** (المعروفة سابقًا بـ Gym) هي مكتبة لتطوير ومقارنة خوارزميات التعلم المعزز:

- ✅ توفر بيئات معيارية للاختبار
- ✅ تدعم مجموعة واسعة من المهام
- ✅ تكامل مع أطر التعلم الآلي الرئيسية

## `المزايا الأساسية`

| الميزة | الشرح |
|--------|-------|
| ⚡ بيئات متنوعة | أكثر من 100 بيئة جاهزة |
| 🧠 واجهة موحدة | API بسيط ومتسق لجميع البيئات |
| 📊 دعم التصور | عرض نتائج التدريب بشكل مرئي |

---
<br><br><br>

## `المستوى المبتدئ`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `gymnasium.make(id)` | إنشاء بيئة | `env = gymnasium.make('CartPole-v1')` | كائن البيئة |
| `env.reset()` | إعادة تعيين البيئة | `observation = env.reset()` | الحالة الأولية |
| `env.step(action)` | تنفيذ خطوة | `observation, reward, done, info = env.step(action)` | نتائج الإجراء |
| `env.render()` | عرض البيئة | `env.render()` | نافذة العرض |
| `env.action_space` | فضاء الإجراءات | `print(env.action_space)` | معلومات الإجراءات الممكنة |
| `env.observation_space` | فضاء الملاحظات | `print(env.observation_space)` | معلومات الحالة |
| `env.close()` | إغلاق البيئة | `env.close()` | تحرير الموارد |
| `env.seed()` | تحديد البذرة | `env.seed(42)` | نتائج قابلة للتكرار |
| `gymnasium.__version__` | إصدار المكتبة | `print(gymnasium.__version__)` | رقم الإصدار |
| `env.spec` | مواصفات البيئة | `print(env.spec)` | معلومات البيئة |

---
<br><br><br>

## `المستوى المتوسط`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `Wrappers` | تعديل البيئات | `env = TimeLimit(env, max_episode_steps=100)` | بيئة معدلة |
| `VectorEnv` | بيئات متوازية | `envs = gymnasium.vector.make('CartPole-v1', num_envs=4)` | بيئات متعددة |
| `env.step()` مع متجه | خطوات متوازية | `observations, rewards, dones, infos = envs.step(actions)` | خطوات متعددة |
| `RecordVideo` | تسجيل الفيديو | `env = RecordVideo(env, 'videos')` | تسجيل الجلسات |
| `Monitor` | تسجيل النتائج | `env = Monitor(env, 'results')` | تسجيل الإحصائيات |
| `env.get_action_meanings()` | معاني الإجراءات | `print(env.get_action_meanings())` | تفسير الإجراءات |
| `env.unwrapped` | الوصول للبيئة الأصلية | `base_env = env.unwrapped` | البيئة غير المغلقة |
| `env.reward_range` | نطاق المكافأة | `print(env.reward_range)` | الحد الأدنى والأقصى للمكافأة |
| `env.metadata` | بيانات وصفية | `print(env.metadata)` | معلومات إضافية |
| `env.configure()` | تكوين البيئة | `env.configure(remotes=1)` | تغيير الإعدادات |

---
<br><br><br>

## `المستوى المتقدم`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `Env` فصل مخصص | إنشاء بيئة مخصصة | `class MyEnv(gymnasium.Env): ...` | بيئة جديدة |
| `Space` فضاء مخصص | تعريف فضاء مخصص | `class MySpace(gymnasium.Space): ...` | فضاء جديد |
| `register()` | تسجيل بيئات | `gymnasium.register(id='MyEnv-v0', entry_point='myenv:MyEnv')` | بيئة مسجلة |
| `AsyncVectorEnv` | بيئات غير متزامنة | `envs = AsyncVectorEnv([make_env])` | بيئات متوازية |
| `Wrapper` مخصص | إنشاء غلاف مخصص | `class MyWrapper(gymnasium.Wrapper): ...` | سلوك معدل |
| `env.physics` | محرك فيزيائي | `print(env.physics)` | الوصول للمحرك |
| `env.model` | نموذج البيئة | `print(env.model)` | هيكل البيئة |
| `env.sim` | محاكاة البيئة | `print(env.sim)` | حالة المحاكاة |
| `env.render(mode='rgb_array')` | إخراج صورة | `img = env.render(mode='rgb_array')` | مصفوفة بكسل |
| `env.compute_reward()` | حساب مخصص للمكافأة | `reward = env.compute_reward(achieved_goal, desired_goal)` | مكافأة مخصصة |

---
<br><br><br>

## `مستوى الخبير`

| الدالة | الوصف | مثال | النتيجة |
|--------|-------|------|---------|
| `VectorEnv` مخصص | بيئات متوازية مخصصة | `class MyVectorEnv(gymnasium.vector.VectorEnv): ...` | تنفيذ متوازي |
| `env.get_attr()` | الحصول على خصائص | `values = env.get_attr('attribute')` | قراءة الخصائص |
| `env.set_attr()` | تعيين خصائص | `env.set_attr('attribute', value)` | تعديل الخصائص |
| `env.call()` | استدعاء دالة | `results = env.call('method', *args)` | تنفيذ طرق |
| `env.env_method()` | استدعاء طريقة البيئة | `results = env.env_method('method', *args)` | تنفيذ على البيئات |
| `env.close_extras()` | تنظيف إضافي | `env.close_extras()` | تحرير موارد إضافية |
| `env.observation()` | تحويل الملاحظة | `obs = env.observation(obs)` | معالجة الملاحظة |
| `env.action()` | تحويل الإجراء | `action = env.action(action)` | معالجة الإجراء |
| `env.reward()` | تحويل المكافأة | `reward = env.reward(reward)` | معالجة المكافأة |
| `env.info()` | تحويل المعلومات | `info = env.info(info)` | معالجة المعلومات |