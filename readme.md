## `Akka` - руководство

`Akka` - набор библиотек с открытым исходным кодом для разработки масштабируемых, устойчивых систем, 
охватывающих процессорные ядра и сети. `Akka` позволяет сосредоточиться на удовлетворении потребностей бизнеса вместо 
написания низкоуровневого кода для обеспечения надежного поведения, отказоустойчивости и высокой производительности.

Многие распространенные практики и принятые модели программирования не затрагивают важных проблем, присущих проектированию 
систем для современных компьютерных архитектур. Чтобы быть успешным, распределенные системы должны справляться с ситуацией, 
когда компоненты вылетают без ответа, сообщения теряются без следа на проводе, а латентность сети колеблется. Эти проблемы 
возникают регулярно в тщательно управляемых средах внутри центра обработки данных - тем более в виртуализированных архитектурах.

### Содержание:

#### Руководство по началу работы:
 
1. [Почему современным системам нужна новая модель программирования](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/why-modern-systems-need-anew-programming-model.md)
2. [Как модель актора отвечает потребностям современных распределенных систем](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/how-the-actor-model-meets-the-needs-of-modern-distributed-systems.md)
3. [Обзор библиотек и модулей Akka](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/overview-of-akka-libraries-and-modules.md)
4. [Быстрый старт с Акка](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/akka-quicksrart.md)
5. [Введение в пример](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/introduction-to-the-example.md)
   * [1. Архитектура акторов](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/part1-actor-architecture.md)
   * [2. Создание первого актора](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/creating-the-first-actor.md)
   * [3. Работа с акторами устройств](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/working-with-device-actors.md)
   * [4. Работа с группами устройств](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/working-with-device-groups.md)

#### Общие понятия:

1. [Терминология, концепции](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/Terminology_Concepts.md)
2. [Системы акторов](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/actor-systems.md)
3. [Что такое актор?](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/what-is-an-actor.md)
4. [Наблюдение и мониторинг](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/supervision-and-monitoring.md)
5. [Ссылки, пути и адреса акторов](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/actor-references-paths-and-addresses.md)
6. [Прозрачность местоположения](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/location-transparency.md)
7. [Акка и модель памяти Java](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/akka-and-the-java-memory-model.md)
8. [Надежность доставки сообщений](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/message-delivery-reliability.md)
9. [Конфигурация](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/concepts/configuration.md)

#### Акторы:

1. [Акторы](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/actors.md)
2. [Отказоустойчивость](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/fault-tolerance.md)
3. [Диспетчеры](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/dispatchers.md)
4. [Почтовые ящики](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/mailboxes.md)
5. [Маршрутизация](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/routing.md)
6. [FSM](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/FSM.md)
7. [Персистентность](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/persistence.md)
   * [Снимки (Snapshots)](https://github.com/steklopod/akka/blob/akka_starter/src/main/resources/readmes/actors/snapshots.md)


Чтобы помочь вам справиться с этими реалиями, `Akka` обеспечивает:

* **Многопоточное поведение без использования низкоуровневых конструкций параллелизма**, таких как атомики или блокировки, - 
избавляя вас от мысли даже о проблемах видимости памяти;

* **Прозрачная удаленная связь между системами и их компонентами** - освобождает вас от написания и поддержки сложного сетевого кода.

* **Кластеризованная архитектура с высокой доступностью**, которая является эластичной, масштабируется внутри или снаружи по 
требованию, что позволяет вам создавать действительно реактивную систему.

Использование `Akka` моделей акторов обеспечивает уровень абстракции, который облегчает запись правильных параллельных и 
распределенных систем. Модель актора охватывает полный набор библиотек `Akka`, предоставляя вам последовательный способ 
понимания и использования. Таким образом, `Akka` предлагает глубину интеграции, которую вы не можете достичь, выбирая 
библиотеки для решения индивидуальных проблем и пытаясь собрать их вместе.

**Акторы** - это  являются единицей исполнения в `Акка`. Модель `Actor` представляет собой абстракцию, которая упрощает 
запись правильных параллельных и распределенных систем. 

Изучая `Akka` и как использовать модель актора, вы получите доступ к обширному и глубокому набору инструментов, которые 
позволят решить сложные проблемы с распределенными / параллельными системами в единой модели программирования, где все 
будет сочетаться плотно и эффективно.

### Преимущества использования модели Actor

_Следующие характеристики `Akka` позволяют вам интуитивно решать сложные задачи параллелизма и масштабируемости:_

* **Модель, управляемая событиями**. Участники выполняют работу в ответ на сообщения. Общение между акторами асинхронно, 
позволяя Акторам отправлять сообщения и продолжать свою работу без блокировки, чтобы ждать ответа;

* **Сильные принципы изоляции**. В отличие от обычных объектов в Scala, у актора нет общедоступного API с точки зрения 
методов, которые вы можете вызвать. Вместо этого его общедоступный API определяется через сообщения, которые обрабатывает 
актор. Это предотвращает любое разделение состояния между акторами; единственный способ наблюдать за состоянием другого 
актора - это послать ему сообщение с просьбой об этом;

* **Прозрачность местоположения**. Система создает акторы из фабрики и возвращает ссылки на экземпляры. Поскольку местоположение 
не имеет значения, экземпляры акторов могут запускаться, останавливаться, перемещаться и перезапускаться, чтобы масштабироваться 
вверх и вниз, а также восстанавливаться после неожиданных сбоев;

* **Легкость**. Каждый экземпляр потребляет всего несколько сотен байтов, что реально позволяет миллионам одновременно 
действующих акторов существовать в одном приложении.


_Если этот проект окажется полезным тебе - нажми на кнопочку **`★`** в правом верхнем углу._
