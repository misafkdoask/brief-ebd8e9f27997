# Delivery-стек и комплаенс для AI-агентства (2025-2026)

Research agent report, 2026-07-22.

## A. Delivery-стек

### Что стандартизируют агентства
- Слои: n8n (backbone, глубочайшие agent-примитивы, 70+ AI-нод, LangChain в n8n 2.0); Zapier/Make (быстрый клиентский glue); code-first: LangGraph (лидер продакшена), CrewAI (прототипы), Claude Agent SDK (автономные пайплайны); no-code платформы Lindy/~$50, Relevance $19-199, Gumloop ~$97 - скорость, но lock-in и per-task цены.
- Триггер миграции Zapier→self-hosted n8n: биллинг >$300/мес; payback 8-12 нед.
- "Make прячет сложность в UI, n8n - в голову" → n8n требует технического оператора (у нас есть).
- Self-hosted n8n = unlimited executions + full data control (комплаенс-аргумент для fintech/crypto).
- С 15 июня 2026 Claude Agent SDK / claude -p не ест лимиты подписки - отдельный monthly credit pool.
- **n8n Sustainable Use License**: платный консалтинг/билд/поддержка - можно; "n8n as a service" (один инстанс, много клиентов со своими кредами) - нельзя без Embed. Толкает к client-owned инстансам.

### Ownership/handover
- Модель 1 (agency-hosted, lock-in ретейнер) - максимум recurring, но грязный оффбординг, изоляция, лицензия.
- Модель 2 (client owns) - покупатели всё чаще требуют: контроль, portability, data sovereignty, чистый выход.
- Синтез успешных: деплой в аккаунтах клиента, lock-in = maintenance-ретейнер ("API меняются, кто-то должен следить"), не инфраструктура.
- Бенчмарки: automation-проекты $2,500-15,000 setup; custom agents $20-50K+; maintenance $500-5,000/мес (avg $2-5K для агентских систем). Мотив: project fee → retainer после измеримой ценности.

### Model/API стратегия
- Global: Claude (тексты/агенты), GPT (широта), Gemini (мультимодал/кост); batch API + prompt caching ≈ -50%. Чистый паттерн: ключи клиента в аккаунтах клиента - API-косты вне нашего P&L.
- RF: OpenAI блокирует РФ с mid-2024. Рабочий паттерн = API-агрегаторы: ProxyAPI (~3-4x официала, стабильный, Claude Code из коробки - продакшен), AITunnel (~2x, бэкап), Polza AI (ниже официала, подозрение на подмену моделей - избегать для клиентских данных).
- Домашние модели для RF PII: YandexGPT 5.1 Pro (сильнейший текст нач. 2026), GigaChat 2.0 (код/Сбер-экосистема). Паттерн интеграторов: домашние/on-prem для ПДн, западные через агрегатор для PII-free creative/analysis.

### Templates/IP
- Build once, deploy many = маржа. Пример: $47K/yr на перепродаже 3 workflows. Gap рынка = не "больше шаблонов", а шаблоны, решающие одну конкретную бизнес-проблему с документацией.
- Деплой копии в клиентский инстанс: клиент владеет копией, мастер-библиотека+доки+eval harness = наш IP.

## B. Комплаенс

### EU AI Act
- 2 авг 2026: Article 50 transparency. Синтетика (аудио/видео/имидж/текст) - machine-readable маркировка; чат-боты представляются; deepfakes и public-interest тексты - disclosure. Спрятанные лейблы не считаются.
- 2-местный не-EU шоп, обслуживающий EU-клиентов = deployer: Article 4 AI-literacy (с фев 2025), governance, disclosure. Маркетинг-контент не high-risk; GPAI-обязательства на провайдерах моделей, не на нас.

### Платформы + FTC
- Meta: обязательный disclosure для political/social с реалистичным AI; авто-"AI info" лейблы на креативах из Meta-тулов; self-certification.
- Google (TechCrunch 09.07.2026): авто-лейблы на ads из Google gen-AI; self-declare контрол для внешнего AI; "How this ad was made" в My Ad Center.
- TikTok: строже всех - AIGC toggle/AI Disclosure tag, removals +340%. C2PA-метаданные автотриггерят лейблы.
- FTC (Operation AI Comply, 12+ дел): бьёт за overclaim AI-возможностей, не за использование AI. "AI-powered" claims требуют substantiation.

### RF
- Маркировка рекламы (ОРД/ЕРИР): erid + "Реклама" + данные рекламодателя на каждый креатив; штрафы 100-500K ₽ за креатив; с 2026 ЕРИР матчит цепочки AI в реальном времени; мелкий erid = отсутствующий. Любая публикующая автоматизация для RF обязана включать ОРД-шаг → это сервисная возможность ("автоматизируем цепочку маркировки").
- Закон о маркировке ИИ-контента: принят mid-2026, в силе 1 сен 2026, смягчён: платформы дают техвозможность тегать, обязанности маркировать свой AI-контент НЕТ. Следить за подзаконкой.
- 152-ФЗ: клиентская CRM в западный LLM = трансграничная передача ПДн; иностранные провайдеры не подпишут договор поручения → PII в западные API нельзя вообще (и через агрегатор тоже). PII → YandexGPT/GigaChat с поручением или on-prem; деперсонализация до любого cross-border вызова.

### Procurement (что спрашивают клиенты)
- DPA + список субпроцессоров (LLM-провайдеры = субпроцессоры), retention, incident process, RBAC/least-privilege с конкретикой, ротация ключей, MFA, audit logs, "тренируются ли модели на данных" (ответ: no-training API tiers).
- Для low-touch вендора достаточно DPA + security one-pager; SOC 2 на день 1 не нужен.
- Практики 2-местного шопа: креды только в аккаунтах клиента (invited seats); least-privilege by construction (advertiser не admin, скоупы, ключ на workflow, ротация квартально); DPA-шаблон + subprocessor page; retention statement (логи авто-purge, EXECUTIONS_DATA_MAX_AGE); MFA, без секретов в JSON; security one-pager (закрывает сделки 3x быстрее).

## Рекомендованный v1 стек (~$15-75/мес fixed)

| Компонент | Выбор | Кост |
|---|---|---|
| Workflow engine (на клиента) | n8n self-hosted на VPS клиента ($5-10/мес, платит клиент) или его n8n Cloud €24/мес | $0 нам |
| Наш dev/staging | self-hosted n8n на VPS $10-20/мес | ~$15 |
| Agent/build | Claude Code + Agent SDK (credit pool) | $0 |
| LLM Global | Ключи клиента; batch+caching -50% | $0 (pass-through) |
| LLM RF | YandexGPT/GigaChat через аккаунт клиента для PII; ProxyAPI для PII-free premium; AITunnel бэкап | usage, биллится клиенту |
| Templates/IP | Приватный Git: JSON + доки + eval-промпты | $0 |
| Ops | UptimeRobot free + error-alert workflow → наш TG | $0 |
| Security | Bitwarden, DPA-шаблон, one-pager | ~$0 |

Revenue: setup $1.5-5K/пакет, ретейнер $300-1,500/мес/клиент, шаблоны редеплоятся.

## Чеклист комплаенса

Global: Article 50 disclosure с 02.08.2026; Article 4 AI-literacy note (1 стр); Meta/Google/TikTok AI-декларации в каждом ad-workflow; C2PA-политика на клиента; без "AI-powered" overclaim; DPA + субпроцессоры + no-training tiers; креды у клиента, least-privilege, ротация, MFA, log-purge.

RF: erid через ОРД + "Реклама" автоматизированным шагом (Яндекс-каналы автомаркируются - безопаснее всего); роли отчётности в ЕРИР зафиксировать в договоре; штрафы 100-500K ₽/креатив; НИКАКОГО PII в иностранные API; проверka РКН-регистрации клиента как оператора ПДн до подключения CRM; AI-теги с 01.09.2026 (добровольно); ProxyAPI для продакшена, избегать дешёвых реселлеров; закрывающие документы через RF-юрлицо агрегатора.

Ключевые источники: digitalapplied.com, docs.n8n.io/sustainable-use-license, digital-identity-architects.com, arsum.com, taskip.net, latenode.com (17-agency survey), cloudzero.com, vc.ru/promptra/2962649 (агрегаторы), sostav.ru/blogs/289807/86785, azoneai.ru, artificialintelligenceact.eu/article/50, datamatters.sidley.com, techcrunch.com/2026/07/09 (Google AI ad labels), commonthreadco.com, beneschlaw.com (FTC), callibri.ru (маркировка 2026), kommersant.ru/doc/8515349, anti-malware.ru, pdaudit.ru, deepinspect.ai, docket.io.
