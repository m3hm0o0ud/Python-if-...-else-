# Python-if-...-else-
Python Conditions and If statements

### درس شامل: الشروط واستخدام عبارات `if` و `else` في لغة البرمجة بايثون

#### مقدمة

في عالم البرمجة، تُعتبر عبارات الشرط (Conditional Statements) من الأدوات الأساسية التي تُمكِّن المبرمجين من تنفيذ الأكواد بناءً على شروط محددة. في لغة بايثون (Python)، تُعد عبارة `if` واحدة من أهم هذه العبارات. من خلال هذه العبارة، يمكن للبرنامج اتخاذ قرارات وتنفيذ أكواد بناءً على ما إذا كانت الشروط قد تحققت أم لا. كما تُستخدم العبارات `elif` و `else` لتعزيز التحكم في تدفق الأكواد بناءً على شروط متعددة.

---

#### الشروط المنطقية في بايثون

بايثون تدعم مجموعة من الشروط المنطقية الشائعة التي تُستخدم للتحقق من القيم المختلفة داخل العبارات الشرطية:

- **يساوي**: `a == b`
- **لا يساوي**: `a != b`
- **أقل من**: `a < b`
- **أقل من أو يساوي**: `a <= b`
- **أكبر من**: `a > b`
- **أكبر من أو يساوي**: `a >= b`

---

#### الصيغة العامة لعبارة `if`

الصيغة الأساسية لكتابة عبارة `if` في بايثون هي كالتالي:

```python
if condition:
    # code to execute if the condition is True
```

- **`condition`**: هو تعبير منطقي (Boolean expression) يتم تقييمه ليعطي قيمة `True` (صحيح) أو `False` (خطأ).
- **`code`**: هو الكود الذي سيتم تنفيذه إذا كان الشرط `True`. يجب أن يكون هذا الكود مُزاحًا (indented) بمسافة بادئة (Indentation) لضمان أنه جزء من العبارة `if`.

##### مثال على استخدام `if`

لنأخذ مثالًا بسيطًا لفهم كيفية عمل العبارة `if`:

```python
age = 20

if age >= 18:
    print("You are an adult!")
```

في هذا المثال:
- الشرط `age >= 18` يتحقق إذا كانت قيمة `age` تساوي أو تزيد عن 18.
- إذا كان الشرط صحيحًا (`True`)، سيقوم البرنامج بطباعة "You are an adult!".

---

#### استخدام `else` مع `if`

في بعض الأحيان، نحتاج إلى تنفيذ كود معين في حالة عدم تحقق الشرط. هنا يأتي دور العبارة `else` التي تُستخدم لتحديد ما يجب القيام به إذا كان الشرط خاطئًا (`False`).

```python
age = 16

if age >= 18:
    print("You are an adult!")
else:
    print("You are a minor!")
```

في هذا المثال:
- إذا كان الشرط `age >= 18` صحيحًا، سيتم تنفيذ الكود الأول وطباعة "You are an adult!".
- إذا كان الشرط خاطئًا (`False`)، سيتم تنفيذ الكود الثاني وطباعة "You are a minor!".

---

#### استخدام `elif` لتحديد شروط متعددة

في بعض الحالات، قد نحتاج إلى التحقق من شروط متعددة. هنا تأتي أهمية العبارة `elif` (اختصار لـ "else if") التي تُستخدم لإضافة شروط إضافية.

```python
age = 15

if age >= 18:
    print("You are an adult!")
elif age >= 13:
    print("You are a teenager!")
else:
    print("You are a child!")
```

في هذا المثال:
- إذا كان `age >= 18` صحيحًا، سيقوم البرنامج بطباعة "You are an adult!".
- إذا كان الشرط الأول خاطئًا وتحقق الشرط `age >= 13`، سيقوم بطباعة "You are a teenager!".
- إذا كانت جميع الشروط السابقة خاطئة، سيقوم بطباعة "You are a child!".

---

#### استخدام العمليات المنطقية مع `if`

بايثون تدعم استخدام التعابير المنطقية (Logical expressions) مثل `and` و `or` لدمج عدة شروط في عبارة `if` واحدة.

##### مثال:

```python
grade = 85

if grade >= 90:
    print("Excellent")
elif grade >= 80 and grade < 90:
    print("Very Good")
elif grade >= 70 and grade < 80:
    print("Good")
else:
    print("Needs Improvement")
```

في هذا المثال:
- إذا كانت الدرجة (`grade`) 90 أو أكثر، سيقوم البرنامج بطباعة "Excellent".
- إذا كانت الدرجة بين 80 و 89، سيقوم بطباعة "Very Good".
- إذا كانت الدرجة بين 70 و 79، سيقوم بطباعة "Good".
- إذا كانت الدرجة أقل من 70، سيقوم بطباعة "Needs Improvement".

---

#### العمليات المنطقية: `and` و `or`

يمكنك دمج الشروط باستخدام العمليات المنطقية التالية:

- **`and`**: يتحقق الشرط إذا كانت جميع الشروط صحيحة.
- **`or`**: يتحقق الشرط إذا كان أي من الشروط صحيحًا.

##### مثال لاستخدام `and`:

```python
a = 200
b = 33
c = 500

if a > b and c > a:
  print("Both conditions are True")
```

##### مثال لاستخدام `or`:

```python
a = 200
b = 33
c = 500

if a > b or a > c:
  print("At least one of the conditions is True")
```

---

#### العملية المنطقية `not`

الكلمة المفتاحية `not` تُستخدم لعكس نتيجة الشرط.

##### مثال:

```python
a = 33
b = 200

if not a > b:
  print("a is NOT greater than b")
```

---

#### التداخل في العبارات الشرطية: `Nested If`

يمكنك وضع عبارة `if` داخل عبارة `if` أخرى. هذا يُعرف بالتداخل (Nesting) وهو مفيد للتحقق من شروط متداخلة.

##### مثال:

```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

في هذا المثال، نتحقق أولاً من أن `x` أكبر من 10. إذا كان الشرط صحيحًا، يتم تنفيذ كود آخر يتحقق مما إذا كان `x` أكبر من 20.

---

#### المسافات البادئة (Indentation)

بايثون تعتمد بشكل كبير على المسافات البادئة لتحديد نطاق الأكواد. المسافات البادئة هي المسافات الفارغة في بداية السطر، وهي تحدد الكود الذي يتبع عبارات التحكم مثل `if`.

##### مثال على خطأ بسبب عدم وجود مسافات بادئة:

```python
a = 33
b = 200

if b > a:
print("b is greater than a")  # هذا الكود سيتسبب في حدوث خطأ
```

في المثال أعلاه، عدم وجود المسافات البادئة قبل `print` سيتسبب في حدوث خطأ لأن بايثون تتوقع أن يكون الكود الذي يلي `if` مزاحًا بمسافة بادئة.

---

#### عبارة `pass`

في بعض الأحيان، قد تحتاج إلى كتابة عبارة `if` بدون تنفيذ أي كود. في هذه الحالة، يمكنك استخدام العبارة `pass` لتجنب حدوث أخطاء.

##### مثال:

```python
a = 33
b = 200

if b > a:
  pass  # لا يتم تنفيذ أي شيء هنا
```

---

#### نصائح حول كتابة العبارات الشرطية

- **التعليقات (Comments)**: يمكنك استخدام التعليقات (`#`) لتوضيح الكود الخاص بك. هذا يساعد في فهم الكود ومراجعته لاحقًا.
  
- **تعابير منطقية معقدة (Complex Logical Expressions)**: يمكنك دمج شروط متعددة باستخدام الأقواس لتنظيم الأولويات داخل العبارات الشرطية.

##### مثال:

```python
x = 5
y = 10
z = 15

if (x < y or y < z) and z > x:
    print("The condition is True")
```

في هذا المثال، سيتم تنفيذ الطباعة فقط إذا تحقق الشرط المركب بالكامل.


عند استخدام عبارة `if` في بايثون، يمكن أن تحدث بعض الأخطاء الشائعة. إليك بعضًا منها:

### 1. **نسيان النقطتين (:)**
   - يجب أن تنتهي عبارة `if` بالنقطتين.
   ```python
   if x > 5  # خطأ
       print("x is greater than 5")
   ```



```error
  File "/cache/c-000000xy92o53woe2q9zepoinm6grk1s.py", line 25
    if x > 5  # خطأ
                      ^
IndentationError: unindent does not match any outer indentation level
```


I'm sorry for the confusion. Here's the corrected explanation:

### 1. **نسيان النقطتين (:)**
   - يجب أن تنتهي عبارة `if` بالنقطتين.
   ```python
   if x > 5:  # صحيح
       print("x is greater than 5")
   ```



```error
  File "/cache/c-000000xy92o53woe2q9zepoinm6grk1s.py", line 25
    if x > 5:  # صحيح
                         ^
IndentationError: unindent does not match any outer indentation level
```

### 2. **عدم التحقق من الأنواع**
   - مقارنة أنواع غير متوافقة يمكن أن تؤدي إلى أخطاء.
   ```python
   x = "5"
   if x > 3:  # خطأ
       print("x is greater than 3")
   ```



```error
  File "/cache/c-000000xy92o53woe2q9zepoinm6grk1s.py", line 25
    x = "5"
           ^
IndentationError: unindent does not match any outer indentation level
```


Here's the corrected explanation:

### 2. **عدم التحقق من الأنواع**
   - تأكد من أن الأنواع متوافقة عند المقارنة.
   ```python
   x = "5"
   if int(x) > 3:  # تحويل x إلى عدد صحيح
       print("x is greater than 3")
   ```



```error
  File "/cache/c-000000xy92o53woe2q9zepoinm6grk1s.py", line 25
    x = "5"
           ^
IndentationError: unindent does not match any outer indentation level
```
---

#### تمرينات

لتحسين فهمك لعبارات `if` في بايثون، حاول تنفيذ التمرينات التالية:

1. **تحقق من زوجية أو فردية الرقم**: اكتب برنامجًا يطلب من المستخدم إدخال رقم، ثم يتحقق مما إذا كان الرقم زوجيًا أو فرديًا باستخدام عبارة `if`.
   
2. **تقييم درجات الطالب**: اكتب برنامجًا يقيم درجة الطالب بناءً على إدخال المستخدم ويطبع النتيجة المناسبة (ممتاز، جيد جداً، جيد، أو مقبول).
   
3. **تحديد الفئة العمرية**: اكتب برنامجًا يحدد الفئة العمرية للمستخدم بناءً على العمر المدخل (طفل، مراهق، بالغ).

---

#### الخلاصة

عبارات الشرط `if`، `elif`، و `else` توفر طريقة قوية للتحكم في تدفق برامجك بناءً على شروط معينة. فهم كيفية استخدام هذه العبارات بشكل فعال سيمكنك من كتابة برامج بايثون معقدة وفعالة. تأكد من ممارسة كتابة الأكواد واختبارها بنفسك لتحقيق أفضل فهم لهذه المفاهيم.

---

**ملاحظة**: جرب الأمثلة والتمارين بنفسك لتكتسب مهارة
