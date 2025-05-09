---
order: 3
title: Биометрические учетные данные
---

## **Что такое биометрические учетные данные?**

Биометрические данные - это физическая характеристика, например, глаз, палец, лицо, голос, походка. Когда измеряется физическая характеристика человека, она преобразуется в нечто, что можно сохранить - шаблон регистрации.

После завершения регистрации, для сопоставления биометрических данных физический атрибут измеряется снова и переводится в то, что может быть сопоставлено -- образец-кандидат. Затем образец сопоставляется с шаблоном. Оценка соответствия сравнивается с пороговым значением для возврата положительного или отрицательного результата.

Существуют разные способы хранения биометрических данных.

**Централизованный**

Биометрический провайдер хранит биометрические данные нескольких человек в общей базе данных. Каждая проверяющая сторона интегрируется с провайдером и может видеть биометрические данные.

**Децентрализованный**

Биометрический провайдер хранит данные каждого человека в отдельном хранилище, которое невозможно восстановить без биометрического вектора.

**Хранится у пользователя**

Биометрические данные надежно хранятся на устройстве человека с использованием защищенных от несанкционированного доступа учетных данных.

### **Как работают биометрические данные, хранящиеся у пользователя**

Доверяющие стороны используют открытые стандарты для проверки учетных данных, выданных их доверенными поставщиками биометрических данных. Доверяющие стороны никогда не видят биометрические данные.

1. Проверить биометрические данные и выдать регистрационное удостоверение, содержащее биометрические данные и личный идентификатор.

2. Сверьтес биометрические данные с данными регистрации и выдайте данные для проверки биометрических данных с личным идентификатором.

3. Доверяющие стороны проверяют, что биометрические учетные данные являются последними, надежными и содержат ожидаемый частный идентификатор.

### **Что такое биометрические учетные данные?**

**Привязанные к кошельку учетные данные** -- учетные данные были помещены в кошелек при выпуске и взяты из того же кошелька при проверке. Предполагается, что в оба раза кошелек контролирует одно и то же лицо.

**Биометрическое удостоверение личности** -- то же лицо, которое получило удостоверение личности при выдаче, предоставило его для проверки.

Мы предлагаем два возможных подхода к внедрению биометрических учетных данных и решению этих проблем.

## **Как реализовать биометрические учетные данные?**

### **Образцы, взятые эмитентом и верификатором**

В этой модели эмитент и верификатор договариваются об общем поставщике биометрических данных.

Эмитент требует, чтобы держатель зарегистрировался в биометрической службе и предоставил биометрический образец через службу, прежде чем эмитент выдаст удостоверение личности.

Выданное удостоверение содержит ссылку на биометрический шаблон.

Во время проверки проверяющий требует от держателя предоставить биометрический образец через тот же сервис и проверяет его соответствие шаблону, указанному в учетных данных.

:::note 

Документация по добавлению плагина биометрической службы.

:::

**Плюсы**

Может использовать биометрическое оборудование, предоставленное эмитентом и верификатором.

Находясь вне контроля держателя, он может пользоваться большим доверием

**Минусы**

Биометрический сервис может сопоставлять эмитента, верификатора и держателя \*

Каждому эмитенту и верификатору необходимо интегрироваться с биометрическим сервисом\*\*

*\*Некоторые биометрические сервисы разработаны с учетом сохранения конфиденциальности.*

*\*\*Биометрические стандарты могут снизить стоимость интеграции и блокировки.*

### **Образцы, взятые с помощью подхода «кошелька идентификации»**

При таком подходе эмитент просит держателя предоставить подтверждение биометрической проверки перед выдачей первичного удостоверения личности.

Приложение (мобильный цифровой кошелек) обнаруживает запрос, обрабатывает биометрические данные, регистрирует владельца, выдает учетные данные и предоставляет их эмитенту.

Первичное удостоверение личности с биометрической привязкой выдается эмитентом.

Проверяющий запрашивает основные учетные данные с подтверждением биометрической проверки.

Кошелек обнаруживает запрос, обрабатывает биометрические данные и предоставляет верификатору комплексное доказательство.

Первичные учетные данные: учетные данные, которые содержат атрибуты, представляющие интерес для верификатора, в дополнение к атрибутам биометрической привязки.

#### **Биометрическая регистрация**

Держатель настраивает кошелек, интегрированный с биометрическим сервисом. Когда биометрическая привязка требуется впервые, держатель кошелька регистрируется в биометрическом сервисе.

Биометрическая служба выдает удостоверение личности, которое обычно содержит как минимум следующие атрибуты:

1. Атрибут, содержащий шаблон регистрации -- эталонный биометрический образец, который сохраняется во время регистрации, с которым сравниваются будущие биометрические образцы.

2. Атрибуты, которые можно встроить в основные учетные данные, чтобы связать их с действительными учетными данными биометрической проверки, выданными тому же владельцу

Биометрические данные необходимо преобразовать в текстовый формат, чтобы их можно было встроить в JSON. Наиболее популярным методом является использование кодировки «Base64».

Биометрический шаблон, обеспечивающий достаточную конфиденциальность, может быть встроен непосредственно в основные учетные данные, что позволяет избежать необходимости в учетных данных для регистрации.

Биометрические данные для регистрации и первоначальной проверки могут быть выданы с использованием одного и того же биометрического образца, чтобы избежать взятия дополнительного образца у владельца.

Атрибуты биометрической привязки обычно могут быть меньшего размера, чем при внедрении биометрического шаблона непосредственно в учетные данные.

#### **Выдача**

Держатель запрашивает первичные учетные данные у эмитента. Эмитент запрашивает подтверждение недавней биометрической проверки.

Кошелек удостоверения личности держателя обнаруживает, что запрос включает атрибуты биометрической привязки, и активирует связанный плагин, который запрашивает учетные данные биометрической проверки из биометрической службы.

Биометрическая служба запрашивает проверку биометрических учетных данных регистрации. Биометрическая служба проверяет новый биометрический образец по шаблону, включенному в учетные данные регистрации. Биометрическая служба выдает учетные данные, показывающие действительную биометрическую проверку, которая содержит атрибуты биометрической привязки и временную метку проверки.

Кошелек предоставляет биометрические данные для проверки подлинности эмитенту, который проверяет актуальность данных.

Эмитент выдает основные учетные данные с дополнительными биометрическими атрибутами привязки, включая идентификационные данные выдавшей биометрической службы.

#### **Проверка**

Проверяющий запрашивает комплексное подтверждение основных учетных данных и последних учетных данных биометрической верификации.

Кошелек идентификации держателя обнаруживает, что запрос включает биометрические атрибуты привязки, и запускает связанный плагин, который запрашивает биометрические учетные данные верификации из биометрической службы. Биометрический плагин кошелька следует тому же процессу, который использовался во время выдачи для получения последних биометрических учетных данных верификации.

Владелец предоставляет биометрические данные для проверки подлинности в виде комплексного доказательства вместе с основными данными.

Верификатор проверяет, что учетные данные биометрической проверки получены от доверенного поставщика биометрических услуг, который использовался при выдаче, и что атрибуты биометрической привязки основных учетных данных соответствуют атрибутам биометрической привязки в учетных данных биометрической проверки.

#### **Преимущества**

-  Биометрические данные берутся на устройстве и доступны только поставщику биометрических услуг.

-  Биометрическому сервису не нужно хранить данные владельца, но есть гарантия того, что данные не были изменены владельцем

-  Эмитенту и верификатору не нужно интегрироваться с биометрическим сервисом

-  Кошелек держателя можно легко интегрировать с несколькими биометрическими сервисами.

-  Реестр доверия может содержать список биометрических служб, которым следует доверять в экосистеме.

-  Поставщики биометрических услуг могут гарантировать, что все взаимодействия осуществляются с доверенным кошельком.

### **Проблемы конфиденциальности и предлагаемые решения**

**Как сохранить шаблон регистрации, обеспечив конфиденциальность?**

Подход с использованием кошелька идентификации: субъекту идентификации необходимо предоставить защищенные от несанкционированного доступа проверяемые учетные данные, выданные поставщиком биометрических услуг.

Подход «эмитент-верификатор»: зависит от конкретной используемой биометрической службы.

**Как привязать учетные данные к биометрическому шаблону без корреляции со стороны верификатора?**

Верификатор проверяет доказательство с нулевым разглашением (ZKP), сравнивая атрибуты биометрической привязки основных учетных данных с учетными данными биометрической проверки, не раскрывая атрибуты привязки.

**Как привязать учетные данные к биометрическому шаблону без корреляции со стороны эмитента?**

Используйте слепые подписи, чтобы не раскрывать фактический атрибут привязки.