---
order: 1
title: Настройка монетизируемых учетных данных
---

Это подробное руководство о том, как монетизировать свои учетные данные с помощью Cyberos.

### **Создание экосистемы**

Администраторы экосистемы могут устанавливать плату за проверку для участников экосистемы. Проверяющие смогут получить доступ к учетным данным только в том случае, если они находятся в одной экосистеме с эмитентом. См. пошаговое руководство по [настройке экосистемы](./../ekosistemnye-instrumenty/sozdanie-ekosistemy).

:::note 

Администраторы экосистемы должны приглашать верификаторов в экосистему с оплаченными учетными данными только в том случае, если у них установлены платежные отношения.

:::

### **Назначение схем и добавление цен проверки**

Цены проверки добавляются к схемам при назначении их участникам экосистемы.

Сначала необходимо [создать схему](./../sozdanie-skhemy), а затем [назначить ее экосистеме.](./../ekosistemnye-instrumenty/sozdanie-ekosistemy)

Плата за верификацию будет отображаться для всех участников экосистемы. Плата за верификацию отображается в Рублях, но администраторы экосистемы могут совершать транзакции со своими участниками экосистемы в предпочитаемой ими валюте.

:::note 

Cyberos взимает процент от платы за верификацию в качестве комиссии платформы. За каждую проверку, где эта комиссия слишком низкая, мы взимаем минимальную плату платформы.

Система поддерживает отслеживание комиссий с точностью до долей рубля, до шести знаков после запятой.

:::

### **Выдача удостоверений**

Процесс выдачи удостоверений будет таким же.

Эмитент увидит сообщение о том, что учетные данные могут быть проверены только участниками указанной экосистемы и за проверку взимается плата.

:::note 

Тип удостоверения с нулевым разглашением является обязательным для платной проверки и будет выбран по умолчанию.

:::

Для владельцев монетизируемые учетные данные будут выглядеть почти так же, как и обычные учетные данные: в настройках учетных данных они смогут увидеть значок «Привязан к экосистеме» с пояснением, что эти учетные данные были выпущены в рамках определенной экосистемы и могут быть переданы только верификаторам, авторизованным этой экосистемой.

### **Создание шаблона проверки и его назначение**

При [создании шаблона проверки](./../proverka-uchetnykh-dannykh) будет показано сообщение о том, что за проверку каждого удостоверения с использованием выбранной схемы взимается плата.

[Шаблоны проверки необходимо добавить в экосистему](./../ekosistemnye-instrumenty/sozdanie-ekosistemy), и они будут видны всем участникам.

:::note 

Монетизируемые учетные данные не поддерживают верификацию между кошельками.

:::

### **Выбор DID для проверки**

При использовании шаблона проверки учетных данных, который можно монетизировать, верификатору будет предложено выбрать DID верификатора. Это должен быть тот же DID, который участвует в экосистеме.

:::note 

Если у владельца имеется одинаковая информация в монетизируемых учетных данных из двух разных экосистем, верификация по умолчанию будет осуществляться в наименее дорогой экосистеме.

:::

### **Получение отчета по выставлению счетов**

Все платежи управляются администратором экосистемы. Cyberos предоставляет отчет по выставлению счетов, который может быть загружен администратором экосистемы.

Данные отчета о выставлении счетов можно выбрать для определенного диапазона дат, и они будут включать информацию о дате проверки, схеме, которая была проверена, идентификаторе проверки, DID эмитента и верификатора, успешности проверки, а также о комиссиях за проверку и платформу.

Отчет о выставлении счетов включает в себя все проверки, в ходе которых учетные данные были отправлены для проверки. Например, если был сделан запрос на проверку, но учетные данные не были предоставлены, они не будут включены. Однако если были предоставлены недействительные учетные данные и проверка не пройдена, они будут включены в отчет о выставлении счетов.

:::note 

Администраторы экосистемы берут на себя ответственность за возврат платежей и споры.

:::

:::note 

Администраторы экосистемы могут удалять участников экосистемы, которые не соответствуют требованиям экосистемы.

:::


