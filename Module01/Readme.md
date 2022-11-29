# Excel_analytics

- В **Orders** сразу отформатировал диапазон ячеек как таблицу, для более удобного синтаксиса встроке формул.
<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module01/img/1.png">
</p>

- Для **LookUp1** результирующие данные вывел в транспонированном виде, т.к. ИМХО удобочитаемее.

<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module01/img/2.png">
</p>


- **LookUp2** - вывод средней цены зазаказ по введенному Product ID
<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module01/img/3.png">
</p>


- Для создания **DashBoard** пользовался [**видео**](https://www.youtube.com/watch?v=j2YIAEmRpQs&ab_channel=%D0%91%D0%B8%D0%BB%D1%8F%D0%BB%D0%A5%D0%B0%D1%81%D0%B5%D0%BD%D0%BE%D0%B2%E2%80%93Excel%2CVBA%26More), отдельный рахмет создателю.
<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module01/img/4.png">
</p>


# Архитектура аналитического решения

![Fail download](https://github.com/gyllub/DE-101/blob/main/Module01/%D0%90%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0.jpg "Архитектура аналитического решения")


Выше представлена архитектура аналитического решения сервиса по выполнению заказаов электромонтажа.
Заказ поступает от клиента через различные источники и попадает в CRM, откуда уже в систему хранения. Далее с обрабатывается необходимыми сервисами и передается исполнителю. После успешного выполнения - в базу выполненных заказов и в социальные сети.