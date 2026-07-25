# Стратегический драфт: AI Marketing Automation Venture (Mikhail + Anna)
Дата: июль 2026. Основа: 8 research-дайджестов + 3 red-team вердикта (market-reality: survives; competition: fail; execution: fail).

---

## 1. Вердикт по venture thesis

**GO-WITH-CHANGES.** Гипотеза services-first подтверждена рынком, но в исходной форме план дважды не пережил red-team. Изменения обязательные, не косметические.

**Что подтверждено данными:**
- Платформенный путь (flow B, «свой Jasper») закрыт: Jasper выжил только уходом в enterprise (валюация срезана до ~$1.2B, 4+ раунда лэйоффов — https://www.maginative.com/article/jasper-cuts-internal-valuation-as-ai-growth-slows/), Copy.ai куплен Fullcast (окт 2025 — https://www.prnewswire.com/news-releases/fullcast-announces-the-acquisition-of-copyai-302584121.html), Icon.com рухнул к марту 2026 несмотря на Founders Fund и домен за $12M (https://www.ctol.digital/news/icon-com-12m-domain-human-ads-ai-startup-collapse-investors-2026/).
- Implementation gap реален и оплачиваем: ~88% adoption AI, но только ~6% извлекают ценность; 74% не могут масштабировать value (Gartner CMO Spend 2026); Salesforce Agentforce — <10% attach на базе 150K+ клиентов (https://www.eesel.ai/blog/is-salesforce-agentforce-worth-the-cost). Даже гиганты не могут развернуть агентов self-serve — это и есть TAM услуг.
- Ценовая «мертвая зона» существует: между $59/mo (Jasper Pro) и $100K+/yr (Typeface, Agentforce) никто не ставит И не оперирует AI-маркетинг-систему за $1-5K/mo.

**Обязательные изменения (из red-team):**
1. **Решить контрактно-платежный вопрос ДО любого EN-аутрича.** RU-нексус — структурный блокер для лицензированных crypto/fintech клиентов (vendor onboarding, KYC) и для платежных рельсов (Stripe/Upwork/PayPal/Wise закрыты для RU-резидентов). Варианты: Anna фронтит контракты (если она вне РФ), юрлицо в KZ/AM/UAE, либо стейблкоины для crypto-native клиентов. Если нерешаемо — venture официально пересобирается как RU/CIS-first с перецененными ожиданиями.
2. **Убить генералистское меню.** Не «SMM, PR, Content, SEO, agents по запросу», а 2 именованные системы с baseline→after KPI: AEO/GEO (метрика: citation share) и Content Engine (метрика: cost per published asset). Слово «AI automation» из питча убрать — 305K+ участников только в одном Skool-комьюнити Liam Ottley продают то же самое (https://communityhunter.com).
3. **90-дневная валидация = только async fixed-scope продукты** (платные аудиты + 2-4-недельные спринты с жестким концом). Retainer'ы и always-on системы — только после триггера по capacity: оба фаундера part-time, incident response невозможен, а maintenance = ~80% lifecycle cost автоматизаций.
4. **Партнерское соглашение с explicit-триггером «Mikhail выходит на фултайм»** (его цель — signed offer в августе). Без прописанной ветки контингенции план нежизнеспособен.
5. **B2B SaaS аутрич начинать с месяца 1, не 3** — крипта в H1 2026 в даун-цикле (лэйоффы Coinbase, Kraken, Gemini), валидация не должна висеть на одном секторе.

---

## 2. Рынок: Global vs РФ/СНГ

**Рекомендация: двухполосная схема с гейтом на день 45.**

- **EN платит 3-5x за идентичную работу**: GEO-ретейнеры $3-15K/mo (https://thedigitalelevator.com/blog/aeo-and-geo-pricing-guide/) против 60-150K ₽/mo в РФ (https://vc.ru/ai/3007956-prodvizhenie-v-neyrosetyah-tseny-i-modeli). Стратегически значимый рынок — EN.
- **Но EN-полоса условна**: она открывается только после решения entity/payment-вопроса (п.1 выше). До этого EN-аутрич — потеря времени и сжигание теплого нетворка.
- **РФ — cash-flow и валидационная полоса, не стратегия**: пилоты 100-200K ₽ закрываются за недели, Kwork-инфраструктура у Mikhail уже live (уникальный ассет), «продвижение в нейросетях» — сформированная категория (~15 агентств, медиана ретейнера ~150K ₽/mo, Sostav: https://www.sostav.ru/blogs/286072/82723). Но чеки в 3-5x ниже, и часы тут не строят EN-кейс. Кап: ~30-40% capacity.
- **Гейт (hard tripwire из red-team):** если к дню 45 ноль платных EN-аудитов — весь capacity переключается на RU-пилоты, EN-полоса становится «проблемой 2027 года», условной на entity-фикс.

РФ-специфика как фича, а не баг: OpenAI заблокирован (RU IP/карты/ключи), managed-доступ через ProxyAPI/AITUNNEL или YandexGPT (152-ФЗ) / GigaChat / DeepSeek — само по себе продаваемая услуга (https://vc.ru/promptra/2962649-openai-api-v-rossii-kak-rabotat-bez-vpn).

---

## 3. ICP: топ-2 сегмента

### ICP #1 — Crypto/Fintech B2B infra (Global EN, лид-сегмент, но с фильтром)
- **Кто:** биржи/кошельки/on-ramp, B2B crypto-инфраструктура (кастоди, платежи, compliance-tooling), fintech SaaS. 20-200 человек, seed–Series B, Dubai/EU/remote. Покупатель: Head of Marketing / CMO / founder-CEO (на seed — фаундер).
- **Боль:** paid-каналы законодательно задушены (Google — только MiCA-авторизованные CASP в EU; Meta — 3-уровневая авторизация с марта 2026), organic + AI-search visibility = единственный канал. AI-поиск уже измеряемое поле боя: Coinbase+Kraken забирают ~22% всех US crypto AI-цитирований, ChatGPT рекомендует Coinbase в 85% exchange-запросов — все ниже топ-5 невидимы и знают это (https://www.prnewswire.com — 5WPR Crypto AI Visibility Index). Плюс compliance-bottleneck: 68% команд с GenAI at scale упираются в QA/legal-ревью за 2 квартала.
- **Чек:** crypto-агентства берут $3-6K/mo entry, $10-50K/mo full-service — специализированный line item $2.5-8K/mo продается легко относительно того, что они уже платят.
- **Канал:** теплый нетворк EMCD/Choise + LinkedIn 1st/2nd degree (reach-система и person-map уже построены), Telegram-чаты крипто-фаундеров, aeo-audit teardown как door-opener DM.
- **Фильтр (red-team):** только licensed/funded/revenue-positive игроки; сектор в даун-цикле — квалифицировать бюджеты жестко. Ниша уже занята incumbents с кейсами (Victoria Olsina, Coinbound, NinjaPromo) — не конкурировать со strategy-слоем, а продавать implementation-спринты (см. п.5).

### ICP #2 — B2B SaaS seed–Series B (Global EN, scale-сегмент, старт с месяца 1)
- **Кто:** B2B SaaS, 10-100 сотрудников, $1-20M ARR, US/EU/remote. Покупатель: VP Marketing / Head of Growth / founder-CEO.
- **Боль:** buying committees ресерчат вендоров через ChatGPT/Perplexity до первого sales-касания; AI Overviews триггерятся на 48% запросов; классический SEO-трафик падает. Агентства категории стоят $8-25K/mo — недоступно; DIY-инструменты не работают (77% SMB без prompting-стратегии).
- **Чек:** $2.5-5K/mo — ровно в документированной мертвой зоне между $59/mo тулами и $8K+/mo агентствами.
- **Канал:** LinkedIn build-in-public (posting machine у Mikhail уже есть), 2nd-degree интро из fintech-нетворка, Indie Hackers/RevGenius. Цикл 2-3 месяца — потому старт сразу.

**RU-полоса (не ICP, а лейн):** e-commerce/D2C и B2B-сервисы с высоким потоком заявок, 100M-2B ₽ выручки. Вход через Kwork (AI-agent гиги 80-300K ₽) + VC.ru кейс-статья + Telegram. ~50% РФ SMB конвертятся на кейсах с ROI-цифрами, не на демо (https://kod.ru/bariery-vnedrieniya-ai-v-malom-i-srednem-biznese).

---

## 4. Оффер и pricing: лестница

Продаем **только 2 именованные системы** (AEO/GEO Implementation + Content Engine; SMM Autopilot и PR/Outreach — в бэклог до клиента #3). Никогда не «AI automation», никогда не «unlimited».

| Ступень | Global (EN) | РФ | Скоуп |
|---|---|---|---|
| **T0. AI Visibility Snapshot** | free | free | 1-страничный teardown: как бренд выглядит в ChatGPT/Perplexity/AI Overviews (+Алиса/YandexGPT для РФ) на 5-10 buyer-запросах + 3 фикса. Loom/PDF в DM. Кап 1-2 ч, генерится из aeo-audit skill |
| **T1. Paid Audit** (валидационный продукт) | $1,500–2,500 | 60–90K ₽ | 20-30 запросов, citation-share vs конкуренты, техпасс (schema, answer-first структура), off-site карта (Reddit = 40.1% LLM-цитирований), приоритизированный 90-дневный roadmap. 5-10 рабочих дней. Рынок: аудиты $1-5K (https://www.stackmatix.com/blog/aeo-services-pricing) |
| **T2. Pilot Sprint** (2-4 нед, fixed scope) | $3,500–6,000 | 100–200K ₽ | Одна именованная система под ключ на инфре клиента + runbook + baseline-метрика. 50% стоимости аудита зачитывается при букинге за 30 дней. РФ-цена = установленная рыночная ступень «платный пилот» (https://vc.ru/ai/2791769-stoimost-ii-agenta-dlya-biznesa) |
| **T3. Retainer** (только после capacity-триггера) | $2,500–5,000/mo (AEO Growth); $1,500–2,500/mo (run) | 80–150K ₽/mo | 4-6 оптимизированных ассетов/мес + schema + мониторинг + monthly report vs KPI. Рыночный band: GEO mid-market $2-8K/mo (https://gigawattgroup.com/insights/geo-aeo-pricing-models-what-agencies-charge-in-2026/) |

**Контрактные правила:**
- Flat fee, outcome-framed, но НЕ outcome-priced (attribution-риск для шопа без трек-рекорда). KPI в каждом SOW.
- API/модельные косты — pass-through на ключах клиента (5-10x token variance съест маржу; плюс снимает недоверие к credit-биллингу платформ).
- IP: клиент владеет задеплоенными workflow/промптами на своей инфре (self-hosted n8n, свои ключи) — продавать открыто как anti-lock-in. Venture оставляет background IP и reusable-шаблоны через non-exclusive license-back (это легальный фундамент будущего продукта).
- Scope: 2 раунда правок, explicit «not included», pre-written change-order с квотой за 24 ч.
- Capacity: max 1 спринт одновременно, очередь как фича.

**Математика 90 дней:** 2-3 аудита + 1 спринт ≈ $6.5-9K выручки за ~60-80 delivery-часов — внутри конверта 10-15 ч/нед на фаундера.

---

## 5. Позиционирование и отстройка

**Формула:** «Мы ставим и измеряем AI-маркетинг-систему на ВАШЕМ стеке. Вы владеете всем. Flat fee. ROI по каждому workflow — или честно говорим, что AI тут не поможет.»

Это прямой антидот к: (а) Gartner-прогнозу отмены 40%+ agentic-проектов к 2027 (https://newmarketpitch.com/blogs/news/agentic-ai-funding-analysis), (б) недоверию к credit-биллингу платформ (Copy.ai Trustpilot 1.9/5), (в) sub-$3K «GEO»-офферам, которые рынок уже считает перелейбленным SEO.

**Честный ответ «почему мы, а не 1000 AI-агентств»:**
1. **Мы сидели в вашем кресле.** Оба фаундера шипили маркетинг внутри крипто-компании (EMCD/Choise). Generic-агентства не понимают MiCA/certification-ограничения и производят compliance-небезопасный копирайт. Compliance-baked-in content pipeline — deliverable, который AAA-толпа физически не может продать.
2. **Мы продаем implementation, а не мониторинг.** Profound/Peec/Otterly говорят ГДЕ вы теряете AI-видимость за $29-99/mo; мы исполняем fix-list. Позиционируемся ПОД strategy-инкумбентами (Olsina) и НАД тулами — партнерство с тулами, не конкуренция.
3. **Anti-hype фильтр как оффер.** «Убиваем AI-проекты, которые не должны существовать» — отстройка от AAA-хорды через отказ. Каждый оффер привязан к одному измеренному baseline→after KPI.
4. **Anti-lock-in.** Все работает на инфре клиента и продолжает работать без нас. «Красный флаг 2026 buyer-гайдов — агентство, не отвечающее, кто владеет кодом и аккаунтами» (https://getuplift.ai/blog/ai-automation-agency).

**Red-team поправка:** implementation-moat имеет half-life 12-18 месяцев (Profound Agents, AirOps уже автоматизируют monitor→fix→publish). Якорить deliverables в том, что платформы не могут: off-site authority (Reddit/PR/entity), compliance-safe копирайт, кросс-канальная стратегия. n8n-워크플оу — plumbing, не продукт.

---

## 6. GTM на $0

**Правило из red-team: ОДИН канал дистрибуции, еженедельный ship, канальные часы приоритетнее delivery-часов до сделки #2.**

- **Основной канал: LinkedIn build-in-public (EN).** У Mikhail уже есть: posting machine, reach-система, person-map, comment engine, voice corpus. Формат: публичные unsolicited AEO-teardowns известных crypto/fintech брендов (playbook Olsina) — proof manufacturing за 30 дней без клиентов.
- **Warm DM (не канал, а спусковой крючок):** 10-15 таргетов из EMCD/крипто-нетворка, teardown-в-DM через Telegram/LinkedIn. Единственный путь к EN-сделке внутри 90 дней — cold email в этой нише мертв (бизнесы получают AI-agency питчи ежедневно).
- **Dogfooding как proof:** добиться цитирования собственного сайта venture в ChatGPT/Perplexity по своей категории, каждый питч открывать этим скриншотом.
- **RU-лейн:** Kwork (инфра live, autopilot есть, кап 5/день) + одна VC.ru кейс-статья с ROI-цифрами (де-факто lead-gen поверхность категории) + Telegram-личный бренд Anna/Mikhail.
- **НЕ делать:** cold email, обе платформы контента сразу (LinkedIn EN ИЛИ VC.ru RU — выбор зависит от гейта дня 45), конференции до первого кейса.

---

## 7. План 90 дней

**Pre-flight (неделя 0, блокирующая):** партнерское соглашение + entity/payment-решение + dry-run передачи delivery Anna (см. п.8). Без этого не стартовать.

- **Недели 1-2:** одностраничник 2 систем + sales-страница аудита; шаблон аудита (цель: <8 ч на аудит к третьему); список 15 crypto/fintech таргетов (фильтр licensed/funded) + 10 B2B SaaS таргетов; 2 Kwork-гига опубликованы; первый публичный teardown на LinkedIn.
- **Недели 3-4:** 10-15 warm DM с бесплатными snapshot'ами; еженедельный LinkedIn-пост (teardown-формат); первый RU-лид с Kwork в работе. **Milestone: 1 платный аудит продан к концу недели 4** (EN $1,500 или RU 60-90K ₽).
- **Недели 5-6:** delivery аудитов #1-2; параллельно B2B SaaS DM-волна. **День 45 — ГЕЙТ:** ноль платных EN-аудитов → весь capacity на RU-пилоты, EN замораживается до entity-фикса.
- **Недели 7-10:** конверсия аудита в спринт ($3.5-6K / 100-200K ₽, зачет 50% аудита); delivery спринта #1; продолжается weekly ship в канал.
- **Недели 11-13:** завершение спринта, замер baseline→after; кейс с цифрами (EN LinkedIn-пост или VC.ru статья — по итогу гейта); предложение retainer'а клиенту спринта ТОЛЬКО если capacity-триггер выполнен (один фаундер 20+ ч/нед); иначе — второй спринт/аудит.

**Milestone успеха (день 90):** 1 EN-клиент (аудит+спринт, $5-8.5K) ИЛИ 2 RU-пилота (200-400K ₽). EN-клиент = стратегически значимый исход; 2 RU-пилота = валидация с пониженной планкой.

---

## 8. Зафиксировать ДО старта

1. **Партнерское соглашение (письменно):** committed hours/нед каждого; split sales vs delivery; equity/vesting; **explicit trigger-clause «Mikhail принимает фултайм-оффер»** (варианты: пауза venture / Anna фронтит / скоуп падает до audits-only); условия выхода.
2. **Юрструктура и деньги:** кто может выставлять USD/EUR-инвойсы (Anna? третья страна: KZ/AM/UAE?); стейблкоин-рельсы для crypto-native; для РФ — самозанятость/ИП с лицензионным приложением. **Это блокер #1 из двух red-team лензов.**
3. **Bus factor:** cross-train Anna на delivery-стек ИЛИ сузить ее роль до sales/CS с Mikhail-независимым аудит-тулингом; один dry-run handoff до клиента #1. Верифицировать реальные часы и технические способности Anna — сейчас это assumption.
4. **Операционные дефолты в каждой системе до продажи:** degradation-safe (queue-and-hold вместо автопубликации при аномалии), health-check алерты в Telegram обоим, written next-business-day SLA (продается как async-фича), runbook исполнимый Anna без Mikhail.
5. **Бренд:** имя/домен/сайт-одностраничник; НЕ использовать label «AI marketing automation agency»; сайт сразу строить под AEO (dogfooding).
6. **Инструменты:** Otterly ($29/mo) или Peec ($95/mo) как monitoring-input; n8n self-hosted у клиента; ключи клиента (OpenAI/Anthropic глобально; ProxyAPI/YandexGPT/GigaChat для РФ). Стартовый tooling-бюджет <$150/mo.

---

## 9. Метрики и kill-criteria

**Метрики недели:** DM отправлено / snapshot доставлено / аудитов продано / delivery-часы / канальные публикации (1/нед минимум).

**Kill-criteria (гипотеза невалидна):**
- **День 45:** 0 платных EN-аудитов → kill EN-полосы (не venture), пивот на RU-only.
- **День 90:** 0 платных клиентов на обоих рынках при ≥30 warm DM и ≥8 опубликованных proof-ассетах → гипотеза «services-first AI marketing» невалидна для этой пары в этой конфигурации; stop.
- **Качественные kill-сигналы:** (а) 3+ EN-сделки умерли именно на vendor onboarding/KYC из-за RU-нексуса при нерешаемом entity-вопросе; (б) Mikhail подписал фултайм и триггер-clause сработал без жизнеспособной Anna-фронт ветки; (в) конверсия snapshot→платный аудит <5% на 30+ доставленных snapshot'ах (означает: оффер не бьет в боль либо доверия нет).
- **Anti-kill оговорка:** долгий B2B-цикл (2-3 мес для SaaS) — не kill-сигнал, если есть живой пайплайн (2+ сделки в стадии proposal к дню 90).

---

## 10. Путь services → product

**Правило Jasper-теста перед любым продуктовым шагом:** «Если модельный провайдер завтра шипнет мой use case бесплатно — что останется?» Допустимые ответы для 2 человек: proprietary workflow-данные, vertical depth, клиентские отношения (https://www.growthhunt.ai/growth-story/jasper).

**Триггеры продуктизации (все три, не раньше):**
1. ≥3 повторяемых delivery ОДНОЙ И ТОЙ ЖЕ системы (playbook forward-deployed engineering);
2. шаблонная библиотека покрывает ~70% delivery (license-back clause из п.4 легально ее накапливает);
3. $10K+ MRR на retainer'ах (типично месяцы 6-12; медиана рынка 8-12 мес до $10K MRR).

**Что продуктизировать (в порядке вероятности):**
1. **Audit report generator** — внутренний тул по пути Surfer SEO (агентский инструмент → SaaS): автоматизированный AEO-аудит crypto/fintech как self-serve продукт $99-299 разово или $99/mo мониторинг+fix-list. Vertical depth = защита.
2. **Compliance-gated content pipeline** как named methodology → вертикальный SaaS для regulated finance (паттерн «31 из 40 агентских клиентов переведены на $299-799/mo платформу, $2.7M ARR за 28 мес» — https://www.mindstudio.ai/blog/start-ai-automation-business-case-studies).
3. **НИКОГДА:** general-purpose «Jasper для X» — wrapper-economics trap, подтвержденная самим Jasper.

**Мост:** сервисные клиенты = первая когорта продукта. До триггеров — только шаблоны внутри delivery, никакой разработки «на будущее» (YAGNI).

---

### Сводка изменений vs исходная гипотеза
| Было | Стало |
|---|---|
| «AI-трансформация маркетинга» (широкое меню) | 2 именованные системы с KPI (AEO/GEO + Content Engine) |
| Global + РФ параллельно | Двухполосная схема с гейтом дня 45; EN условен на entity-фикс |
| Retainer'ы с первого клиента | Только async fixed-scope (аудит+спринт) до capacity-триггера |
| Crypto-first, SaaS с месяца 3 | Crypto warm + SaaS с месяца 1 параллельно |
| Старт немедленно | Блокирующая неделя 0: соглашение + платежные рельсы + handoff dry-run |