# smsaero_api_v2
Класс для работы с API сервиса smsaero.ru на Yii2

### Установка
```bash
composer require smsaero/smsaero_api_v2
```

```php
$smsaero_api = new \SmsAero\SmsaeroApiV2('email', 'api_key', 'SIGN'); // api_key из личного кабинета
$smsaero_api->send(['70000000000', '70000000001'], 'Тестовая отправка'); // Отправка сообщений
$smsaero_api->check_send(123456); // Проверка статуса SMS сообщения
$smsaero_api->sms_list(null, 'тест', 3); // Получение списка отправленных sms сообщений
$smsaero_api->balance(); // Запрос баланса
$smsaero_api->tariffs(); // Запрос тарифа
$smsaero_api->sign_add('new sign'); // Добавление подписи
$smsaero_api->sign_list(); // Получить список подписей
$smsaero_api->group_add('new_group_name'); // Добавление группы
$smsaero_api->group_list(); // Получение списка групп
$smsaero_api->group_delete(123); // Удаление группы
$smsaero_api->contact_add('70000000000', null, null, 'male', 'name', 'surname', null, 'param example'); // Добавление контакта
$smsaero_api->contact_delete(123); // Удаление контакта
$smsaero_api->contact_list(); // Список контактов
$smsaero_api->blacklist_add(123); // Добавление в чeрный список
$smsaero_api->blacklist_delete(123); // Удаление из чeрного списка
$smsaero_api->blacklist_list(); // Список контактов в черном списке
$smsaero_api->hlr_check('70000000000'); // Создание запроса на проверку HLR
$smsaero_api->hlr_status(474664); // Получение статуса HLR
$smsaero_api->number_operator('79136535500'); // Определение оператора
$smsaero_api->viber_send('70000000000', null, 'Bonus', 'INFO', 'Тестовое сообщение'); // Отправка Viber-рассылок
$smsaero_api->viber_statistic(1636); // Статистика по Viber-рассылке
$smsaero_api->viber_list();  // Список Viber-рассылок
$smsaero_api->viber_sign_list(); // Список доступных подписей для Viber-рассылок
```