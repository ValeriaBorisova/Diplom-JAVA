# [Отчёт по итогам тестирования][Task]

| `Gradle` [_Test Summary_](https://github.com/ValeriaBorisova/Diplom-JAVA/blob/master/Documentation/Test%20Summary.png) | `Gradle` [_Test Allure-Report_][Netlify] |
| :---: | :---: |


- [ ] **На начальном этапе** было проведено **исследовательское (ручное) тестирование** для ознакомления с проектом.
- [ ] **На следующем этапе** были созданы **авто-тесты, согласно [Плану автоматизации тестирования]

- [ ] Тестовые сценарии отрабатывались в контексте непосредственной оплаты, а также для кредитной линии (`Happy path`&`Unhappy path`). При этом проверялась корректность внесения информации в две базы данных: [_PostgreSQL_][PostgreSQL] (`default database`) и [_MySQL_][MySQL].
- [ ] Всего было исполнено **36** тестов, [успешных](https://github.com/ValeriaBorisova/Diplom-JAVA/blob/master/Documentation/Test%20Summary.png) из них всего **63%**. При этом обе заявленные базы данных поддерживаются одинаково хорошо, производительность [_PostgreSQL_][PostgreSQL] оказалась несколько выше. В целом можно рекомендовать более тщательную проработку кредитной части сервиса

#### ⚠️ Проведённая работа выявила ряд проблем, требующих внимания ⚠️Issue

[Task]: https://github.com/netology-code/qa-diploma/tree/2ccafd34b6f9eb3a66dd7a11a0b8b1ba3f266e50#%D0%BE%D1%82%D1%87%D1%91%D1%82%D0%BD%D1%8B%D0%B5-%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-%D0%BF%D0%BE-%D0%B8%D1%82%D0%BE%D0%B3%D0%B0%D0%BC-%D1%82%D0%B5%D1%81%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F
[PostgreSQL]: https://www.postgresql.org/about/
[MySQL]: https://www.mysql.com/about/
[Netlify]: http://172.27.32.1:58247/index.html#
