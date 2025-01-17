# Тема работы

Исследование особенностей и трендов в музыке с использованием данных Spotify и разработка системы музыкальных рекомендаций.

# Цели работы
1. Изучить основные характеристики музыкальных композиций, представленных в датасете Spotify.
2. Выявить закономерности и тренды в музыкальных данных.
3. Разработать и протестировать несколько подходов к построению системы музыкальных рекомендаций.

# Описание исходных данных

В проекте использован датасет, содержащий информацию о 30 000 треках с платформы Spotify. Данные включают такие параметры, как популярность треков, жанры, темп, танцевальность, энергичность, продолжительность, громкость, а также множество других музыкальных характеристик.

Источник данных: [Kaggle.](https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs)


# Полученные результаты
1. Датасет предварительно обработан, включая удаление пропусков и создание дополнительных признаков, таких как год и месяц выпуска треков.
2. Проведен детальный анализ музыкальных характеристик, включающий визуализацию распределений, выявление корреляций между признаками и изучение тенденций в музыке за последние десятилетия.
    Ключевые тенденции
    1. Энергичность и громкость: Современная музыка становится всё более энергичной, что выражается в увеличении значения показателей energy и loudness. Особенно это заметно с конца 1990-х годов.
    Музыка с высокой энергичностью ассоциируется с быстрыми и яркими жанрами, такими как pop, rap и EDM.

    2. Танцевальность: В последние десятилетия танцевальные треки приобрели большую популярность. Жанры rap и latin лидируют по танцевальности (danceability), что объясняет их высокую востребованность на вечеринках и мероприятиях.

    3. Сокращение продолжительности треков: Анализ показал, что современные треки в среднем короче, чем в предыдущие десятилетия. Это может быть связано с трендом на быстрое потребление контента и популярностью стриминговых платформ.

    4. Популярные жанры: Жанр pop остаётся самым популярным, демонстрируя наивысшие значения популярности (track_popularity). За ним следуют такие жанры, как rap и dance, которые часто используют высокую танцевальность и энергичность для привлечения слушателей.

    5. Позитивное настроение треков: Музыка с высокой валентностью (valence), выражающая позитивные эмоции, такие как радость и веселье, остаётся наиболее востребованной. Большая часть популярных треков написана в мажоре (mode), что подчёркивает предпочтение слушателей к бодрым и весёлым композициям.

    6. Эволюция музыкальных характеристик:

        - До 1970-х годов наблюдаются хаотичные данные, что объясняется ограниченностью информации.
        - С конца 20-го века усилилась роль лирики и танцевальности в треках.
        - Сложные треки с высоким уровнем акустичности постепенно теряют популярность, уступая место более динамичным и электронным композициям.
    
    7. Особенности поджанров:
        - Поджанры, такие как electropop и trap, показывают ярко выраженную популярность среди молодежи, благодаря своим танцевальным ритмам и энергичности.
        - Более медленные и продолжительные треки характерны для жанров, таких как rock и classical, которые сохраняют аудиторию с классическими вкусами.

3. Построено три системы рекомендаций:
    - Косинусная похожесть: алгоритм, основывающийся на вычислении угла между векторами признаков треков. Простой, но эффективный подход.
    - Кластеризация: метод на основе группировки треков с использованием алгоритма K-Means и поиска ближайших соседей внутри кластера.
    - Автоэнкодер: использование нейронной сети для автоматического извлечения скрытых признаков и поиска похожих треков по их компактным представлениям.
    
    Сравнение подходов показало, что автоэнкодер исключительно субъективно демонстрирует наибольшую точность рекомендаций, находя треки с наиболее схожим звучанием, однако все три варианта вполне справляются со своей задачей

# Направления для улучшения
1. Добавление данных пользователей для создания персонализированных рекомендаций.
2. Расширение объема датасета для улучшения качества рекомендаций.
3. Разработка гибридных алгоритмов, сочетающих несколько методов анализа и рекомендаций.

