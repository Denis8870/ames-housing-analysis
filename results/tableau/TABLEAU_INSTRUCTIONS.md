# Інструкція зі створення дашборда в Tableau Public

Файл даних: `ames_tableau.csv` (1460 рядків, 19 колонок).

## 1. Підключення даних
1. Відкрийте Tableau Public Desktop → **Connect → Text file** → оберіть `ames_tableau.csv`.
2. У вікні Data Source перевірте типи: `SaleDate` = Date; `SalePrice`, `PricePerSqFt`, `GrLivArea` = числа (#); `NeighborhoodName`, `AgeGroup`, `SaleCondition` = текст (Abc).
3. Унизу натисніть **Sheet 1**.

## 2. Аркуші (мінімум три)
**Аркуш «Медіанна ціна за районами»**
- Перетягніть `NeighborhoodName` у **Rows**, `SalePrice` у **Columns**.
- Клацніть на `SUM(SalePrice)` → **Measure → Median**.
- Відсортуйте за спаданням (кнопка сортування на панелі зверху).
- Перетягніть `SalePrice` на **Color** (теж Median).

**Аркуш «Динаміка цін»**
- `SaleDate` у **Columns**: клацніть на пілюлю → оберіть **Month** (друга група з назвою Month, пілюля стане зеленою: неперервна).
- `SalePrice` у **Rows** → Median.
- Marks → **Line**. За бажання: клацніть правою на графіку → **Add Reference Line** (Median).

**Аркуш «Ціна і площа»**
- `GrLivArea` у **Columns**, `SalePrice` у **Rows**.
- Меню **Analysis → Aggregate Measures** → зніміть галочку (щоб кожна точка була окремим продажем).
- `AgeGroup` на **Color**, `Id` на **Detail**. Marks → Circle.

**Аркуш «KPI»** (ключові показники)
- Перетягніть `Number of Records` на **Text**. Окремо створіть ще два аркуші (або один із **Measure Values**): `SalePrice` → Median, `PricePerSqFt` → Median.
- Назви: «Кількість продажів», «Медіанна ціна, USD», «Медіанна ціна за кв. фут, USD».

## 3. Фільтри (мінімум два інтерактивні елементи)
1. Перетягніть `YrSold` у **Filters** → **Add all** → OK. Клацніть на пілюлі правою → **Show Filter**. Потім у меню пілюлі: **Apply to Worksheets → All Using This Data Source**.
2. Так само додайте фільтр `SaleCondition` (або `AgeGroup`) і застосуйте до всіх аркушів.
3. Додатково (бонус): у дашборді оберіть аркуш із районами → іконка лійки **Use as Filter**. Клік по району відфільтрує решту.

## 4. Дашборд
1. **Dashboard → New Dashboard**. Розмір: Fixed або Automatic.
2. Перетягніть аркуші: KPI зверху, райони ліворуч, динаміку й «Ціна і площа» праворуч.
3. Перетягніть **Text** з лівої панелі й напишіть назву: «Ринок нерухомості Еймса, 2006–2010» і короткий опис показників. Додайте відображення фільтрів (Show Filter).
4. Перевірте, що фільтр року змінює всі аркуші.

## 5. Публікація
1. **File → Save to Tableau Public As…** → увійдіть у акаунт → вкажіть назву.
2. Відкриється сторінка в браузері: скопіюйте посилання (адресний рядок) і надішліть його.
