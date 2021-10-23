# Автоматизированный алгоритм обезличивания данных
# Команда Legaltech
## Модель для задачи конкурса Лидеры Цифровой Трансформации
Модель алгоритма автоматизированной обработки и обезличивания персональных данных (ФИО) в .pdf файлов и .jpeg изображений.

# Структура
Алгоритм модели представляет собой структуру состоящую из следующих блоков:
  1. Чтение файла
  2. Обработка .pdf-файла (преобразование файла в .jpeg изображения)
  3. Применеие алгоритма Optical Character Recognition (OCR) для распознавания текста с изображения
  4. Применеие алгоритма Named-entity recognition (NER) для определения именованных сущеностей (конкретно - ФИО)
  5. Размытие обнаруженной информации на исходном изображении
  6. Сохранение полученных изображений

# Технологический стек
Для данной задачи были использованы следующие **Open Source** решения:
  1. Tesseract OCR - https://github.com/tesseract-ocr/tesseract 
  2. Navec и Slovnet (в рамках рускоязычного NLP инструмента Natasha): 
     https://github.com/natasha/navec 
     https://github.com/natasha/slovnet 

# Как запустить решение
  1. Необходимо скачать все файлы с репозитория
  2. Установить скаченные зависимости 
    ```
    pip install -r requirements.txt
    ```
  3. Установить Tesseract OSR: https://digi.bib.uni-mannheim.de/tesseract/tesseract-ocr-w64-setup-v5.0.0-alpha.20210811.exe
  4. Переместить **Tesseract-OCR** каталог в директорию с кодом
  5. Устновить языковые пакеты **Natasha**:
    https://storage.yandexcloud.net/natasha-navec/packs/navec_hudlit_v1_12B_500K_300d_100q.tar
    https://storage.yandexcloud.net/natasha-slovnet/packs/slovnet_ner_news_v1.tar
  6. Поместить языковые пакеты в директорию с кодом
  7. Создать папку output (туда будет выгружен итоговый результат работы алгоритма)
  
