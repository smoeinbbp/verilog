# نت‌ها و متغیر‌ها در Verilog

مدارهای منطقی در Verilog با مجموعه‌ای از عناصر منطقی پیوسته و همچنین مجموعه‌ای از عبارات رویه‌ای که رفتار مدار را توصیف می‌کنند، مدل سازی می‌شوند. به اتصالات بین عناصر منطقی مدار ** nets ** و به سیگنال های تولید شده توسط دستورات رویه‌ای برای ذخیره سازی اطلاعات ** variables ** گویند. هر یک از این داده‌ها می‌توانند بصورت تکی \(scalar\) و یا برداری \(vector\) در مدار تعریف شوند.

## نت‌ها

یک**نت**نشان دهنده‌ی یک نود\(گره\) در مدار است. نت ها انواع مختلفی دارند. برای سنتز تنها نت ** wire ** مهم می‌باشد. یکwire \(سیم\) خروجی یک عنصر منطقی را به ورودی عنصر دیگر در مدار متصل می‌کند. همانطور که اشاره شد، این داده می‌تواند بصورت تکی و یا برداری در مدار تعریف شود. برای مثال در شکل ۱۴ سیگنال های نقلی c1، c2 و c3 بصورت تکی هستند که ارتباطات بین ماژول های مدار تمام جمع کننده را برقرار کردند. در شکل ۱۵ سیگنال های نقلی بصورت یک بردار سه بیتی C تعریف شده است. همانطور که مشاهده می‌شود در شکل ۱۴ سیگنال های نقلی از نوعwireتعریف نشده‌اند.دلیل این امر آن است که لازم نیست نت ها را در مدار مشخص کنیم وVerilogتمام سیگنال ها را به طور پیش فرض از نوع نت در نظر می‌گیرد. البته کد زیر را هم که شامل تعریف نت ها می‌باشد، می‌توان در دستورات استفاده نمود:

```
wire c1, c2, c3;
```

در کد شکل ۱۵ لازم است تا C را بصورت بردار تعریف کنیم.در غیر این صورت، کامپایلر Verilog قادر به تشخیص ارتباط بین سیگنال های C\[1\]، C\[2\] و C\[3\] نمی‌باشد از آنجایی که این سیگنال ها از نوع نت می‌باشند، بردار C بصورت wire تعریف شده است.

نوع دیگری از نت ها، نت ** tri ** می‌باشد. این نت مشخص کننده‌ی یک نت سه حالته \(tri-state\) است که نشان می‌دهد یک سیگنال ممکن است علاوه بر مقادیر منطقی0و1، مقدار z امپدانس بالا \(high-impedance\) داشته باشد.

## متغیرها 

یک مدار با استفاده از متغیر ها رفتار خود را توصیف می‌کند. یک**متغیر**می‌تواند در یک بخش از دستورات Veirlog مقدار دهی شود و آن مقدار را تا زمانی که مقدار جدیدی به آن اضافه نشود در خود نگه می‌دارد. متغیر ها به دو دسته‌ی ** reg ** و ** integer ** تقسیم می‌شوند. تمام سیگنال هایی که توسط دستورات رویه‌ای مقدار دهی می‌شوند، باید با استفاده از کلمه کلیدی reg یا integer تعریف شوند. در شکل ۱۷ سیگنال تکی carryout و بردارهای S و C نمونه هایی از متغیر reg هستند. همچنین متغیر نشان دهنده‌ی یک متغیر integer می‌باشد. چنین متغیر هایی برای توصیف رفتار یک مدار مفید هستند.

 

 

