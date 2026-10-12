# VavilonAI — штат ИИ-сотрудников для Claude Code

Открытые материалы курса **VavilonAI**: правила, сотрудники, скиллы и приборы, на которых работает штат автора, и сайты, которые он собрал. У каждого — свой репозиторий с инструкцией: что это, как поставить, как устроено.

Здесь только наше. Чужие скиллы, которыми пользуются наши сотрудники, — в конце страницы, ссылками на авторов.

## Как ставить

Скилл — папка в `~/.claude/skills`:

```sh
git clone https://github.com/VavilonAI/<скилл>.git ~/.claude/skills/<скилл>
```

Сотрудник — один файл в `~/.claude/agents`:

```sh
curl -fsSL https://raw.githubusercontent.com/VavilonAI/<сотрудник>/main/<сотрудник>.md -o ~/.claude/agents/<сотрудник>.md
```

Начни со слоя 1 — шаблона штаба: он задаёт правила, по которым работают все остальные.

## Слой 1. Правила

Один файл CLAUDE.md задаёт, как ИИ работает с тобой: читать перед правкой, не выдумывать имена, проверять только с твоего «да». С него начинается всё остальное.

| репозиторий | что это | как ставить |
|---|---|---|
| [`shtab`](https://github.com/VavilonAI/shtab) | Шаблон штаба: CLAUDE.md с правилами, агент Explore, проверки, модели, ключи, передача дел | шаблон: Use this template |

## Слой 2. Сотрудники

Агент с карточкой: своя зона, своя модель, «не моё» — кому отдать. Сотрудник сам зовёт свои скиллы; основная сессия сама решает, кому отдать задачу.

| отдел | сотрудник | что делает | его скиллы |
|---|---|---|---|
| Сайты и приложения | [Ревьюер анимации](https://github.com/VavilonAI/motion-reviewer) `motion-reviewer` | Аудит производительности анимаций по проекту: оценка каждой, антипаттерны, конкретный апгрейд | — |
| Сайты и приложения | [Сайтостроитель](https://github.com/VavilonAI/site-builder) `site-builder` | Сайт целиком — от брифа до живого демо: сцены, фото заведения, тесты, выкладка на Cloudflare Pages | [`scene-site`](https://github.com/VavilonAI/scene-site) |
| Сайты и приложения | [Веб-дизайнер](https://github.com/VavilonAI/web-designer) `web-designer` | Вид и ощущение интерфейса: аудит, стиль, палитра, шрифты, полировка движения | — |
| Figma | [Дизайнер Figma](https://github.com/VavilonAI/figma-designer) `figma-designer` | Макет из Figma — в сайт и обратно, сверка токенов, проверка макета до вёрстки | [`design-to-site`](https://github.com/VavilonAI/design-to-site), [`figma-audit`](https://github.com/VavilonAI/figma-audit), [`site-to-figma`](https://github.com/VavilonAI/site-to-figma), [`tokens-sync`](https://github.com/VavilonAI/tokens-sync) |
| Тексты, визуал, монтаж | [Арт-директор](https://github.com/VavilonAI/art-director) `art-director` | Картинки и видео: референсы, брендборд, инфографика, ретушь, короткие AI-клипы | — |
| Тексты, визуал, монтаж | [Контент-продюсер](https://github.com/VavilonAI/content-producer) `content-producer` | Готовые файлы для соцсетей из утверждённого текста: карусели в PNG и MP4 | — |
| Тексты, визуал, монтаж | [Копирайтер](https://github.com/VavilonAI/copywriter) `copywriter` | Тексты, по которым действуют: лендинги, заголовки, редактура, посты, сценарии | — |
| Тексты, визуал, монтаж | [Монтажёр](https://github.com/VavilonAI/video-editor) `video-editor` | Вертикальный ролик 1080×1920 к выкладке: кадр, субтитры, безопасные поля | [`vertical-cut`](https://github.com/VavilonAI/vertical-cut) |
| Маркетинг и продажи | [Исследователь аудитории](https://github.com/VavilonAI/audience-research) `audience-research` | Кто аудитория и что ею движет, ступени осознанности, тон голоса бренда | — |
| Маркетинг и продажи | [CRO-специалист](https://github.com/VavilonAI/cro-specialist) `cro-specialist` | Конверсия: где люди уходят со страницы, из формы, онбординга; A/B-тесты | — |
| Маркетинг и продажи | [Менеджер по продажам](https://github.com/VavilonAI/sales-manager) `sales-manager` | От показа до оплаты: ответы на «подумаю» и «дорого», протокол продажи, договорённости | — |
| Маркетинг и продажи | [SEO-специалист](https://github.com/VavilonAI/seo-specialist) `seo-specialist` | Видимость в поиске: аудит, разметка, структура сайта, цитирование в AI-поиске | — |
| Маркетинг и продажи | [Стратег](https://github.com/VavilonAI/strategist) `strategist` | Маркетинговые решения: цена, оффер, запуски, реклама, воронки, письма, аналитика | — |
| Деньги и право | [Бизнес-консультант](https://github.com/VavilonAI/business-advisor) `business-advisor` | Решения о бизнесе: окупится ли, масштабировать или закрывать, разбор выписок | [`statement-import`](https://github.com/VavilonAI/statement-import) |
| Деньги и право | [Юрист](https://github.com/VavilonAI/legal-advisor) `legal-advisor` | Подготовка к разговору с юристом: договор, приём клиента, данные на сайте, риски | [`client-intake`](https://github.com/VavilonAI/client-intake), [`compliance-check`](https://github.com/VavilonAI/compliance-check), [`contract-review`](https://github.com/VavilonAI/contract-review), [`privacy-basics`](https://github.com/VavilonAI/privacy-basics) |
| Промпты и код | [Сборщик промптов](https://github.com/VavilonAI/prompt-compiler) `prompt-compiler` | Системный промпт из сырого текста или голосового — XML по стандартам Anthropic, команда /superprompt | — |
| Промпты и код | [Веб-архитектор](https://github.com/VavilonAI/web-architect) `web-architect` | Full-stack код: написать, отрефакторить, ускорить, починить; строгий TypeScript | — |

## Слой 3. Скиллы

Инструкция под одну работу: шаги, справочники, скрипты. Работает и без сотрудника — Claude зовёт скилл, когда запрос похож на его описание.

| отдел | скилл | что делает | чей сотрудник |
|---|---|---|---|
| Сайты и приложения | [`app-build`](https://github.com/VavilonAI/app-build) | Браузерное приложение без фреймворка и без шага сборки — от нуля до выкладки | — |
| Сайты и приложения | [`scene-site`](https://github.com/VavilonAI/scene-site) | Сайт заведения одной командой: сцены, найденные фото, анимация, тесты, демо на Pages | [Сайтостроитель](https://github.com/VavilonAI/site-builder) |
| Figma | [`design-to-site`](https://github.com/VavilonAI/design-to-site) | Вёрстка макета из Figma с доказательством совпадения числом | [Дизайнер Figma](https://github.com/VavilonAI/figma-designer) |
| Figma | [`figma-audit`](https://github.com/VavilonAI/figma-audit) | Проверка макета до вёрстки: контраст, цели касания, недорисованные состояния | [Дизайнер Figma](https://github.com/VavilonAI/figma-designer) |
| Figma | [`site-to-figma`](https://github.com/VavilonAI/site-to-figma) | Готовая страница сайта — в правимый кадр Figma | [Дизайнер Figma](https://github.com/VavilonAI/figma-designer) |
| Figma | [`tokens-sync`](https://github.com/VavilonAI/tokens-sync) | Сверка токенов кода и переменных Figma: цвет, отступ, радиус — одно значение | [Дизайнер Figma](https://github.com/VavilonAI/figma-designer) |
| Тексты, визуал, монтаж | [`vertical-cut`](https://github.com/VavilonAI/vertical-cut) | Вертикальный ролик 1080×1920 из любого исходника: кроп, субтитры, звук | [Монтажёр](https://github.com/VavilonAI/video-editor) |
| Деньги и право | [`client-intake`](https://github.com/VavilonAI/client-intake) | Приём клиента до первой строчки кода: анкета, объём одним письмом, красные флаги | [Юрист](https://github.com/VavilonAI/legal-advisor) |
| Деньги и право | [`compliance-check`](https://github.com/VavilonAI/compliance-check) | Проход по сайту или процессу: где могут предъявить претензию | [Юрист](https://github.com/VavilonAI/legal-advisor) |
| Деньги и право | [`contract-review`](https://github.com/VavilonAI/contract-review) | Разбор входящего договора до похода к юристу: что подписываешь и что спросить | [Юрист](https://github.com/VavilonAI/legal-advisor) |
| Деньги и право | [`privacy-basics`](https://github.com/VavilonAI/privacy-basics) | Что сайт собирает о посетителе и что об этом написать | [Юрист](https://github.com/VavilonAI/legal-advisor) |
| Деньги и право | [`statement-import`](https://github.com/VavilonAI/statement-import) | Банковские выписки и чеки — в учёт: извлечение, единый вид, дубли, сверка | [Бизнес-консультант](https://github.com/VavilonAI/business-advisor) |
| Приборы и сторожа | [`agency-catalog`](https://github.com/VavilonAI/agency-catalog) | Каталог трёхсот готовых ролей по 21 отрасли: найти нужную и поставить | — |

## Слой 4. Приборы и сторожа

Хуки и проверки, которые ловят ошибки до того, как их увидит человек.

| репозиторий | что это | как ставить |
|---|---|---|
| [`guards`](https://github.com/VavilonAI/guards) | Хуки-сторожа: субагент без модели, тихая правка секретов, кириллица в bash | плагин, одной командой |
| [`proverka`](https://github.com/VavilonAI/proverka) | Как пользоваться прибором проверки с тремя исходами: сделано, сломано, НЕ ПРОВЕРЕНО | скилл, папкой |
| [`repo-gates`](https://github.com/VavilonAI/repo-gates) | Как менять репозиторий, чтобы правка доехала и не сломалась молча | скилл, папкой |

## Готовые работы

Сайты, собранные этим штатом, — с исходниками.

| репозиторий | что это | как ставить |
|---|---|---|
| [`demo-salon`](https://github.com/VavilonAI/demo-salon) | Демо-сайт вымышленного салона: Next.js 16, статический экспорт, свои проверки | исходники сайта |
| [`demo-sites`](https://github.com/VavilonAI/demo-sites) | Пять демо-сайтов вымышленных заведений на одном генераторе: 3D, анимация, запись онлайн | исходники сайта |

## Поставить всё разом

```sh
mkdir -p ~/.claude/agents ~/.claude/skills
for s in agency-catalog app-build client-intake compliance-check contract-review design-to-site figma-audit privacy-basics proverka repo-gates scene-site site-to-figma statement-import tokens-sync vertical-cut; do
  git clone -q https://github.com/VavilonAI/$s.git ~/.claude/skills/$s
done
for a in art-director audience-research business-advisor content-producer copywriter cro-specialist figma-designer legal-advisor motion-reviewer sales-manager seo-specialist site-builder strategist video-editor web-architect web-designer; do
  curl -fsSL https://raw.githubusercontent.com/VavilonAI/$a/main/$a.md -o ~/.claude/agents/$a.md
done
```

Плагины (`guards`, `prompt-compiler`) ставятся своей командой — она на их страницах.

## Чужие скиллы, которыми пользуются наши сотрудники

Не наши: код, права и поддержка — у авторов. Ставить по их инструкциям; наши сотрудники находят скилл по имени.

| набор | автор | лицензия | кто из наших пользуется или зачем |
|---|---|---|---|
| [marketingskills](https://github.com/coreyhaines31/marketingskills) | Corey Haines | MIT | CRO-специалист, SEO-специалист, `scene-site`, Копирайтер, Стратег |
| [taste-skill](https://github.com/Leonxlnx/taste-skill) | Leon Lin (Leonxlnx) | MIT | `scene-site`, Арт-директор, Веб-дизайнер |
| [emil-skills](https://github.com/emilkowalski/skills) | Emil Kowalski | MIT | Веб-дизайнер |
| [vercel-agent-skills](https://github.com/vercel-labs/agent-skills) | Vercel Labs | MIT | `scene-site`, Веб-дизайнер |
| [ui-ux-pro-max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Next Level Builder | MIT | Веб-дизайнер |
| [impeccable](https://github.com/pbakaus/impeccable) | Paul Bakaus | Apache-2.0 | `scene-site`, Веб-дизайнер |
| [motion-ai-kit](https://github.com/motiondivision/ai-kit) | Motion | MIT | Ревьюер анимации |
| [10k-websites](https://github.com/thatswyn/10k-websites) | thatswyn | MIT | `design-to-site`, `scene-site`, Сайтостроитель |
| [artithea](https://github.com/Artithea) | Artithea | MIT | `proverka` |
| [yasko](https://github.com/yasikvlad) | Влад Яско (yasikvlad) | у большинства репозиториев не указана — только ссылкой | Арт-директор, Бизнес-консультант, Исследователь аудитории, Контент-продюсер, Копирайтер, Менеджер по продажам, Стратег |
| [agency-agents](https://github.com/msitarzewski/agency-agents) | AgentLand Contributors | MIT | каталог карточек ролей, который скачивает скилл agency-catalog |
| [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | VoltAgent | MIT | образцы DESIGN.md брендов для scene-site — положить в ~/.claude/skills/scene-site/references/design-md/ |
| [proverka](https://github.com/Artithea/proverka) | Artithea | MIT | сам прибор проверки, которым пользуется скилл proverka |

## Лицензия

Наше — © 2026 VavilonAI, CC BY-NC 4.0: учиться, пользоваться и переделывать под себя со ссылкой на автора можно; продавать и включать в платные продукты нельзя. У чужого — лицензии авторов.
