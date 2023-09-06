# SF_Gri_PJ-04_final
## 33.1. Итоговый проект по автоматизации тестирования (PJ-04)
### Объект тестирования: Ростелеком
Для тестирования сайта были использованы:
- ручные и автоматизированные тесты;
- разбиение на классы эквивалентности;
- анализ граничных значений;
- тестирование состояний и переходов;
- чек-лист/тест-кейсы/баг-репорты.

###### Тесты настроены на запуск через Run!

Страница восстановления пароля (как позитивные, так и негативные тесты) требует ручной ввод символов с картинки.
_________________________________

##### Окружение:
- Windows 10 Корпоративная
- Chrome Версия 116.0.5845.180 (Официальная сборка), (64 бит)

Использована комбинация:
```
.send_keys(Keys.КОМАНДА, 'a')
```
```
.отправить ключи (Keys.DELETE)
```
- Для корректной работы в Windows среде необходима замена `COMMAND` на `CONTROL`
_________________________________
##### Папка tests:
- `test_negative_auth_page` - тестируем негативные сценарии страницы авторизации
- `test_negative_reg_page` - тестируем негативные сценарии страницы регистрации test_negative_new_pass_page - тестируем негативные сценарии страницы восстановления пароля
- `test_positive_auth_page` - тестируем позитивные сценарии страницы авторизации
- `test_positive_reg_page` - тестируем позитивные сценарии страницы регистрации
- `test_positive_new_pass_page` - тестируем позитивные сценарии страницы восстановления пароля
_________________________________
##### Папка pages:

- `Api_RegMail` - GET-запросы к виртуальному почтовому ящику (1secmail.com) для получения валидного e-mail и кода для регистрации на сайте/восстановления пароля.
- `locators` - локаторы XPath и CSS на web-элементы сайта
- `auth` - функции-обёртки для локаторов, распределённые по классам в зависимости от тематики тестов
- `base` - функции для применения к локаторам явных ожиданий, получения главной страницы сайта и пути текущей страницы
- `config` - исходные статические данные
- `settings` - учетные данные, используемые в процессе теста
