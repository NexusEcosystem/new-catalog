---
order: 1
title: Создание экосистемы
---

Вы можете создать экосистему через меню слева, нажав кнопку **Экосистема -> Создать экосистему**.

При создании экосистемы на блокчейне создается реестр доверия на цепочке, список взаимоотношений между эмитентами и верификаторами. Он упрощает процесс определения того, какие эмитенты и верификаторы заслуживают доверия в рамках конкретной экосистемы.

Ecosystem Tools -- это дополнительная функция. Если вы не видите ее в строке меню и хотите включить ее для своей учетной записи, свяжитесь с support@cyberos.io

Первые шаги в создании вашей экосистемы -- определение вашего бренда. Брендинг экосистемы важен, он будет присутствовать в удостоверениях, выдаваемых участниками, и шаблонах проверки для верификаторов. Наличие четко определенного бренда упрощает для участников экосистемы доверие к экосистеме и унифицированный опыт от выдачи удостоверений до хранения и проверки.

Вам необходимо будет задать **имя** экосистемы, **описание,** добавить **URL-адрес экосистемы** -- действительный URL-адрес, ведущий на страницу с описанием преимуществ и основных деталей присоединения к вашей экосистеме.

**Профиль администратора экосистемы DID** позволит вам выбрать существующего или добавить нового DID, который будет администратором экосистемы.

Следующий шаг позволит вам создать документ структуры управления, который будет использоваться для доведения правил и рекомендаций экосистемы до всех заинтересованных сторон, обеспечивая ясность и последовательность, что поможет согласовать все заинтересованные стороны в процессах, связанных с выпуском и проверкой.

### **Пригласить участника**

После настройки экосистемы вы можете начать приглашать участников. Участники экосистемы могут быть Эмитентами, Верификаторами или и теми, и другими в зависимости от их роли в вашей экосистеме. Вы сможете назначать схемы учетных данных на основе роли участника.

Участники экосистемы могут иметь и управлять своими собственными учетными записями Truvera, но мы также позволяем нашим клиентам создавать экосистемы, в которых учетные записи участников управляются и оплачиваются ими. Использование [субсчетов](./../upravlenie-komandoy/sub-akkaunty) позволяет создавать дополнительные учетные записи Cyberos и приглашать их к участию в экосистеме с помощью API.

После нажатия кнопки **«Пригласить участников»** вы сможете выбрать схему учетных данных и роль участника.

Участникам экосистемы необходимо иметь учетную запись в Cyberos, чтобы присоединиться к экосистеме. Когда они войдут в свою учетную запись Cyberos Workspace и нажмут на ссылку, предоставленную администратором экосистемы, им сразу же будет предложено **присоединиться к экосистеме** и выбрать профиль организации, который будет использоваться для участия в экосистеме.

Администратор экосистемы и участники увидят список эмитентов и верификаторов в таблице.

Администратор экосистемы сможет **приостанавливать** , **удалять** или **редактировать** существующих участников экосистемы. Он также может изменять роль участника и назначать схемы.

### **Назначить схемы учетных данных**

Чтобы назначить схему учетных данных участникам, вам сначала нужно [создать схемы](./../sozdanie-skhemy). Чтобы назначить схему, нажмите кнопку **Добавить схему**.

Вы сможете выбрать нужную схему из раскрывающегося списка или ввести URL-адрес схемы и назначить ее участникам экосистемы.

Вы можете добавить цену проверки для вашей схемы, которая установит плату за каждую проверку учетных данных с использованием выбранной схемы. Узнайте больше о ценах проверки.

Схемы учетных данных могут иметь ограниченную или публичную проверяемость. Если схема назначена хотя бы одному участнику, который может ее проверить, проверка будет ограничена только этими участниками. Если назначенных проверяющих нет, схема будет публично проверяемой.

Назначенные схемы будут немедленно доступны участникам, и после выдачи учетных данных с использованием схемы, назначенной экосистеме, брендинг экосистемы будет виден на протяжении всего пути пользователя учетных данных.

Брендинг экосистемы будет виден в кошельке после того, как участник экосистемы выдаст учетные данные.

### **Добавить шаблоны проверки**

Администратор экосистемы сможет добавлять шаблоны проверки, которые будут доступны всем участникам экосистемы.