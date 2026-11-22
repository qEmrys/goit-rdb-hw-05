# goit-rdb-hw-05

Домашнє завдання з теми 5 курсу Relational Databases for DS: typed-схема Olist у PostgreSQL, feature engineering pipeline через CTE-chain (RFM, cohort_quarter, rolling 30-day AOV, cancellation_rate, preferred_category), recursive CTE для referral chain, Materialized View з REFRESH CONCURRENTLY, EXPLAIN (ANALYZE, BUFFERS), reflection.

## Датасет

Brazilian E-Commerce Public Dataset by Olist (Kaggle `olistbr/brazilian-ecommerce`). Використовуються 5 файлів: customers, orders, order_items, products, sellers.

- Офіційне джерело: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Файли

- `HW5.ipynb` — notebook з output клітинок.
- `data/olist.tar.xz.part00` … `part04` — CSV з Kaggle без змін (ті самі, що в goit-rdb-hw-04), запаковані в tar.xz і розбиті на частини по 3.5 МБ. В архіві також є order_reviews, у цьому ДЗ він не використовується.

## Запуск

Відкрити `HW5.ipynb` у Google Colab → Runtime → Restart and run all.

Notebook сам знаходить дані: спочатку `data/olist/*.csv`, потім частини архіву в `data/`, потім KaggleHub, а якщо Kaggle недоступний, скачує частини архіву з цього репозиторію. PostgreSQL 16 запускається через `pixeltable-pgserver` (`pip install pgserver` на поточному Colab не ставиться).
