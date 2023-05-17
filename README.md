# Тестовое задание

### Дано:
- Имеется сервис дислокации вагонов, который возвращает список вагонов, их дату прибытия на станцию, а такж привязанную накладную. Вызов сервиса эмулируется функцией get_current_dislocation()
- Имеется сервис, который предсказывает дату прибытия по накладной. На вход передается список из уникальных накладных.
Вызов сервиса эмулируется функцией get_predicted_date_by_invoices()


### Необходимо сформировать сервис (функцию api_call), которая бы:
1. Получал бы список вагонов из сервиса дислокации.
2. Формировал список накладных тех вагонов, у котороых отсутствует дата прибытия.
3. Отправлял этот список в сервис предсказания даты прибытия.
4. У всех вагонов без даты прибытия выставлял предсказанную дату прибытия.
5. Возвращал список с обновленными данными. 

### Выполнение задания:
1. Создан список с накладными, у которых "arrivale_date" отсутствует.
2. По каждой накладной из этого списка создана дана прибытия.
3. В списке "locations" с помощью функции "api_call" изменены пустые даты прибытия на предсказанные даты.

### Используемые технологии:
- Модуль "pprint" для более удобного вывода накладных при тесте.
- Range в функции "get_current_dislocation" уменьшен для более удобного отслеживания дат.
- Модули "black" и "isort" для форматирования кода.
