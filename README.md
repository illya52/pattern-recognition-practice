# Мініпроєкт: Порівняння класичних моделей класифікації

## Структура проєкту
- `data/heart_disease.csv` — початковий набір даних.
- `notebooks/PR04_Прізвище_Імя.ipynb` — головний Notebook з усім кодом (ПР4-7).
- `models/best_classifier.joblib` — збережений фінальний Pipeline.
- `reports/` — результати крос-валідації та фінального тестування.

## Результати експериментів
- **Основна метрика:** F1-міра (для позитивного класу 1).
- **Найкраща модель:** k-NN (Параметри: k=9, metric=manhattan).
- **Результати на Test:** 
  - Accuracy: 0.7541
  - F1-Score: 0.8000
  - ROC-AUC: 0.8869

## Як використовувати модель
```python
import joblib
model = joblib.load('models/best_classifier.joblib')
predictions = model.predict(new_data)
```