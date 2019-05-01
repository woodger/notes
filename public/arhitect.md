# Архитект

## Микросервисная архитектура

Взаимодействие небольших, слабо связанных и легко изменяемых модулей — микросервисов.

В микросервисной архитектуре системы выстраиваются из компонентов, выполняющих относительно элементарные функции, и взаимодействующие с использованием экономичных сетевых коммуникационных протоколов (в стиле `REST` (`JSON`, `Buffers`).

`Buffers` — протокол сериализации (передачи) структурированных данных, предложенный Google как эффективная бинарная альтернатива текстовому формату `XML`.

За счёт повышения **гранулярности** модулей микросервисная архитектура нацелена на уменьшение степени зацепления (точек связей) и увеличение связности, что позволяет проще добавлять и изменять функции в системе в любое время.

В традиционных вариантах **сервис-ориентированной** архитектуры модули достаточно сложные, а взаимодействие между ними организуется на стандартизованных тяжеловесных протоколах (`SOAP`, `XML-RPC`).

Ключевые аспекты, для микросервисной архитектуры:

- акцент на простоту, независимость развёртывания и обновления каждого из микросервисов;
- микросервис по возможности выполняет только одну достаточно элементарную функцию;
- могут быть реализованы на различных языках программирования, фреймворков, выполняться в различных средах контейнеризации, виртуализации, под управлением различных операционных систем на различных аппаратных платформах: приоритет отдаётся в пользу наибольшей эффективности;

Философия микросервисов - сервис должен «делать что-то одно, и делать это хорошо» и взаимодействовать с другими программами простыми средствами.

Каждый из микросервисов как правило изолируется в отдельный контейнер или небольшую группу контейнеров, доступную по сети другим микросервисам и внешним потребителям, и управляется средой **оркестрации**, обеспечивающей отказоустойчивость и балансировку нагрузки.



## DevOps

Разработка + Тестирование + Эксплуатация

DevOps - набор практик, нацеленных на активное взаимодействие специалистов по разработке со специалистами по информационно-технологическому обслуживанию и взаимную интеграцию их рабочих процессов друг в друга.
Базируется на идее быстро обновлять программные продукты.

В идеале, системы автоматизации сборки и выпуска должны быть доступны всем разработчикам в любом окружении, и у разработчиков должен быть контроль над окружением, а информационно-технологическая инфраструктура должна становиться более сфокусированной на приложении.

Ключевые аспекты разработки и доставки программного обеспечения:

- `Code` разработка и анализ кода, контроль версий;
- `Build` инструменты непрерывной интеграции, сборка;
- `Test` инструменты непрерывного тестирования;
- `Пакет` предварительная установка приложения;
- `Release` управление изменениями, официальное утверждение выпуска, автоматизация выпуска;
- `Конфигурация` конфигурация и управление инфраструктурой;
- `Мониторинг` мониторинг производительности приложения.

Цели `DevOps`:

- Сокращение времени для выхода на рынок;
- Снижение частоты отказов новых релизов;
- Сокращение времени выполнения исправлений;
- Уменьшение количества времени на восстановления (в случае сбоя новой версии).

Чтобы эффективно использовать DevOps, прикладные программы должны соответствовать набору архитектурно значимых требований (ASR), таких как: возможность развертывания, изменяемость, тестируемость и возможности мониторинга.