# Тестовое задание на вакансию Data-Helper
## 1. Базовая работа с python/numpy
Скачайте 10-20 изображений с лицами из интернета какими удобно средствами. <br>
Воспользуйтесь одним из готовых face-detector/face-landmark-detector для того,
чтобы на выбранных изображениях найти лицо и ключевые точки на лице. Можно для
этого взять связку библиотек OpenCV (opencv-python) & dlib (dlib-python). <br>Результат детектирования лица (bbox) & landmarks (points) визуализировать в jupyter-notebook для первых 5-10 картинок.

Задание выполнено в [OneCell_DataHelper.ipynb](https://github.com/MariaNguen/OneCell_DataHelper/blob/main/OneCell_DataHelper.ipynb). Блокнот не отображается в Github, можно посмотреть по [ссылке в Google Colab](https://colab.research.google.com/drive/1UgeUP6jKsJBxMOOI_Xbmx555j_le0U7u?usp=sharing) (где он и был сделан).

## 2. Оценка метрик и валидация моделей
Скачайте датасет с kaggle-соревнования [Kaggle: Facial Keypoints Detection](https://www.kaggle.com/c/facial-keypoints-detection/data)<br>
Задетектируйте при помощи выбранного выше landmark-детектора точки на лицах из
этого датасета и посчитайте метрики для Ground-Truth точек которые эквивалентны
точкам из модели (в opencv 68-point модель, в kaggle разметка для 15-точек. <br>
Подумайте, предложите метрики, которые стоит посчитать для этой задачи. Мы хотим при помощи этих метрик оценить несколько факторов:
- оценить точность детектирования каждой из точек и всех точек в среднем
- оценить точность позиционирования (насколько точки смещаются относительно GT)
для каждой landmark и в среднем

Отберите и визуализируйте (изображение + точки Ground Truth + Predicts) 3-5 изображений с самым высоким качеством детектирования и с самым низким.

Задание выполнено в [OneCell_DataHelper.ipynb](https://github.com/MariaNguen/OneCell_DataHelper/blob/main/OneCell_DataHelper.ipynb). Блокнот не отображается в Github, можно посмотреть по [ссылке в Google Colab](https://colab.research.google.com/drive/1UgeUP6jKsJBxMOOI_Xbmx555j_le0U7u?usp=sharing) (где он и был сделан).

## 3. Работа с инструментами разметки
Мы видим, что модель некоторые точки неверно детектирует на скачанных нами лицах и
мы хотим отправить эти данные на разметку человеком. Для этого мы хотим в инструмент
для разметки данных загрузить изображения и предсказания модели для последующего
исправления людьми. Соответственно в этом задании нужно:
- завести если нет аккаунт на сервисе [supervisely](https://supervise.ly/)
- почитать документацию и разобраться с [SDK/Python-API для supervisely](https://sdk.docs.supervise.ly/)
- написать код для загрузки данных в supervisely (в этом же jupyter-notebook)
- загрузить 5-10 изображений и предсказаний модели в supervisely и вставить
скриншот с работающего сервиса
- замерьте скорость разметки и оцените время разметки с нуля и время доразметки
результатов работы модели

Задание выполнено в [OneCell_DataHelper_Task3.ipynb](https://github.com/MariaNguen/OneCell_DataHelper/blob/main/OneCell_DataHelper_Task3.ipynb).
