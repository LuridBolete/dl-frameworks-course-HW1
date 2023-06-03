# dl-frameworks-course-HW1

Что сделано

Код реализован в polars.

Датасет разделен на train и test в соотношении 70/30.

Обучен CatBoostRegressor с гиперпараметрами по умолчанию: 
при этом была получена точность предсказаний RMSE=0.3488.

Для обучения регрессора были использованы признаки, полученные 
из TfidfVectorizer (sklearn.feature_extraction.text).

Далее был произведен подбор гиперпараметров для модели
с помощью Optuna. За счет этого удалось улучшить точность
предсказаний до RMSE=0.3479
При этом были рассмотрены следующие гиперпараметры:
  - 'n_estimators'
  - 'penalties_coefficient',
  - 'learning_rate',
  - 'subsample',
  - 'min_child_samples',
  - 'max_depth', 
  - 'l2_leaf_reg',
  - 'model_size_reg'

По результатам работы Optuna'ы представлена визуализация.

Настроен DVC-репозиторий.

Подготовлен summary_report.
