---
title: C
localeTitle: C
---
# مرحبا بالعالم! - برنامج C الأول الخاص بك

## الحصول على أقصى استفادة من هذه الدورة

تأكد من أنك مرتاح مع جميع المفاهيم الموجودة في هذا الجزء من الدليل قبل الانتقال. يعد تشغيل برنامجك الأول أمرًا مهمًا لأنه سيتيح لك المتابعة مع الأمثلة ، وهو أمر جيد آخر للقيام بالممارسة يجعله مثاليًا! سيكون للمفاهيم التي قد تكون مربكة تعليقًا يربط ملحقًا. إذا لم تفهم مفهومًا ، فتأكد من الرجوع إلى الملحق لمزيد من المعلومات.

## هدف الدورة

أهداف هذه الدورة هي تدريس لغة C للمبتدئين. من الناحية المثالية ، شخص ما لم يسبق له أن لمس لغة كمبيوتر من قبل سيمكنه معرفة C باتباع هذه الأدلة. ومع ذلك ، فإنها ستظل مفيدة للمبرمجين الأكثر خبرة من خلال تضمين ملخص في نهاية كل مقالة. على الرغم من أن المحتوى الذي يتم تدريسه هنا قابل للتحويل إلى وحدات التحكم الدقيقة مثل Arduino ، إلا أنه ليس محور هذا الدليل.

## ما هو C؟

ج هي لغة برمجة عامة الغرض اخترعها دنيس ريتشي بين عامي 1969 و 1973 في مختبرات بيل. منذ ذلك الحين ، تم استخدامه لإنشاء أشياء مثل Linux Kernel ، والذي يسمح للبرامج بالتفاعل مع الأجهزة على أنظمة التشغيل المستندة إلى Linux. يمكنه القيام بذلك ، وعمليات أخرى منخفضة المستوى ، لأنه صُمم ليكون قريبًا جدًا من رمز الماكينة بينما لا يزال قابلاً للقراءة. وبسبب هذا ، فإنه يوفر الوصول المباشر إلى ذاكرة الكمبيوتر والأجهزة. وهذا يجعله مفيدًا جدًا في تطبيقات الأجهزة والروبوتات حيث يكون الوصول إلى هذه الميزات سريعًا أمرًا مهمًا. ج ، مثل لغات أخرى منخفضة المستوى ، يتطلب تجميع. تأخذ عملية التجميع رمز C الذي يمكن قراءته بواسطة شخص وتحويله إلى كود يمكن قراءته وتنفيذه بواسطة الكمبيوتر. يتطلب التجميع مترجمًا ، والذي يمكن استخدامه إما من سطر الأوامر أو يمكن استخدامه في بيئة تطوير متكاملة (IDE).

إذا كنت تفضل استخدام سطر الأوامر ، ففكر في `gcc` . يمكن العثور عليه افتراضيًا على أنظمة التشغيل GNU + Linux وعلى Mac ، ويسهل الوصول إليه على Windows. للمبتدئين ، ومع ذلك ، قد يكون وجود بيئة تطوير متكاملة أكثر راحة. فكّر في CodeBlocks أو Xcode إذا كنت مهتمًا بالقدرة على كتابة التعليمات البرمجية وتشغيلها من واجهة المستخدم الرسومية.

الآن بعد أن أصبحت لديك هذه الخلفية ، دعنا نبدأ بالبرنامج "Hello، World". "Hello، World" هي طريقة تقليدية لبدء استخدام لغة: فهي تُظهر أننا نستطيع كتابة التعليمات البرمجية وتشغيلها ، لذا فهي مكان جيد للبدء!

## مرحبا العالم في C

```C
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
    return 0;
}
``` 

دعونا كسر هذا البرنامج لأسفل خطوة بخطوة.

الأول هو `#include` :

```C
#include <stdio.h> // This is called preprocessor directives
``` 

هذه تعليمات إلى المحول البرمجي للعثور على مجموعة من ملفات الرأس وتضمينها. تحتوي ملفات الرأس على تعليمات برمجية إضافية يمكننا استخدامها. في هذه الحالة ، تم إرشاد المحول البرمجي لتضمين `<stdio.h>` ، والذي يحتوي على جميع أنواع الوظائف المفيدة مثل `printf()` . يمكننا أيضا أن يكتب ذلك ك `#include"stdio.h"` . سنتطرق إلى التفاصيل المتعلقة بالوظائف التي يتم إجراؤها لاحقًا ، ولكن في الوقت الحالي تذكر فقط أن إحدى الوظائف هي مجموعة من الرموز التي يمكننا استخدامها.

```C
int main(void)
{
}
``` 

هذا الرمز يعلن الوظيفة الرئيسية. وتتمثل المهمة الرئيسية الخاصة ، وسوف تحصل دائما على الدعوة ودائما هو الجزء الرئيسي من البرنامج. إذا لم يكن هذا في برنامجك ، فلا يمكن تشغيل البرنامج ولن يتم ترجمته.

إن بدء تعريف الدالة مع `int` يعني أن هذه الدالة ستعطي قيمة `int` عندما يتم تشغيلها من خلال كودها ، فهذا ناتج هذه الدالة. `int` هو نوع بيانات "الأعداد الصحيحة" ، والأعداد الصحيحة عبارة عن أرقام كاملة مثل -3 أو 0 أو 18. لذا فنحن نعرف أن هذا الكود سيتم تشغيله ، وعندما يتم ذلك ، سوف يعطينا رقمًا صحيحًا. حسب الاصطلاح ، هذا العدد الصحيح هو 0.

التالي هو `main` . `main` هي اسم هذه الوظيفة ، وكما تعلمتم في وقت سابق ، من المهم أن يكون لديك وظيفة `main` لأن برنامجك لن يعمل بدونه. يتبع `main` `(void)` . هذا يخبر المترجم أن هذه الوظيفة لا تأخذ أي معلمات ، وهذا يعني أنه لا يوجد لديه مدخلات.

قد لا يكون هذا منطقيًا في الوقت الحالي ، ولكنك ستتعلم المزيد عن هذا الأمر عند بدء القراءة عن الوظائف في C لاحقًا. الآن ، تذكر فقط أن `main` مطلوب لبرنامج C ، ولا يأخذ أي إدخال ، ويعطي رقمًا كخرج.

وأخيرًا ، هناك الأقواس: `{` و `}` . هذه علامة بداية ونهاية الدالة. يمثل القوس المجعد المفتوح ( `{` ) البداية ، ويمثل قوس الإغلاق المجعد ( `}` ) النهاية. كل شيء بين الاثنين داخل الوظيفة.

الآن دعونا ننظر إلى اللحم من البرنامج:

 `    printf("Hello, World!\n"); 
` 

`printf` هي دالة تأخذ النص وتطبعه على الشاشة. تشير الأقواس إلى المعلومات التي نريد أن تأخذها وظيفة `printf` وطباعتها على الشاشة. نوضح أن هذا هو سلسلة نريد طباعتها عن طريق محاذاتها بين علامتي اقتباس مثل "هذا".

لاحظ \\ n الموجود داخل علامات التنصيص- يخبر هذا عن وظيفة `printf` لطباعة سطر جديد. الخط الجديد هو ما يتم طباعته عندما تضغط على إدخال على لوحة المفاتيح. بدون إخبار C بشكل صريح بطباعة سطر جديد ، ستتم طباعة كل شيء على نفس السطر.

وأخيراً ، يتم إتمام العبارة printf () بفاصلة منقوطة ( `;` ). هذا يدل على أن هذا الخط من الشفرة قد انتهى. بدون ذلك ، لا يعرف المترجم أين ينتهي سطر واحد ويبدأ آخر ، لذلك من المهم تضمينه.

ينتهي البرنامج بعبارة عودة:

```C
return 0;
``` 

هذا يدل على أن الوظيفة قد انتهت وأنه يجب أن تنتهي بإعطاء قيمة 0 إلى أي مما جعلها تعمل. عندما تقوم بتشغيل التعليمات البرمجية على جهاز الكمبيوتر الخاص بك ، فمن الجيد أن يكون ذلك لأنه يسمح للبرامج الأخرى بالتفاعل مع جهازك بطريقة أفضل.

كما كان من قبل ، ينتهي هذا السطر بفاصلة منقوطة للإشارة إلى اكتمال الخط.

## تجميع وتشغيل

يمكنك حفظ ملف hello world الخاص بك كما تريد ، ولكن يجب أن ينتهي بامتداد الملف .c. في هذا المثال ، تم تسمية الملف "helloworld.c" ، لأن هذا هو اسم واضح بملحق الملف .c.

هناك العديد من الطرق لتجميع والحصول على كود C تعمل على جهاز الكمبيوتر الخاص بك. وهنا عدد قليل:

#### تجميع وتشغيل من سطر الأوامر مع GCC

إذا كنت تقوم بتشغيل Mac أو GNU + Linux ، فهذا يعني أنك قد قمت بالفعل بتثبيت GCC.

لتشغيل برنامج C ، يجب أن يتم تجميعها. لكي يتم التحويل من سطر الأوامر باستخدام gcc ، قم بتشغيل الأمر التالي من المحطة الطرفية الخاصة بك:

```shell
gcc -o helloworld ./helloworld.c
``` 

`gcc` هو Gnu C Compiler ، وسوف يقوم بتجميع الملف C الذي نعطيه إلى برنامج يمكن تشغيله بواسطة الكمبيوتر.

`-o helloworld` يخبر مجلس التعاون الخليجي أنك تريد أن يكون الملف الذي تم تجميعه (الناتج من gcc) ملفًا يسمى "helloworld". الجزء الأخير من الأمر يخبر دول مجلس التعاون الخليجي حيث يمكن العثور على ملف C المطلوب تجميعه. إذا لم تكن راضيًا عن التنقل من سطر الأوامر ، فستكون هذه الخطوة صعبة ، ولكن هذا أمر جيد - من السهل تعلمه والعودة إليه ، أو يمكنك تجربة من بيئة تطوير متكاملة (IDE).

بمجرد تجميعها ، قم بتشغيل الأمر التالي:

```shell
./helloworld
``` 

إذا سار كل شيء بشكل جيد ، يجب أن ترى `Hello, World!` المطبوعة على الشاشة.

#### تجميع وتشغيل C مع CodeBlocks

[يمكن تنزيل Codeblocks من هنا.](http://www.codeblocks.org/downloads/26) جعل برنامج جديد مع `file` -> `new` -> `file` المصدر، حدد C / C ++، حدد C كلغة الخاص بك، ثم قم بنسخ فوق النص helloworld.c أن تقرأ من خلال وقت سابق. ترجمة وتشغيل التعليمة البرمجية باستخدام `Build` -> `Build and Run` .

#### تجميع وتشغيل C مع Xcode

[يمكن تنزيل Xcode من هنا.](https://developer.apple.com/xcode/)

#### تجميع وتشغيل C مع Dev-C ++

[يمكن تنزيل Dev-C ++ من هنا.](https://sourceforge.net/projects/orwelldevcpp/) أنشئ برنامجًا جديدًا `file` -> `new` -> `Source File` ، ثم انسخ النص helloworld.c الذي تقرأه سابقًا ثم احفظ الملف مع `file` -> `save As` as hello.c ، ثم ترجم الشفرة وقم بتشغيلها `Execute` -> `Compile & Run` .

# قبل أن تذهب ...

## مراجعة

*   C لغة مشتركة للغة البرمجة.
*   تم استخدام C لإعادة تنفيذ نظام التشغيل Unix.
*   C مفيد لأنه صغير وسريع ولديه إمكانية الوصول إلى العمليات منخفضة المستوى. ولهذا السبب ، يتم استخدامه كثيرًا في الروبوتات وأنظمة التشغيل والإلكترونيات الاستهلاكية ، ولكن ليس في أشياء مثل صفحات الويب.
*   يحتوي برنامج AC على بعض الأجزاء المهمة:
*   بيان التضمين ، الذي يخبر المترجم C بمكان العثور على كود إضافي سيتم استخدامه في البرنامج.
*   الوظيفة الرئيسية ، حيث يتم تنفيذ الكود أولاً ويلزم للترجمة.
*   الاشياء داخل هذه الوظيفة الرئيسية التي سيتم تنفيذها ، بما في ذلك بيان العودة الذي يغلق البرنامج ويعطي قيمة للبرنامج الذي يطلق عليه.
*   يحتاج C إلى أن يتم تجميعه ليتم تشغيله.
*   يمكن استخدام C للوصول إلى عناوين أجهزة محددة وتنفيذ نوع punning لتطابق متطلبات الواجهة المفروضة من الخارج ، مع انخفاض وقت التشغيل على موارد النظام.