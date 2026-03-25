# Named Entity Recognition на датасете CoNLL-2003

# Стек
Python, PyTorch, Hugging Face Transformers, BERT/DistilBERT, BiLSTM, BiLSTM+Attention, scikit-learn, pandas, NumPy, TensorBoard

# Описание проекта
Данный проект посвящен реализации и сравнительному анализу архитектур для задачи Named Entity Recognition (NER) на датасете CoNLL-2003. 

# Реализованы:
- BiLSTM (классическая RNN архитектура)
- BiLSTM+Attention (с механизмом внимания)
- BERT/DistilBERT (трансформерные модели)
- Кастомная предобработка с фильтрацией словаря

Проект включает загрузку CoNLL-2003, обучение моделей и оценку по метрикам точности.

# Цель проекта
Создать эффективные модели NER для распознавания сущностей (PER, LOC, ORG, MISC) и сравнить:

- RNN архитектуры (BiLSTM vs BiLSTM+Attention)

- Трансформеры против классических методов

- Влияние предобработки на качество и скорость

# Основные компоненты системы
Датасет: CoNLL-2003 (train/valid/test) в BIO формате

# Модели:

- BiLSTM
- BiLSTM с self-attention
- Предобученные BERT/DistilBERT

# Обучение:
- Custom DataLoader с padding
- Мультиметрики (accuracy, F1 micro/macro/weighted)
- Оценка: compute_metrics с sklearn

# Используемые данные
CoNLL-2003 English NER (~20k предложений, 9 классов)

# Результаты и выводы
Реализованы три архитектуры с полной оценкой метрик. Трансформеры демонстрируют превосходство над RNN. BiLSTM+Attention дает прирост над vanilla BiLSTM.
