# Планирование тестирования

## Перечень автоматизируемых сценариев

### 1 Заполнение всех полей формы "Купить" или "Купить в кредит" *валидными* значениями

Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Номер карты" APPROVED номер карты
4. Ввести в поле "Месяц" *валидное* значение
5. Ввести в поле "Год" *валидное* значение
6. Ввести в поле "Владелец" *валидное* значение
7. Ввести в поле "CVC/CVV" *валидное* значение 
8. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: появляется окошко: "Успешно! Операция одобрена Банком.", в таблице Payment Gate появляются данные карты APPROVED, таблица с заявкой на покупку тура заполнена

### 2 Заполнение поля "Номер карты" в форме "Купить" или "Купить в кредит" заблокированным номером карты
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести DECLINED номер карты
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: появляется окошко: "Ошибка! Банк отказал в проведении операции.", в таблице Payment Gate появляются данные карты DECLINED, таблица с заявкой на покупку тура не заполнена

### 3 Оставляем поле "Номер карты" пустым
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Оставить пустым поле "Номер карты"
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"
   
**Ожидаемый результат**: под полем "Номер карты" появляется сообщение: "Неверный формат"

### 4 Заполнение поля "Номер карты" 10 цифрами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Заполнить поле "Номер карты" 10 цифрами
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Номер карты" появляется сообщение: "Неверный формат"

### 5 Заполнение поля "Номер карты" неизвестной картой
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/g
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Заполнить поле "Номер карты" неизвестной картой
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: появляется окошко: "Ошибка! Банк отказал в проведении операции."

### 6 Заполнение поля "Номер карты" буквами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Заполнить поле "Номер карты" буквами
  
**Ожидаемый результат**: в поле ничего не вводится

### 7 Заполнение поля "Номер карты" символами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Заполнить поле "Номер карты" символами
   
**Ожидаемый результат**: в поле ничего не вводится

### 8 Оставляем поле "Месяц" пустым
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Оставить поле "Месяц" пустым
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Месяц" появляется сообщение: "Неверный формат"

### 9 Заполнение поля "Месяц" значением 00
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Месяц" значение 00
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Месяц" появляется сообщение: "Неверно указан месяц"

### 10 Заполнение поля "Месяц" числом 13
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Месяц" числом 13
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Месяц" появляется сообщение: "Неверно указан месяц"

### 11 Заполнение поля "Месяц" буквами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Месяц" буквами
   
**Ожидаемый результат**: в поле ничего не вводится

### 12 Заполнение поля "Месяц" символами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Месяц" символами
   
**Ожидаемый результат**: в поле ничего не вводится

### 13 Оставляем поле "Год" пустым
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Оставить поле "Год" пустым
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Год" появляется сообщение: "Неверный формат"

### 14 Заполнение поля "Год" числом 20
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Год" число 20
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Год" появляется сообщение: "Истек срок действия карты"

### 15 Заполнение поля "Год" числом 30
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Год" число 29
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Год" появляется сообщение: "Неверно указан срок действия карты"

### 16 Заполнение поля "Год" одной цифрой
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Год" цифру 9
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Год" появляется сообщение: "Неверный формат"

### 17 Заполнение поля "Год" буквами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Год" буквами
   
**Ожидаемый результат**: В поле ничего не вводится

### 18 Заполнение поля "Год" символами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Год" символами
   
**Ожидаемый результат**: В поле ничего не вводится

### 19 Заполнение поля "Владелец" только именем
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Владелец" только имя
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Владелец" появляется сообщение: "Неверный формат"

### 20 Заполнение поля "Владелец" именем и фамилией на русском языке
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести имя и фамилию в поле "Владелец" на русском языке
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Владелец" появляется сообщение: "Неверный формат"

### 21 Заполнение поля "Владелец" двойным именем
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Владелец" двойное имя
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: появляется окошко: "Успешно! Операция одобрена Банком."

### 22 Оставляем поле "Владелец" пустым
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Оставить поле "Владелец" пустым
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "Владелец" появляется сообщение: "Неверный формат"

### 23 Заполнение поля "Владелец" символами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Владелец" символами
   
**Ожидаемый результат**: в поле ничего не вводится

### 24 Заполнение поля "Владелец" цифрами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "Владелец" цифрами
   
**Ожидаемый результат**: В поле ничего не вводится

### 25 Заполнение поля "CVC/CVV" 2 цифрами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "CVC/CVV" 2 цифры
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "CVC/CVV" появляется сообщение: "Неверный формат"

### 26 Оставляем поле "CVC/CVV" пустым
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Оставить поле "CVC/CVV" пустым
4. Заполнить остальные поля формы *валидными* значениями
5. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под полем "CVC/CVV" появляется сообщение: "Неверный формат"

### 27 Заполнение поля "CVC/CVV" символами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "CVC/CVV" символами
   
**Ожидаемый результат**: в поле ничего не вводится

### 28 Заполнение поля "CVC/CVV" буквами
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Ввести в поле "CVC/CVV" буквами
  
**Ожидаемый результат**: в поле ничего не вводится

### 29 Отправка незаполненной формы
Шаги воспроизведения:
1. Открыть страницу по адресу http://localhost:8080/
2. Нажать кнопку "Купить" или "Купить в кредит"
3. Нажать на кнопку "Продолжить"

**Ожидаемый результат**: под всеми полями формы появляется сообщение: "Неверный формат"

#### Значениями для полей являются:
- APPROVED карта — 1111 2222 3333 4444;
- DECLINED карта — 5555 6666 7777 8888;
- Месяц - от 1 до 12, но если год-текущий - не меньше текущего месяца;
- Год - 2 последние цифры текущего и последующих 5 лет;
- Владелец - от 1 до 64 символов: заглавные английские буквы, пробелы, тире, апостроф;
- CVC/CVV - 3 цифры.

## Перечень используемых инструментов с обоснованием выбора

- **IDE: IntelliJ IDEA**;
- **Gradle** - для автоматизации сборки и добавления зависимостей, легче по сравнению с **Maven**;
- **JUnit5** - популярный и полнофункциональный фреймворк для модульного тестирования;
- **Selenide** - популярный и простой инструмент для UI тестов;
- **Docker-compose** - для быстрого развёртывания SUT с заданными параметрами и версиями БД;
- **Allure** - подходящая система репортинга для планируемого объёма тестирования;
- **DBeaver** - для проверки данных в БД.

## Перечень и описание возможных рисков при автоматизации

**Финансовые риски**: Существует потенциальная угроза значительных финансовых затрат, особенно в случае, если окупаемость инвестиций будет зависеть от регулярных релизов продукта. Важно оценить эффективность автоматизации и убедиться, что выгоды будут превышать затраты. В случае отсутствия регулярных релизов, ручная проверка может оказаться более экономически целесообразной.

**Управление объемом тестов**: Большое количество тестов может стать проблемой, требующей значительного внимания к поддержке и актуализации. Важно разработать эффективную стратегию управления тестовыми сценариями, чтобы минимизировать риски устаревания и обеспечить их актуальность.

**Изоляция входных данных**: Использование изолированных входных данных может привести к эффекту пестицида, при котором тесты перестают выявлять новые дефекты из-за однотипности данных. Для преодоления этого риска следует рассмотреть разработку генератора случайных данных, обеспечивающего разнообразие входных параметров.

**Риски при использовании заглушек в банковском сервисе**: Использование заглушек в банковском сервисе может создать риск, связанный с недостаточным выявлением дефектов при подключении реальной системы. Важно тщательно тестировать заглушки и предварительно оценить их соответствие реальным условиям работы, чтобы избежать непредвиденных проблем при переходе к реальной системе.

## Интервальная оценка с учётом рисков в часах

1. Подготовка к проведению тестирования - 10 часов.
2. Разработка автотестов - 28-36 часов.
3. Создание баг-репортов - 6-10 часов.
4. Составление отчёта по результатам автоматизации - 6-10 часов.

## План сдачи работ

1. Планирование тестирования: 13.12.2023 - 15.12.2023
2. Разразботка автотестов: 16.12.2023 - 18.12.2023
3. Создание баг-репортов: 19.12.2023
4. Составление отчёта по результатам автоматизации: 20.12.2023