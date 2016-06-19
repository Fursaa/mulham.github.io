---
layout: post
date: 2016-06-18
title: سلسلة دروس SQL|عمليات AND & OR
---

الفهرس :

[الدرس الأول : التعريف بـ SQL](intro)

[الدرس الثاني : بناء SQL](build)

[الدرس الثالث : تصريح SELECT](select)

[الدرس الرابع : تصريح تحديد الاختلاف في SQL](select-distinct)

[الدرس الخامس : عبارة WHERE في SQL](where)

الدرس السادس : عمليات AND & OR في SQL

[الدرس السابع : دالة ORDER BY في SQL](order-by)

[الدرس الثامن: تصريح INSERT INTO في SQL](insert-into)

[الدرس التاسع: تصريح UPDATE في SQL](update)

[الدرس العاشر: تصريح DELETE في SQL](delete)

*****************

تستخدم عمليات AND (و) ، OR (أو) لتشريح (فلترة) التسجيلات بناء على أكثر من شرط واحد .


عمليات AND & OR في SQL 


عملية AND تعرض التسجيل إذا كان كلاً من الشرط الأول والشرط الثاني محققين

عملية OR تعرض التسجيل اذا كان الشرط الأول أو الشرط الثاني فقط محقق ، أي اذا تحقق أحد الشرطين فقط .

* Toc
{:toc}


**استعراض قاعدة بيانات**


سنستخدم قاعدة البيانات المعروفة جيداً : Northwind


في الأسفل تحديد من جدول الزبائن Customers


![customers](/assets/customers.png)

# مثال على عملية AND


تصريح SQL التالي يحدد جميع الزبائن من دولة Germany و مدينة Berlin ضمن جدول الزبائن


        SELECT * FROM Customers

        WHERE Country='Germany'

        AND City='Berlin';

# مثال على عملية OR


تصريح SQL التالي يحدد جميع الزبائن من مدينة Berlin أو مدينة München ضمن جدول الزبائن


        SELECT * FROM Customers

        WHERE City='Berlin'

        OR City='München';


# اجتماع AND & OR


يمكنك أيضاً جمع AND و OR في تصريح واحد (استخدم الأقواس لتشكيل تعبيرات مركبة )


تصريح SQL التالي يحدد جميع الزبائن من دولة Germany والمدينة يجب أن تكون مساوية لـ Berlin أو München ضمن جدول الزبائن .

        SELECT * FROM Customers

        WHERE Country='Germany'

        AND (City='Berlin' OR City='München');


التالي: [دالة ORDER BY](order-by)