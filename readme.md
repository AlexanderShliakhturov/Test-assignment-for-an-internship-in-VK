**Даный репозиторий содержит решение тестового задания при отборе на стажировку в ВК по направлению DataScience.**  

В задании предложено классифицировать временные ряды на два класса. Для обучения модели классификации предоставлен файл 'train.parquet'. 
В файле 'test.parquet' находится тестовая выборка. Для наблюдений из нее нужно сформировать файл 'submission.scv', в котором будут предсказания вероятности отнесения каждого ряда к положительному классу.  

**В репозитории находятся три ноутбука:**  

`EDA_and_feachure_extraction.ipynb` - в нем находится разведовательный анализ тренировочного датасета, а так же процесс формирования фичей для обучения модели.
В этом файле будут сформированы и записаны в файлы 'feachures_scaled.csv' и 'target.csv' - фичи и таргеты, полученные из 'train.parquet'.  

`Make_model.ipynb` - в этом файле открываются 'feachures_scaled.csv' и 'target.csv' и обучается модель классификации.
После обучения модель записывается в файл 'random_forest_model.joblib'.  

`make_submission.ipynb` - в этом файле открывается тестовый датасет и формируются фичи.
После формирования фичей из файла 'random_forest_model.joblib' загружается обученная прежде модель и делаются предсказания. 
Сделав предсказания, формируется и записывается таблица - 'submission.csv'.  

Для того, чтобы заново проделать все этапы работы, нужно последовательно запустить ноутбуки в том порядке, в котором они описаны выше.
В репозитории уже лежат фичи и таргеты для обучения модели, а так же сама обученная модель.  

Для того, чтобы получить файл 'submission.csv' с результатом работы модели для тестовой выборки, нужно запустить ноутбук 'make_submission.ipynb'.
В нем будут использоваться уже существующие фичи и обученная модель.  

В репозитории есть файл 'requirements.txt', включающий необходимые зависимости для запуска кода.  
