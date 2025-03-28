---
order: 2
title: Выдача проверяемых учетных данных
---

В меню «Учетные данные» нажмите «Выдать учетные данные».

### **Выберите схему учетных данных**

Выберите готовую схему учетных данных, нажав на ее имя, или создайте собственную схему. Вы можете нажать на Предварительный просмотр, чтобы увидеть, какие атрибуты включены в шаблон.

### **Выберите дизайн**

Выберите дизайн или создайте новый, для своих учетных данных. В качестве альтернативы вы можете продолжить без дизайна.

### **Добавить получателей**

Если вам нужно выдать много учетных данных, вы можете выдать их оптом. Для этого выберите **Импортировать электронную таблицу.**

Загрузите образец шаблона CSV и заполните необходимые данные для шаблона учетных данных. Загрузите готовый файл .csv обратно в Cyberos. Прочитайте, как правильно отформатировать электронную таблицу в формате CSV.

Если вы хотите добавлять получателей по одному, выберите «Добавить вручную».

Вы можете отправить свои учетные данные по электронной почте или напрямую в их кошелек через их DID.

Чтобы отправить учетные данные по электронной почте, введите адрес электронной почты получателя в поле **«Электронная почта получателя»** .

Чтобы отправить учетные данные непосредственно на кошелек владельца, введите его DID в поле «Идентификатор субъекта» (Идентификатор получателя).

Заполните все остальные атрибуты, которые необходимо включить в учетные данные, *например, имя субъекта, название учетных данных и т. д.*

### **Форматирование CSV-файла для загрузки получателем**

Вы можете загрузить файл-образец CSV, чтобы использовать его в качестве основы для загрузки данных получателя. Файл-образец содержит только 3 столбца с атрибутами *name*, *did* и *date* .

Вам нужно будет добавить столбцы и удалить те, которых нет в вашей схеме учетных данных.

При загрузке файла вы сможете выбрать спецификацию набора символов. UTF-8 будет выбором большинства пользователей. Если ваш набор данных содержит специальные символы, вам может потребоваться выбрать другой набор символов, основанный на том, который используется для кодирования вашего файла данных.

Если вы не знаете владельцев, вам не обязательно использовать его для импорта, вы можете добавить адреса электронной почты для рассылки по электронной почте или распространить учетные данные вручную.

Вам будет предложено сопоставить столбцы в файле csv с полями учетных данных. Если в схеме учетных данных есть обязательные поля, их необходимо заполнить, иначе импорт не будет успешным.

### **Истекает срок действия учетных данных**

Если вам необходимо, чтобы срок действия учетных данных истек, включите переключатель срока действия и введите дату окончания срока действия.

### **Выберите настройки учетных данных**

После того, как вы добавили получателей учетных данных, вы сможете выбрать настройки учетных данных. Сначала выберите, какой профиль организации (DID) вы хотите использовать для выдачи учетных данных.

У вас есть возможность:

-  **Сохранять учетные данные:** эта опция зашифрует учетные данные, предоставив пароль для доступа к ним и сохранит их на серверах Cyberos. Доступ к учетным данным и их проверка могут быть выполнены с помощью URL или QR-кода. Получатель может отсканировать QR-код, чтобы импортировать учетные данные в приложение кошелька. Учетные данные могут быть удалены из облака Cyberos после получения или по временной метке.

-  **Создать PDF-файл:** если вы решите сохранить учетные данные, PDF-файлы будут содержать QR-код, который получатель может отсканировать, чтобы просмотреть и сохранить свои учетные данные в приложении-кошельке на своем телефоне.

-  **Отзыв учетных данных:** Выбрав этот вариант, вы оставляете возможность отзыва учетных данных до недействительного состояния в любое время. Если вы не отметите этот параметр, учетные данные никогда не будут отозваны и всегда будут проверяемыми.

-  **Zero-Knowledge Proof:** выбор этого параметра выдаст ваши учетные данные с подписью Cyberos BBS2025. Это позволяет держателям учетных данных делиться определенными данными, а не показывать все учетные данные, чтобы повысить свою конфиденциальность. Он должен быть включен для платных проверок.

Persisting -- хороший вариант для эмитентов, если они хотят безопасно хранить учетные данные в качестве резервной копии. Он шифрует учетные данные с помощью алгоритма Libsodium crypto secretbox Salsa20/Poly1305 и сохраняет их на наших серверах, которые находятся в России и работают на Yandex Cloud. Поскольку информация об учетных данных зашифрована, Cyberos не может получить к ней доступ, что обеспечивает конфиденциальность и безопасность данных.

### **Распространить учетные данные**

Если вы ввели DID держателя в поле Субъект ID, держатель получит учетные данные непосредственно в свой кошелек без необходимости какой-либо дополнительной коммуникации.

Если вы ввели адрес электронной почты, у вас будет возможность написать сообщение и просмотреть электронное письмо, которое будет отправлено получателю учетных данных.

Если у вас нет или вы не хотите использовать DID или электронную почту для распространения учетных данных, вы можете пропустить ввод этих данных в учетные данные. Система уведомит вас об отсутствии данных получателя, и учетные данные придется распространять вручную.

После выдачи учетных данных важно загрузить их, особенно если вы их не сохранили, иначе вы не сможете их восстановить.