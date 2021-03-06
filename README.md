# Автоматизированный алгоритм обезличивания данных
# Команда Legaltech
## Модель для задачи конкурса Лидеры Цифровой Трансформации
Модель алгоритма автоматизированной обработки и обезличивания персональных данных (ФИО) в .pdf файлов и .jpeg изображений.

# Структура
Алгоритм модели представляет собой структуру состоящую из следующих блоков:
  1. Чтение файла
  2. Обработка .pdf-файла (преобразование файла в .jpeg изображения)
  3. Применение алгоритма Optical Character Recognition (OCR) для распознавания текста с изображения
  4. Применение алгоритма Named-entity recognition (NER) для определения именованных сущностей (конкретно - ФИО)
  5. Размытие обнаруженной информации на исходном изображении
  6. Сохранение полученных изображений

# Технологический стек
Для данной задачи были использованы следующие **Open Source** решения:
  1. Tesseract OCR - https://github.com/tesseract-ocr/tesseract 
  2. Navec и Slovnet (в рамках русскоязычного  NLP инструмента Natasha): 
     https://github.com/natasha/navec 
     https://github.com/natasha/slovnet 

# Предустановка решения
  1. Необходимо скачать все файлы с репозитория
  2. Установить скаченные зависимости 
    ```
    pip install -r requirements.txt
    ```
  3. Установить Tesseract OSR: https://digi.bib.uni-mannheim.de/tesseract/tesseract-ocr-w64-setup-v5.0.0-alpha.20210811.exe
  4. Переместить **Tesseract-OCR** каталог в директорию с проектом
  5. Скачать языковые пакеты **Natasha**:
    https://storage.yandexcloud.net/natasha-navec/packs/navec_hudlit_v1_12B_500K_300d_100q.tar
    https://storage.yandexcloud.net/natasha-slovnet/packs/slovnet_ner_news_v1.tar
  6. Поместить языковые пакеты в директорию с проектом
  7. Распаковать архив poppler в директорию с проектом
  8. Создать папку output (туда будет выгружен итоговый результат работы алгоритма)
  
# Запуск решения
  Для того, чтобы запустить решение из командной строки необходимо выполнить следующую команду:
  ```
  main_restricted.py \\путь к файлу\\
  ```
# Дополнительные сведения
Файл poppler необходим для преобразования .pdf файла в .jpeg 
  
