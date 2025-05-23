---
order: 1
title: Создание профиля организации (DID)
---

Что такое DID?

Децентрализованные идентификаторы (DID) -- это уникальные идентификаторы, которые связаны с цифровой личностью. DID состоят из строки букв и цифр, которые могут храниться в блокчейне и использоваться для аутентификации этой личности.

### **Создать профиль организации (DID)**

Чтобы создать профили организации (DID), выберите «Профили организации» в меню слева, а затем нажмите «Создать профиль организации».

Заполните публичное имя, добавьте логотип и публичное описание, вы можете оставить тип DID по умолчанию «cheqd» (узнайте больше о различных типах DID). Затем выберите **«Создать профиль организации»**.

Размер изображения логотипа не должен превышать 1 МБ. Принимаемые форматы: 'jpeg', 'jpg', 'png', 'bmp'. Изображение логотипа может быть квадратным или круглым, оно будет оптимизировано для отображения.

Все профили вашей организации (DID) будут перечислены на этой странице.

---

### **Выбор типа DID**

Сегодня существует множество различных типов DID, все они поддерживают одну и ту же базовую функциональность, но они различаются тем, как создается DID или где и как хранится и извлекается документ DID. Эти различные типы DID известны как методы DID. Вторая часть формата идентификатора DID -- между первым и вторым двоеточием -- называется именем метода DID.

Cyberos поддерживает 3 типа методов DID did:key, did:cheqd и did:chain

{% table header="row" %}

---

*  {% colwidth=[120] align="center" %}

   Метод

*  {% align="center" %}

   Хранилище

*  {% colwidth=[439] align="center" %}

   Ключи

---

*  {% colwidth=[120] align="center" %}

   `did:key`

*  {% align="center" %}

   Хранится на устройстве пользователя

*  {% colwidth=[439] align="center" %}

   К этому типу DID привязана только одна пара ключей. Если ваши ключи будут раскрыты, вам придется изменить DID и все связанные с ним учетные данные.

---

*  {% colwidth=[120] align="center" %}

   `did:cheqd`

*  {% align="center" %}

   Хранится в блокчейне компании

*  {% colwidth=[439] align="center" %}

   К этому типу DID можно прикрепить несколько пар ключей, ключи можно менять по мере необходимости.

---

*  {% colwidth=[120] align="center" %}

   `did:chain`

*  {% align="center" %}

   Хранится в блокчейне ?

*  {% colwidth=[439] align="center" %}

   К этому типу DID привязана только одна пара ключей. Если ваши ключи будут раскрыты, вам придется изменить DID и все связанные с ним учетные данные.

{% /table %}



---

### **Редактировать профиль организации (DID)**

Нажмите «Профили организаций» в меню, нажмите на три точки DID, который вы хотите изменить, и выберите **«Обновить DID»** .

Обновите данные и выберите **Обновить DID** .

### **Экспорт профиля организации (DID)**

Нажмите на три точки DID, который вы хотите экспортировать, и выберите «Экспортировать DID».

Вы можете экспортировать свой DID в кошелек или другую платформу. Создайте пароль для шифрования файла и выберите Экспорт.

### **Удалить профиль организации (DID)**

Нажмите на три точки DID, который вы хотите удалить, и выберите Удалить DID.

:::note 

Удаление вашего DID сделает его запрещенным. Это означает, что любые учетные данные, которые вы выдали с ним, станут недействительными, и его больше нельзя будет найти в блокчейне. Ваша связанная пара ключей также будет удалена. Это действие нельзя отменить.

:::


