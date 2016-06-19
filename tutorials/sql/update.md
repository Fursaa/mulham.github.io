---
layout: post
date: 2016-06-18
title: سلسلة دروس SQL|تصريح UPDATE
---

الفهرس :


[الدرس الأول : التعريف بـ SQL](intro)

[الدرس الثاني : بناء SQL](build)

[الدرس الثالث : تصريح SELECT](select)

[الدرس الرابع : تصريح تحديد الاختلاف في SQL](select-distinct)

[الدرس الخامس : عبارة WHERE في SQL](where)

[الدرس السادس : عمليات AND & OR في SQL](and-or)

[الدرس السابع : دالة ORDER BY في SQL](order-by)

[الدرس الثامن: تصريح INSERT INTO في SQL](insert-into)

الدرس التاسع: تصريح UPDATE في SQL

[الدرس العاشر: تصريح DELETE في SQL](delete)

*****************


يستخدم تصريح UPDATE لتحديث تسجيلات موجودة مسبقاً في جدول .


* Toc
{:toc}

# بناء تصريح UPDATE


		UPDATE table_name

		SET column1=value1,column2=value2,...

		WHERE some_column=some_value;


> لاحظ عبارة WHERE في تصريح UPDATE !

عبارة WHERE تحدد أي تسجيل أو تسجيلات يجب أن تُحدّث ، إذا قمت بحذف عبارة WHERE ، فسوف تُحدّث جميع التسجيلات! 


# استعراض قاعدة بيانات :



سنستخدم قاعدة البيانات المعروفة جيداً : Northwind


في الأسفل تحديد من جدول الزبائن Customers

![customers](/assets/customers.png)

# مثال على تصريح UPDATE


على فرض أننا نريد تحديث سجل الزبون "Alfreds Futterkiste" لاسم تواصل ContactName ومدينة City جديدين، حينها نستخدم تصريح SQL التالي


		UPDATE Customers

		SET ContactName='Alfred Schmidt', City='Hamburg'

		WHERE CustomerName='Alfreds Futterkiste';

الآن ، سيبدو التحديد من جدول الزبائن على الشكل التالي

![customers3](/assets/customers3.png)

> تحذير! كن حذراً عند تحديث التسجيلات

 فإذا قمت بحذف عبارة WHERE من المثال السابق، كأن تكتب


		UPDATE Customers

		SET ContactName='Alfred Schmidt', City='Hamburg';

حينها ،  سيبدو جدول الزبائن على الشكل

![customers4](/assets/customers4.png)

التالي: [تصريح DELETE](delete)