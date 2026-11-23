# Еко-освіта UA

Інтерактивна екологічна карта України та серія з 5 навчальних стендів: класифікація і маркування відходів, екознаки, екологічна безпека підприємства, утилізація відходів виробництва, енергоефективність.

**Сайт:** https://d-almazov.github.io/eco-edu-ua/

## Що всередині

| Сторінка | Файл |
|---|---|
| Головна | `index.html` |
| Екологічна карта України | `map.html` |
| Стенд 1. Класифікація та маркування відходів | `stands/waste-classification.html` |
| Стенд 2. Екологічні знаки та екомаркування | `stands/ecolabels.html` |
| Стенд 3. Екологічна безпека підприємства | `stands/enterprise-safety.html` |
| Стенд 4. Утилізація безпечних відходів виробництва | `stands/industrial-waste-recycling.html` |
| Стенд 5. Енергоефективність та альтернативна енергетика | `stands/energy-efficiency.html` |

```
assets/
  css/     base.css (спільне), fonts.css, home.css, map.css, stand.css
  js/      map.js (дані й логіка карти), ukraine-regions.js (контури областей)
  fonts/   Golos Text, Unbounded (woff2)
  favicon.svg
```

Сайт статичний: без збирання, фреймворків і залежностей. Відкрийте `index.html` у браузері, і все працює.

## Публікація на GitHub Pages

1. Репозиторій → **Settings** → **Pages**.
2. **Source:** Deploy from a branch.
3. **Branch:** `main`, папка `/ (root)` → **Save**.
4. За хвилину-дві сайт з'явиться за адресою `https://<ваш-логін>.github.io/eco-edu-ua/`.

Файл `.nojekyll` вимикає обробку Jekyll, щоб GitHub віддавав файли як є.

## Друк стендів

Кожен стенд має кнопку «Друк / PDF (A4)» і вміщується на один аркуш A4. У вікні друку увімкніть «Фонову графіку» (Background graphics). Для великого формату (A2, A1) збережіть PDF і масштабуйте в друкарні.

## Як редагувати

- **Текст стенду** правиться прямо в HTML-файлі в папці `stands/`.
- **Дані карти** лежать на початку `assets/js/map.js`:
  - `D`: області (назва, лісистість %, рівень техногенного навантаження 0–3, ключові проблеми);
  - `PTS`: позначки (тип `pzf` — заповідник, `hot` — загроза; назва; широта; довгота; область; опис);
  - `RIV`: річки.
- **Кольори і шрифти** задаються в `assets/css/base.css` та `assets/css/stand.css`.

## Джерела даних

- Закон України «Про управління відходами» № 2320-IX; постанова КМУ № 1102 від 20.10.2023 (Національний перелік відходів).
- ДСТУ ISO 14001, 14020–14025, 50001; Регламент ЄС 2017/1369; система GHS ООН.
- IPCC AR5 (2014), WG III, Annex III: викиди CO₂ за життєвий цикл.
- Оцінки техногенного навантаження і лісистості на карті орієнтовні (узагальнено з відкритих даних Держстату, Держлісагентства, Міндовкілля). Шкода довкіллю від війни: [ecozagroza.gov.ua](https://ecozagroza.gov.ua/).

## Ліцензії сторонніх матеріалів

- Контури областей: [svg-maps/ukraine](https://github.com/VictorCazanave/svg-maps/tree/master/packages/ukraine), автор Olesia Ladanai, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- Шрифти [Golos Text](https://github.com/googlefonts/golos-text) і [Unbounded](https://github.com/googlefonts/unbounded): SIL Open Font License 1.1 (тексти ліцензій лежать в `assets/fonts/`).
