# WiFi_Hack 
# t.me/Master_X_Cha

# مقدمة 
تم تطوير هذه الأداة بلغة Python بهدف اكتشاف الشبكات اللاسلكية القريبة وتجربة الاتصال بها عبر كلمات مرور محددة مسبقًا. تستفيد الأداة من مكتبة Scapy لاكتشاف الشبكات اللاسلكية، ومن أداة nmcli الخاصة بإدارة الاتصالات اللاسلكية على نظام Linux لتجربة الاتصال بالشبكات. تساعد هذه الأداة المستخدمين في اكتشاف الشبكات وتقييم قوة كلمات المرور من خلال قائمة تخمينات، وتستهدف في الأساس أغراض اختبار الاختراق وتقييم الأمان.

# شرح 
1. اكتشاف الشبكات اللاسلكية: تبدأ الأداة بعملية مسح لالتقاط الشبكات المتاحة باستخدام واجهة الشبكة التي يتم إدخالها، وتعرض للمستخدم قائمة بالشبكات التي تم اكتشافها، بما في ذلك اسم الشبكة (SSID) والعنوان الفريد (BSSID).


2. اختيار الشبكة والتخمين: بعد اكتشاف الشبكات، يُمكن للمستخدم اختيار شبكة معينة لمحاولة الاتصال بها عبر كلمات مرور من ملف خارجي.


3. محاولة الاتصال: تحاول الأداة الاتصال بالشبكة المحددة باستخدام كلمات المرور الموجودة في ملف التخمين. تقوم بمحاولة الاتصال حتى تجد كلمة المرور الصحيحة أو تنتهي من كل الكلمات في الملف.

# طريقة استخدامها 
1. بيئة Linux: الأداة تعتمد على nmcli وscapy اللتين تعملان على Linux.


2. صلاحيات الجذر: يتطلب تشغيل الأداة باستخدام صلاحيات الجذر للوصول إلى بطاقة الشبكة ووضعها في وضع المراقبة.


3. ملف كلمات المرور: يجب أن يحتوي على قائمة بكلمات المرور، كل واحدة في سطر مستقل.


# خطوات التشغيل

فى البداية حمل الاداة بالامر: 
```
git clone https://github.com/DataWhisperers1/WiFi_Hack.git
```

1. تثبيت المكتبات اللازمة (إذا لم تكن مثبتة):
```
pip install scapy
```


2. تشغيل الأداة باستخدام صلاحيات الجذر:
```
sudo python3 wif-fi.py
```


3. إدخال واجهة الشبكة: عند تشغيل الأداة، سيطلب منك إدخال اسم واجهة الشبكة (مثل wlan0). تأكد من أنك في وضع المراقبة.


4. إدخال ملف كلمات المرور: سيُطلب منك إدخال اسم الملف الذي يحتوي على كلمات المرور (مثال: passwords.txt).


5. اختيار الشبكة: بعد اكتشاف الشبكات، ستظهر قائمة بها، ويمكنك إدخال رقم الشبكة التي تريد محاولة الاتصال بها.


6. التخمين التلقائي: تبدأ الأداة بمحاولة الاتصال بكلمات المرور في الملف، واحدة تلو الأخرى، حتى يتم العثور على كلمة المرور الصحيحة.



# مثال على كيفية استخدام الأداة
```
$ sudo python3 wi-fi.py
مرحبًا بك في أداة اكتشاف الشبكات!
أدخل اسم واجهة الشبكة (مثل wlan0): wlan0
أدخل اسم ملف كلمات المرور (مثل passwords.txt): passwords.txt
بدء المسح عن الشبكات...

تم اكتشاف شبكة: SSID: MyNetwork, BSSID: 00:11:22:33:44:55

اختر شبكة للاتصال:
1: MyNetwork (BSSID: 00:11:22:33:44:55)
أدخل رقم الشبكة التي تريد الاتصال بها: 1
محاولة الاتصال بشبكة: MyNetwork باستخدام كلمات المرور من الملف...
```

# ملاحظة هامة

استخدام هذه الأداة يجب أن يكون لأغراض تعليمية واختبار أمني مشروع فقط، وعدم استخدامها على شبكات ليس لديك إذن بالاتصال بها، حيث يعتبر هذا غير قانوني ويعرضك للمسؤولية القانونية.
