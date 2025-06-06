# `Python Methods`

# `List Methods`

| #  | Method          | الوصف                              | Example                     | Result             |
|----|-----------------|------------------------------------|-----------------------------|--------------------|
| 1  | `append(x)`     | إضافة عنصر إلى نهاية القائمة       | `lst = [1,2]; lst.append(3)`| `[1, 2, 3]`        |
| 2  | `clear()`       | إزالة جميع العناصر                 | `lst = [1,2]; lst.clear()`  | `[]`               |
| 3  | `copy()`        | إنشاء نسخة سطحية من القائمة        | `lst = [1,2]; lst.copy()`   | `[1, 2]`           |
| 4  | `count(x)`      | حساب عدد تكرارات العنصر x          | `[1,1,2].count(1)`          | `2`                |
| 5  | `extend(iter)`  | توسيع القائمة بعناصر متكررة        | `[1,2].extend([3,4])`       | `[1, 2, 3, 4]`     |
| 6  | `index(x)`      | إيجاد أول ظهور للعنصر x             | `['a','b'].index('b')`      | `1`                |
| 7  | `insert(i,x)`   | إدراج العنصر x في الموضع i          | `[1,3].insert(1,2)`         | `[1, 2, 3]`        |
| 8  | `pop([i])`      | إزالة وإرجاع العنصر في الموضع i     | `[1,2,3].pop(1)`            | `2` (تصبح القائمة `[1, 3]`) |
| 9  | `remove(x)`     | إزالة أول ظهور للعنصر x             | `[1,2,1].remove(1)`         | `[2, 1]`           |
| 10 | `reverse()`     | عكس ترتيب العناصر                   | `[1,2].reverse()`           | `[2, 1]`           |
| 11 | `sort()`        | ترتيب القائمة تصاعدياً              | `[3,1,2].sort()`            | `[1, 2, 3]`        |

# `Dictionary Methods`

| #  | Method          | الوصف                              | Example                     | Result             |
|----|-----------------|------------------------------------|-----------------------------|--------------------|
| 1  | `clear()`       | إزالة جميع العناصر                 | `d = {'a':1}; d.clear()`    | `{}`               |
| 2  | `copy()`        | إنشاء نسخة سطحية من القاموس        | `d = {'a':1}; d.copy()`     | `{'a':1}`          |
| 3  | `fromkeys(seq)` | إنشاء قاموس جديد من سلسلة مفاتيح   | `dict.fromkeys(['a','b'])`  | `{'a':None, 'b':None}` |
| 4  | `get(k[,d])`    | الحصول على قيمة المفتاح أو افتراضية | `{'a':1}.get('a')`          | `1`                |
| 5  | `items()`       | عرض أزواج المفتاح/القيمة           | `{'a':1}.items()`           | `dict_items([('a', 1)])` |
| 6  | `keys()`        | عرض المفاتيح                       | `{'a':1}.keys()`            | `dict_keys(['a'])` |
| 7  | `pop(k[,d])`    | إزالة المفتاح وإرجاع قيمته          | `{'a':1}.pop('a')`          | `1`                |
| 8  | `popitem()`     | إزالة وإرجاع آخر زوج مفتاح/قيمة    | `{'a':1,'b':2}.popitem()`   | `('b', 2)`         |
| 9  | `setdefault(k[,d])`| الحصول على القيمة أو إدراج افتراضية | `{}.setdefault('a',1)`      | `1` (يصبح القاموس `{'a':1}`) |
| 10 | `update(other)` | تحديث القاموس بأزواج مفتاح/قيمة    | `{'a':1}.update({'b':2})`   | `{'a':1, 'b':2}`   |
| 11 | `values()`      | عرض القيم                          | `{'a':1}.values()`          | `dict_values([1])` |

# `Set Methods`

| #  | Method                      | Shortcut | الوصف | Example | Result |
|----|-----------------------------|----------|-------|---------|--------|
| 1  | `add(element)`              |          | إضافة عنصر للمجموعة | `s = {1,2}; s.add(3)` | `{1, 2, 3}` |
| 2  | `clear()`                   |          | إزالة جميع العناصر | `s = {1,2}; s.clear()` | `set()` |
| 3  | `copy()`                    |          | إنشاء نسخة سطحية | `s = {1,2}; s.copy()` | `{1, 2}` |
| 4  | `difference(other_set)`     | `-`      | العناصر الموجودة هنا فقط | `{1,2}.difference({2,3})` | `{1}` |
| 5  | `difference_update(other_set)` | `-=`  | تحديث المجموعة بالفرق | `s = {1,2}; s.difference_update({2})` | `{1}` |
| 6  | `discard(element)`          |          | إزالة عنصر إذا وجد | `s = {1,2}; s.discard(1)` | `{2}` |
| 7  | `intersection(other_set)`   | `&`      | العناصر المشتركة | `{1,2} & {2,3}` | `{2}` |
| 8  | `intersection_update(other_set)` | `&=` | تحديث المجموعة بالعناصر المشتركة | `s = {1,2}; s &= {2,3}` | `{2}` |
| 9  | `isdisjoint(other_set)`     |          | هل المجموعات منفصلة؟ | `{1}.isdisjoint({2})` | `True` |
| 10 | `issubset(other_set)`       | `<=`     | هل هذه المجموعة فرعية؟ | `{1}.issubset({1,2})` | `True` |
| 11 |                             | `<`      | هل هذه المجموعة فرعية حقيقية؟ | `{1} < {1,2}` | `True` |
| 12 | `issuperset(other_set)`     | `>=`     | هل هذه المجموعة شاملة؟ | `{1,2} >= {1}` | `True` |
| 13 |                             | `>`      | هل هذه المجموعة شاملة حقيقية؟ | `{1,2} > {1}` | `True` |
| 14 | `pop()`                     |          | إزالة وإرجاع عنصر عشوائي | `s = {1}; s.pop()` | `1` (تصبح المجموعة `set()`) |
| 15 | `remove(element)`           |          | إزالة عنصر محدد | `s = {1,2}; s.remove(1)` | `{2}` |
| 16 | `symmetric_difference(other_set)` | `^` | العناصر غير المشتركة | `{1,2} ^ {2,3}` | `{1, 3}` |
| 17 | `symmetric_difference_update(other_set)` | `^=` | تحديث المجموعة بالعناصر غير المشتركة | `s = {1,2}; s ^= {2,3}` | `{1, 3}` |
| 18 | `union(other_set)`          | `\|`     | اتحاد المجموعات | `{1} \| {2}` | `{1, 2}` |
| 19 | `update(other_set)`         | `\|=`    | تحديث المجموعة بالاتحاد | `s = {1}; s.update({2})` | `{1, 2}` |

# `Tuple Methods`

| #  | Method       | الوصف | Example | Result |
|----|--------------|-------|---------|--------|
| 1  | `count(value)` | حساب عدد التكرارات | `(1, 2, 2, 3).count(2)` | `2` |
| 2  | `index(value)` | إيجاد أول ظهور للعنصر | `('a', 'b', 'c').index('b')` | `1` |
