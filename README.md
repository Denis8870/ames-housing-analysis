# Дослідження ринку нерухомості: Ames Housing (2006–2010)

Курсова робота з дисципліни «Мови програмування для аналізу даних»
(Національний університет «Полтавська політехніка імені Юрія Кондратюка»).

## Мета
Визначити, які характеристики будинків і умови продажу формують ціну житла в м. Еймс (штат Айова, США) у 2006–2010 роках.

## Дані
- **Набір:** Ames Housing, версія змагання Kaggle «House Prices – Advanced Regression Techniques».
- **Файл:** `data/raw/train.csv` — 1460 продажів, 81 ознака (включно з `SalePrice`).
- **Опис ознак:** `data/raw/data_description.txt`.
- **Джерело:** https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data
- Первинний автор набору: Dean De Cock (2011), *Ames, Iowa: Alternative to the Boston Housing Data*.

## Технології
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook, Tableau Public.

## Запуск
```bash
git clone https://github.com/Denis8870/ames-housing-analysis.git
cd ames-housing-analysis
pip install -r requirements.txt
jupyter notebook notebooks/analysis.ipynb
```
Усі комірки виконуються послідовно. Шляхи до даних — відносні (від папки `notebooks/`).

## Структура
```
data/raw/        вихідні дані
data/processed/  очищені дані
notebooks/       analysis.ipynb — основний аналіз
src/             допоміжні модулі
results/figures/ графіки
results/exports/ результати обчислень
results/tableau/ матеріали для дашборда
```
