# Marketing Analytics & Reporting as an AI Service Line 2025-2026

Research agent report, 2026-07-22.

## 1. Demand

- Marketing analytics software: ~$7.1B (2025) → $14.5B (2031), 12.65% CAGR (Mordor). Data analytics outsourcing: $17-22B (2025), 30%+ CAGR прогнозы.
- 45% SMB decision-makers планируют аутсорсить маркетинг/рекламу в 2025; ~37% малого бизнеса аутсорсит минимум одну функцию.
- Upwork: стабильный поток Looker Studio dashboard джобов ($150 fixed - $100+/hr; intermediate $25-75/hr).
- Marketing analytics = 19% всех новых digital-marketing вакансий 2025 (Addison Group); найм на ~25% ниже допандемийного = talent gap толкает к аутсорсу.
- 73% маркетинг-команд: данные размазаны по источникам = топ-проблема отчётности (Databox). Агентства тратят 5-10 ч/клиент/мес на ручную отчётность; автоматизация экономит ~10.4 ч/клиент/мес. Агентства = второй сегмент покупателей.

## 2. Players and pricing

Tools: Looker Studio free (Pro $9); Supermetrics от €29/мес; AgencyAnalytics от $59/мес (~$179 на 5 клиентов), теперь с AI insights + MCP; Whatagraph от ~$270/мес (AI Summaries с янв 2025); Triple Whale $129-3,799/мес (Moby AI agents на Claude); Northbeam ~$1,000-2,500/мес; Improvado enterprise.

AI-native wave: Julius AI ($10M seed, июл 2025), TextQL ($21M), Zenlytic ($14.4M), Databox Genie. Все - продукты; никто не решает "кто это настроит, определит метрики и владеет числом для CEO".

Service pricing:
- Looker Studio проекты: $2,000-6,000 за 3-5 connected reports; $5,000-15,000 с BigQuery-пайплайном; commodity floor $150-500 за базовый дашборд.
- GA4 аудиты: $4,000-8,000; analytics ретейнеры $2,000-4,000/мес (10-20ч) до $5,000-10,000/мес.
- Reporting как строка в агентских ретейнерах: $200-1,000+/мес; fractional analytics ~$15-30K/год.
- Маржа: тулы $0-100/мес vs $500-1,500/мес ретейнер = 85-95% gross margin.

## 3. AI angle - credible?

Да, с guardrails:
- Официальный Google GA4 MCP server (июль 2025) - Data+Admin API для Claude/Gemini/ChatGPT.
- Готовые n8n-шаблоны: GA4→BigQuery backfill + Telegram; "AI marketing report (GA+Ads+Meta), LLM пишет summary+narrative, email/Telegram" (n8n template 2783).
- Паттерн практиков: BigQuery = source of truth, n8n = оркестратор, LLM = нарратив.
- "Agent-written report" = замена дашбордов 2026; человек ~20 мин review на клиента.

Pitfalls (= моат сервиса):
- Галлюцинированные цифры/атрибуция. Митигация: числа считаются детерминированно (SQL/API), LLM только нарратив поверх verified aggregates.
- Data quality upstream: 48% говорят, что единое определение метрик больше всего улучшит доверие. Metric-definition workshops = billable.
- LLM корреляционны, не каузальны. Только 13% маркетологов полностью доверяют AI без человека = продающая история human-verified сервиса.

## 4. RF/CIS

- Roistat: тарифы от ~5,900 ₽/мес; внедрение от 25,000 ₽. Calltouch от 990 ₽/мес.
- Агентства (i-Media): дашборд от 25K ₽, расширенный от 50K ₽, сквозная аналитика под ключ от 70K ₽, ведение от 20K ₽/мес. DataLens внедрение от 20K ₽.
- Kwork floor: Roistat setup 500-2,000 ₽; полный цикл под ключ 37,000 ₽.
- AI-native reporting services в РФ ещё не crowded: рынок = либо tool setup, либо полный аутсорс маркетинга.
- RF-чеки в 5-10x ниже USD; играть в monthly ведение + ИИ-отчёты (20-40K ₽/мес), не в setup. 152-ФЗ: client-side deployment = ответ.

## 5. Fit (2 чел × 10-15 ч/нед)

- Аудит: 6-12ч. Dashboard/pipeline setup: 15-30ч. Monthly AI reporting retainer после автоматизации: 2-4 ч/клиент/мес.
- Ёмкость: ~60-80 delivery-часов/мес → 1-2 setup в работе + 4-8 reporting-ретейнеров. $2-8K MRR только с этой линии.
- Риски: data access friction (чеклист доступов); клиенты спорят с цифрами (metric-definition sign-off ДО постройки; обещать "one agreed number", не "true ROI"); hallucinated insights (детерминированные числа + human review); scope creep (cap N изменений/мес); commodity floor (конкурировать recurring insight-слоем, не ценой setup).

## Takeaways

1. Спрос структурный: SMB не могут нанять аналитика, покупают результат.
2. Боль оцифрована: 5-10 ч/мес ручного репортинга = чистый ROI-питч.
3. Маржа 85-95%.
4. Стек commodity с mid-2025 (GA4 MCP, n8n шаблоны) - поднять за дни.
5. Инкумбенты валидируют, но wedge = "AI speed + human accountability".
6. Trust risk = дифференциатор (детерминированная архитектура = safety + sales story).
7. RF: якоря setup 25-70K ₽, ведение от 20K ₽/мес.
8. Аналитика = лучший троян портфеля: каждая находка аудита = scoped upsell в другие линии; генерирует цифры для кейсов.
9. Второй покупатель = агентства (white-label reporting).
10. AEO/AI-visibility reporting = natural bolt-on (Peec $95-245/мес, Profound $499+/мес → место для service-wrapped слоя).

## Offer ladder

| Ступень | Оффер | Global | RF | Часы |
|---|---|---|---|---|
| 1. Entry | Marketing Analytics Audit | $500-1,500 | 25-50K ₽ | 6-12ч |
| 2. Project | Dashboard + pipeline setup | $2,000-6,000 | 50-150K ₽ | 15-30ч |
| 3. Recurring | AI Reporting Retainer (weekly digest + monthly LLM-narrative + anomaly alerts, human-reviewed, + call) | $500-1,500/мес | 20-45K ₽/мес | 2-4ч/мес |
| 4. Upsell | Automation/AEO/content проекты из данных; AI-visibility add-on | $150-400/мес addon | 10-30K ₽/мес | varies |

Позиционирование: "Your dashboards tell you what happened. We deliver the why and what to do - every Monday morning, verified by a human." Первая цель: агентства 2-5 чел и SMB с ad spend $5-30K/мес.

Ключевые источники: mordorintelligence.com, deliveredsocial.com, databox.com/ai-marketing-analytics, swydo.com, digitalapplied.com/blog/agency-client-reporting-automation-2026, n8n.io/workflows/2783, i-media.ru/web-analytics, kwork.ru, surmado.com/blog/best-ai-visibility-tools-2026.
