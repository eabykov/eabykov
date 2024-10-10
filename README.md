### Оглавление

1. [Основные принципы](main.md)
2. [Вопросы на собеседовании](questions.md)

### Основные термины SRE

| Термин | Значение |
|-|-|
| SLI | Текущий показатель обслуживания — 99.9% успешных запросов или 99.9% запросов обрабатываются менее чем за 1 секунду
| SLO | Цель уровня обслуживания — приложение отвечает быстрее 1 секунды в 99% случаев или сервис доступен 99,5% времени в году
| SLA | Документально утвержденная договоренность об уровне обслуживания с потребителями сервиса аналогична SLO, с возможными санкциями за нарушение или премиями за соблюдение
| Error Budget | Бюджет проблем — соотношение SLI к SLO, которое помогает разработчикам планировать выполнение задач по улучшению показателей устойчивости и задач с добавлением или изменением функциональности в сервис. Если это соотношение меньше 100%, то в приоритете проблемы с доступностью или производительностью
| Состояние Опасности | Свойство системы или набор условий, которые вместе с определенным набором наихудших обстоятельств окружающей среды приведут к инциденту
| Инцидент | Ситуация, при которой сервис выходит из нормального (стабильного) состояния, например диск базы данных заполняется с значительно большей скоростью, чем раньше, и на нем не останется места через 1 месяц, время ответа возросло с 1 сек до 2 сек, процент ошибок стал 0.4% вместо 0.06% 
| Postmortem | Проработка после инцидента — это анализ произошедшего и планирование мероприятий по предотвращению повторения подобного или уменьшению его последствий 
| MTTD | Время с начала инцидента до его обнаружения (командой мониторинга, сработавшее оповещение и т. д.)
| MTTR | Время с начала инцидента до полного устранения его влияния и восстановления нормальной работы сервиса
| MTTM | Время устранения влияния отличается от MTTR тем, что, возможно, есть поломка, но пользователи или партнеры не имеют проблем с нашим сервисом
| STAMP | Сиситема спроектированая на достижение безопасного состояния системы (уход от Состояние Опасности). Для понимания причин произошедшего инцидента необходимо определить, почему система управления была неэффективной. Для предотвращения будущих инцидентов необходимо переключить внимание с предотвращения инцидентов на более широкую цель - разработку и внедрение средств контроля, которые обеспечат соблюдение необходимых ограничений для безопасности.
