# BarterHub
Платформа для обмена вещами между пользователями

BarterHub - это веб-приложение, позволяющее пользователям публиковать объявления о своих вещах и обмениваться ими с другими пользователями на основе бартерной системы.


🧱 Структура моделей
Модель Ad
Поле	Тип	Описание
user	ForeignKey(User)	Автор объявления
title	CharField	Заголовок
description	TextField	Описание товара
image_url	URLField (optional)	Ссылка на изображение
category	CharField	Категория товара
condition	CharField (choices)	Состояние: новый или б/у
created_at	DateTimeField	Дата публикации (авто)


Модель ExchangeProposal
Поле	Тип	Описание
ad_sender	ForeignKey(Ad)	Объявление отправителя
ad_receiver	ForeignKey(Ad)	Объявление получателя
comment	TextField	Комментарий к предложению
status	CharField (choices)	Статус: ожидает / принята / отклонена
created_at	DateTimeField	Дата создания (автоматическая)