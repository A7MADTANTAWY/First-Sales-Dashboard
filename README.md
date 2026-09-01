<div dir="rtl">

# 🛒 داشبورد المبيعات — تحليل سوبر ماركت

مشروع **Power BI** متكامل لتحليل مبيعات سوبر ماركت، مبني على بيانات معاملات حقيقية. يعرض المشروع مسار العمل الكامل لتحليل البيانات — من استيراد ملف CSV الخام وبناء نموذج البيانات، حتى التصورات التفاعلية وتقرير رسمي احترافي.

![معاينة الداشبورد](docs/Sales%20Dashboard_page-0001.jpg)

---

## 📌 محتويات الملف

- [نظرة عامة](#نظرة-عامة)
- [الـ Filters — عوامل التصفية](#الـ-filters)
- [الـ KPI Cards — أهم الأرقام](#الـ-kpi-cards)
- [تحليل الـ Visuals بالتفصيل](#تحليل-الـ-visuals)
- [القصة الكاملة للداشبورد](#القصة-الكاملة)
- [شرح الداشبورد في Interview](#الـ-interview)
- [البيانات (Dataset)](#البيانات)
- [هيكل المشروع](#هيكل-المشروع)
- [طريقة التشغيل](#طريقة-التشغيل)
- [المهارات](#المهارات)
- [التقنيات](#التقنيات)
- [خطة التطوير](#خطة-التطوير)
- [الرخصة](#الرخصة)

---

## 📖 نظرة عامة

هذا الريبو يحوّل بيانات معاملات سوبر ماركت الخام إلى **داشبورد مبيعات** قابل للاستخدام، بيجاوب على أسئلة عمل رئيسية مثل:

- إزاي **الإيرادات** و**الأرباح** بتتغير مع الوقت؟
- أنهي **product lines** و**branches/cities** بتجيب أعلى مبيعات؟
- إيه شكل **قاعدة العملاء** (النوع والجنس) وإزاي بيدفعوا؟

**أهم جانب**: الداشبورد مش مجرد أرقام — الهدف منها إننا نطلع **Insights و Business Decisions**: مين أفضل فرع؟ إيه أفضل منتج؟ مين العملاء الأكثر قيمة؟ إمتى الطلب بيزيد؟ وإمتى المبيعات بتقع؟

---

## 🎛️ الـ Filters

الجزء اللي على الشمال عبارة عن **Slicers / Filters**، ودي بتغير كل الـ Visuals في الداشبورد حسب اختيارك.

### Branch
- عندك: `Branch A`، `Branch B`، `Branch C`
- لو اخترت مثلًا `Branch A`، كل الأرقام والرسومات بتتفلتر وتعرض بيانات `Branch A` فقط.

### Month
- عندك: `January`، `February`، `March`
- تقدر تشوف أداء المبيعات في شهر معين.
- مثلًا لو اخترت `February`: `Total Sales` هيتغير ← `Product Sales` هتتغير ← `Sales by Day` هيتغير ← `Sales by Hour` هيتغير... إلخ.

### Payment
- طرق الدفع: `Cash`، `Credit card`، `Ewallet`
- بيدي فرصة تعرف: العملاء بيدفعوا إزاي؟ وتحلل مثلًا هل الـ `Credit card` بيحقق مبيعات أعلى من الـ `Cash`.

### Gender
- `Female` و `Male`
- بيدي فرصة تحلل المبيعات حسب نوع العميل، مثلًا: هل الـ `Female` customers بيعملوا sales أكتر من الـ `Male`؟

---

## 💎 الـ KPI Cards — أهم الأرقام

الجزء العلوي بيدي **Executive Summary** سريع: لو المدير فتح الداشبورد يقدر في ثواني يعرف حالة المبيعات.

| المقياس | القيمة | الشرح |
| --- | --- | --- |
| **Total Sales** | **322.97K** | إجمالي قيمة المبيعات ≈ **322,970** خلال الفترة الموجودة في الداتا. |
| **Total Margin** | **4.76%** | نسبة الربح: من كل 100 جنيه Sales، الشركة بتحقق ≈ **4.76 جنيه** Profit. |
| **Total Profit** | **15.38K** | إجمالي الربح ≈ **15,380** = `Sales − COGS` = `322.97K − 307.59K`. |
| **Total Sold Items** | **6K** | عدد المنتجات المباعة ≈ **6,000**. ده مش عدد الفواتير. |
| **Total COGS** | **307.59K** | تكلفة المنتجات اللي اتباعت (Cost of Goods Sold) ≈ **307,590**. |
| **Average Invoice Value** | **322.97** | متوسط قيمة الفاتورة = `Total Sales ÷ Number of Invoices` = `322.97K ÷ ~1K`. |
| **Average Ratings** | **6.97** | متوسط تقييم المعاملات ≈ **7 من 10**. |

**ملاحظة تحليلية مهمة:** الـ Profit Margin منخفض نسبيًا (4.76%) مقارنة بحجم الـ Sales — ممكن يكون عندك مبيعات كبيرة لكن الـ Margin منخفض.

---

## 🖼️ تحليل الـ Visuals

### 1. Total Sales by City 🗺️
- دي الخريطة في أعلى المنتصف، بتوضح المبيعات حسب المدينة.
- **حجم النقطة = حجم الـ Sales** (نقطة كبيرة ← sales أعلى).
- بيساعدك تجاوب على أسئلة زي: أنهي مدينة بتحقق أكبر Sales؟ فين العملاء الأكثر شراءً؟ هل فيه مدينة محتاجة Marketing أكتر؟

### 2. Sales By Branch 🍩
- Donut Chart في الأعلى، عندك 3 فروع:

| الفرع | المبيعات |
| --- | --- |
| Branch C | **110.57K** |
| Branch A | **106.2K** |
| Branch B | **106.2K** |
| **الإجمالي** | **≈ 322.97K** |

- **الاستنتاج:** `Branch C` هو الأعلى في المبيعات، بينما `A` و `B` قريبين جدًا من بعضهم — مفيش فرق ضخم لكن `C` هو الأفضل.

### 3. Sales By Customer Type 👥
- تقسيم العملاء لنوعين:

| النوع | المبيعات |
| --- | --- |
| Member | **164.22K** |
| Normal | **158.74K** |

- الـ `Members` بيحققوا مبيعات أعلى شوية من الـ `Normal` (≈ 50.8% مقابل 49.2%) والفرق بسيط.
- **سؤال تحليلي:** هل الـ Membership فعلاً بيشجع العميل على الشراء؟ ده ممكن يكون عنوان لتحليل أعمق.

### 4. Top 6 Product Lines Sales 📊
- Bar Chart في المنتصف، بيوضح مبيعات كل Product Line.

| Product Line | المبيعات تقريبًا |
| --- | --- |
| Food and beverages | **56K** |
| Sports and travel | 55K |
| Electronic accessories | 54K |
| Fashion accessories | 54K |
| Home and lifestyle | 54K |
| Health and beauty | **49K** |

- **الأعلى:** `Food and beverages` (56K) — **الأقل:** `Health and beauty` (49K).
- الفرق بين أعلى وأقل product line مش كبير، يعني المبيعات موزعة بشكل متقارب نسبيًا.

### 5. Rating by Product Line ⭐
- هنا مش بنشوف sales — بنشوف **متوسط تقييم العملاء لكل Product Line**.

| Product Line | Rating |
| --- | --- |
| Food and beverages | **7.1** (الأعلى) |
| Fashion accessories | 7.0 |
| Health and beauty | 7.0 |
| Electronic accessories | 6.9 |
| Sports and travel | 6.9 |
| Home and lifestyle | **6.8** (الأقل) |

- **تحليل مهم:** `Food and beverages` عنده أعلى Sales **وأعلى Rating** مع بعض.
- `Health and beauty` Rating كويس (7.0) لكن Sales أقل — **ليه Product Line عنده Rating كويس لكن sales قليلة؟**

### 6. Rating by Branch 🌟
- بيعمل مقارنة متوسط التقييم لكل فرع.

| الفرع | Rating |
| --- | --- |
| Branch C | **7.1** |
| Branch A | 7.0 |
| Branch B | 6.8–6.9 |

- `Branch C` = أعلى Rating **وكمان** أعلى Sales، فبيرتبط بـ **Positive Performance Indicator**.

### 7. Sales by Day 📅
- Area/Line Chart بيوضح المبيعات حسب أيام الأسبوع.

| اليوم | المبيعات تقريبًا |
| --- | --- |
| Saturday | **163K** (الأفضل) |
| Tuesday | 158K |
| Wednesday | 143K |
| Friday | 139K |
| Thursday | 138K |
| Sunday | 133K |
| Monday | **125K** (الأضعف) |

- **مهم:** الأيام مرتبة حسب قيمة المبيعات من الأعلى للأقل، مش بالترتيب الزمني.
- **الاستخدام:** استعد بمخزون وموظفين أكبر قبل `Saturday`، وخطط لرفع المبيعات يوم `Monday`.

### 8. Top Sales Hours ⏰
- المحور الأفقي: `Hour`، والمحور الرأسي: `Count of Invoice ID` — بنقيس **عدد الفواتير في كل ساعة**.
- البيانات من **10 AM → 8 PM**، وأعلى Peak عند **7 PM** تقريبًا (أكبر عدد معاملات)، مع انخفاضات مثلًا عند **5 PM**.
- **معلومة عملية:** تقدر تزوّد الموظفين والـ inventory وتعمل promotions في ساعة الذروة (7 PM).

### 9. Sales by Month 📆
| الشهر | المبيعات تقريبًا |
| --- | --- |
| January | **116K** (الأعلى) |
| February | **97K** (الأقل) |
| March | **109K** |

- **القصة:** `January` قوي 📈 ← `February` انخفاض واضح 📉 ← `March` تحسُّن/Recovery 📈 (لكن لسه أقل من January).

---

## 🧭 القصة الكاملة للداشبورد

لو جمعنا كل الرسومات مع بعض، الداشبورد بتحكي القصة دي:

- 💰 **Sales:** الشركة حققت **322.97K** إجمالي مبيعات.
- 💵 **Profit:** حققت **15.38K** ربح بهامش **4.76%** (منخفض نسبيًا).
- 🏢 **Branch Performance:** `Branch C` هو الأفضل في Sales (**110.57K**) وكمان أعلى Rating.
- 👥 **Customer Performance:** `Members` أعلى من `Normal` قليلًا (**164.22K** vs **158.74K**)، الفرق مش كبير.
- 🛍️ **Product Performance:** أفضل product line هو `Food and beverages` (**56K**) والأقل `Health and beauty` (**49K**) مع فروقات محدودة.
- ⭐ **Customer Satisfaction:** أفضل Rating = `Food and beverages` (**7.1**) والأقل `Home and lifestyle` (**6.8**).
- 📅 **Time Analysis:** أفضل يوم `Saturday`، أضعف يوم `Monday`، وأعلى وقت عدد فواتير ≈ **7 PM**.
- 📆 **Monthly Trend:** `January` الأفضل ← انخفاض قوي في `February` ← Recovery في `March`.

---

## 🎤 الـ Interview

لو هتشرح الداشبورد في مقابلة، تقدر تقول بشكل احترافي:

> *"This dashboard provides an overview of the company's sales performance across branches, customer types, product lines, and time periods. The business generated around 322.97K in total sales with 15.38K in profit and a 4.76% profit margin. Branch C was the highest-performing branch in terms of sales and also had the highest customer rating. Food and beverages was the top-performing product line by sales and rating. From the time analysis, Saturday generated the highest sales, while Monday was the weakest day, and the highest transaction activity occurred around 7 PM. Monthly analysis showed that January had the highest sales, followed by a significant decline in February and a recovery in March."*

**أهم حاجة:** الداشبورد مش هدفها تقول "Sales = 322K" وخلاص — الهدف إنك تطلع منها Insights و Business Decisions.

---

## 🗂️ البيانات (Dataset)

البيانات هي عينة **Supermarket Sales** عامة مشهورة: **3 شهور، 1,000 معاملة (يناير–مارس 2019)** تغطي 3 فروع في ميانمار.

| العمود | الوصف |
| --- | --- |
| `Invoice ID` | معرف المعاملة |
| `Branch` / `City` | موقع البيع |
| `Customer type` | `Member` أو `Normal` |
| `Gender` | جنس العميل |
| `Product line` | فئة المنتج |
| `Unit price` / `Quantity` | سعر الوحدة والكمية |
| `Tax 5%` / `Total` | الضريبة والإجمالي |
| `Date` / `Time` | توقيت المعاملة |
| `Payment` | طريقة الدفع (`Cash`, `Credit card`, `Ewallet`) |
| `cogs` / `gross income` | التكلفة والربح الإجمالي |
| `gross margin percentage` | نسبة الهامش |
| `Rating` | تقييم رضا العميل |

**المصدر:** [Supermarket Sales — Kaggle](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales)

---

## 🗃️ هيكل المشروع

```
First-Sales-Dashboard/
├── data/                             # البيانات الخام
│   └── supermarket_sales.csv
├── reports/                          # تقرير Power BI (قابل للتعديل)
│   └── Sales Dashboard.pbix
├── docs/                             # الوثائق ومعاينة الداشبورد
│   └── Sales Dashboard_page-0001.jpg
├── README.md
└── .gitignore
```

---

## 🚀 طريقة التشغيل

**المتطلبات:**
- **Microsoft Power BI Desktop** (مجاني) لفتح وتعديل ملف `.pbix`.

**الخطوات:**
1. استنسخ الريبو:
   ```bash
   git clone https://github.com/<your-username>/First-Sales-Dashboard.git
   ```
2. افتح **`reports/Sales Dashboard.pbix`** في Power BI Desktop.
3. نموذج البيانات بيتحمّل تلقائيًا — من غير أي إعدادات إضافية.
4. نافش مع الـ visuals، أو اطبع/صدّر إلى PDF.

> عايز نظرة سريعة؟ افتح **`docs/Sales Dashboard_page-0001.jpg`**.

---

## 🧠 المهارات

- استيراد وتنظيف وتشكيل البيانات (Power Query)
- بناء نموذج البيانات والعلاقات
- مقاييس DAX للتجميعات والـ KPIs
- تصميم تقارير تفاعلية وسرد القصة بالبيانات (*Storytelling with Data*)
- تنسيق وتخطيط احترافي

---

## 🛠️ التقنيات

| الأداة | الغرض |
| --- | --- |
| **Power BI Desktop** | بناء النموذج والـ DAX والتصورات |
| **Power Query (M)** | تحويل وتنظيف البيانات |
| **DAX** | مقاييس مخصصة وأعمدة محسوبة |
| **CSV** | مصدر البيانات الخام |

---

## 🗺️ خطة التطوير

- [ ] النشر على **Power BI Service** للمشاركة المباشرة
- [ ] إضافة صفحة **Executive Summary**
- [ ] صفحة **Drill-through** لتفاصيل كل product line
- [ ] أتمتة تحديث البيانات عبر Gateway

---

## 📄 الرخصة

هذا المشروع **لأغراض تعليمية/بورتفوليو** ويستخدم بيانات عينة عامة.

---

</div>
