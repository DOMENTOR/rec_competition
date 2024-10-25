# rec_competition

## Состав команды The Boys (Реал Мадрид):
- Буффонище: **Исмаилов Мурад** (ALS-модель + генерация фичей)
- Лотераль: **Имайкин Егор** (Item2Item модель + модели topPopular)
- Скрытый форвард: **Лебедев Никита** (User2User модель + тюнинг BERT'а: лучший скор)
- Плеймейкер: **Труфанов Дмитрий** (KNN-модель, kmeans-модель + построение градиентного бустинга)
- Золотой запасной: **Смирнов Арсений** (Кастомная модель BERT + итоговая модель BERT-replay без тюнинга)
</br>

## Структура проекта:</br>
Папка *Transformers*</br>

- ноутбук с построением, обучением, инференсов модели `BERT4Rec` из библиотеки `Replay`
- итоговая модель `RecommenderBERTModelv9`: **лучший скор 0.2006**
- ноутбук с построением, обучением, инференсов модели кастомного `BERT4Rec`, основанного на дообучении bert-base
- данные для обучения
</br>

Ноутбук *comp_recsys_base_ML.ipynb*</br>

- построение, обучение, инференс, оптимизация моделей кандидатов: `KNN`, `Kmeans`, `TopPopular`, `Item2Item`, `User2User`, `ALS`
- генерация дополнительных фичей для бустинга
- формирование итогового датафрейма
- построение, обучение, инференс, оптимизация модели `CatBoostClassifier`
</br>
Данные для обучения *hw1/hse-rec-sys-challenge-2024*
</br>

## Результаты

`CatBoostClassifier` показал результат на уровне `baseline4`.</br>

Кастомная `Bert-based` модель показала результат на уровне `baseline3`.</br>

Итоговая затюненая модель `RecommenderBERTModelv9` показала результат `выше 0.2`.
