---
title: <img>
slug: Web/HTML/Reference/Elements/img
---

{{HTMLSidebar}}

**HTML-элемент `<img>`** встраивает изображение в документ. Это [замещаемый элемент](/ru/docs/Web/CSS/CSS_images/Replaced_element_properties).

{{InteractiveExample("HTML Demo: &lt;img&gt;", "tabbed-standard")}}

```html interactive-example
<img
  class="fit-picture"
  src="/shared-assets/images/examples/grapefruit-slice.jpg"
  alt="Grapefruit slice atop a pile of other slices" />
```

```css interactive-example
.fit-picture {
  width: 250px;
}
```

Приведённый выше пример показывает очень простое использование элемента `<img>`. Атрибут `src` обязателен и содержит путь к изображению, которое вы хотите встроить в документ. Атрибут `alt` содержит текстовое описание изображения, которое не обязательно, но невероятно полезно для доступности — программы чтения с экрана читают это описание своим пользователям, так они знают какое изображение показано, и так же оно отображается на странице, если изображение не может быть загружено по какой-либо причине.

Есть много других атрибутов, которые могут быть указаны для достижения различных целей, например:

- управление Referrer/CORS в целях безопасности. Смотрите ниже атрибуты `crossorigin` и `referrerpolicy`;
- настройка {{glossary("Intrinsic Size", "внутреннего размера")}} с использованием `width` и `height`, которые полезны, когда вы хотите задать пространство занимаемое изображением, чтобы обеспечить стабильность макета страницы перед его загрузкой;
- адаптивные изображения рекомендуется использовать с атрибутами `sizes` и `srcset` (смотрите также элемент {{htmlelement("picture")}} и наше руководство "[Адаптивные изображения](/ru/docs/Web/HTML/Guides/Responsive_images)").

| [Категории контента](/ru/docs/Web/HTML/Guides/Content_categories) | [Потоковый контент](/ru/docs/Web/HTML/Guides/Content_categories#потоковый_контент), [фразовый контент](/ru/docs/Web/HTML/Guides/Content_categories#phrasing_content), [встроенный контент](/ru/docs/Web/HTML/Guides/Content_categories#встроенный_контент), [явный контент](/ru/docs/Web/HTML/Guides/Content_categories#явный_контент). Если элемент имеет атрибут `usemap`, он так же принадлежит к категории [интерактивного контента](/ru/docs/Web/HTML/Guides/Content_categories#интерактивный_контент). |
| ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Допустимое содержимое                                             | Никакое, так как это {{Glossary("empty element", "пустой элемент")}}.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Пропуск тегов                                                     | Должен иметь открывающий тег и не должен иметь закрывающий.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Допустимые родители                                               | Любой элемент, который разрешает встроенный контент в качестве содержимого.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Допустимые ARIA-роли                                              | Любые                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DOM-интерфейс                                                     | {{domxref("HTMLImageElement")}}                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## Поддерживаемые форматы изображений

Стандарт HTML не содержит списка форматов изображений, которые должны поддерживаться. Поэтому разные {{glossary("user agent","пользовательские агенты")}} поддерживают разные наборы форматов.

### Firefox

Форматы изображений, поддерживаемые Firefox:

- [JPEG](https://ru.wikipedia.org/wiki/JPEG);
- [GIF](https://ru.wikipedia.org/wiki/GIF), включая анимированные GIF;
- [PNG](https://ru.wikipedia.org/wiki/PNG);
- [APNG](/ru/docs/Animated_PNG_graphics);
- [SVG](/ru/docs/Web/SVG);
- [BMP](https://ru.wikipedia.org/wiki/BMP);
- [BMP ICO](<https://ru.wikipedia.org/wiki/ICO_(%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%82_%D1%84%D0%B0%D0%B9%D0%BB%D0%B0)>);
- [PNG ICO](<https://ru.wikipedia.org/wiki/ICO_(%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%82_%D1%84%D0%B0%D0%B9%D0%BB%D0%B0)>).

## Ошибки загрузки изображения

Если ошибка происходит во время загрузки или отрисовки изображения и обработчик события [`onerror`](/ru/docs/Web/HTML/Reference/Global_attributes#onerror) был настроен на обработку события [`error`](/ru/docs/Web/API/HTMLElement/error_event), тогда этот обработчик события будет вызван. Это может произойти в ряде ситуаций, в том числе когда:

- атрибут `src` пустой или {{glossary("null")}};
- указанный {{glossary("URL")}} в атрибуте `src` совпадает с URL страницы, на которой в данный момент находится пользователь;
- указанное изображение каким-то образом повреждено, что препятствует его загрузке;
- метаданные указанного изображения повреждены таким образом, что невозможно получить его размеры, и в атрибутах элемента `<img>` не было указано никаких размеров;
- указанное изображение имеет формат, который не поддерживается {{Glossary("user agent", "пользовательским агентом")}}.

## Атрибуты

К этому элементу применимы [глобальные атрибуты](/ru/docs/Web/HTML/%D0%9E%D0%B1%D1%89%D0%B8%D0%B5_%D0%B0%D1%82%D1%80%D0%B8%D0%B1%D1%83%D1%82%D1%8B).

- `alt`
  - : Этим атрибутом задаётся альтернативное текстовое описание изображения.
    > [!NOTE]
    > Браузеры не всегда отображают изображение на которое ссылается элемент. Это относится к неграфическим браузерам (включая те, которые используются людьми с нарушениями зрения), если пользователь решает не отображать изображения, или если браузер не может отобразить изображение, потому что оно имеет неверный или [неподдерживаемый тип](#supported_image_formats). В этих случаях браузер может заменить изображение текстом записанным в атрибуте `alt` элемента. По этим и другим причинам вы должны по возможности предоставлять полезное описание в атрибуте `alt`.
    > [!NOTE]
    > Пропуск этого атрибута в целом указывает, что изображение является ключевой частью контента и текстовый эквивалент не доступен. Установка этого атрибута в значение пустой строки (`alt=""`) указывает, что это изображение _не_ является ключевой частью контента (декоративное), и что невизуальные браузеры могут пропустить его при {{glossary("Rendering engine", "рендеринге")}}.
- `crossorigin`
  - : Этот атрибут указывает, следует ли использовать {{glossary("CORS")}} при загрузке изображения или нет. [Изображения с включённой поддержкой CORS](/ru/docs/Web/HTML/How_to/CORS_enabled_image) могут быть повторно использованы в элементе {{HTMLElement("canvas")}} не будучи "[испорченными](/ru/docs/Web/HTML/How_to/CORS_enabled_image#security_and_tainted_canvases)". Допустимые значения:
    - `anonymous`: Запрос cross-origin (т.е. с HTTP-заголовком {{httpheader("Origin")}}) выполняется, но параметры доступа не передаются (т.е. нет {{glossary("cookie")}}, не используется [стандарт X.509](https://tools.ietf.org/html/rfc5280) или базовая HTTP-аутентификация). Если сервер не предоставляет параметры доступа исходному сайту (не устанавливая HTTP-заголовок {{httpheader("Access-Control-Allow-Origin")}}), изображение будет "[испорчено](/ru/docs/Web/HTML/How_to/CORS_enabled_image#security_and_tainted_canvases)" и его использование будет ограничено;
    - `use-credentials`: Запрос cross-origin (т.е. с HTTP-заголовком {{httpheader("Origin")}}) выполняется вместе с передачей параметров доступа (т.е. есть {{glossary("cookie")}}, используется [стандарт X.509](https://tools.ietf.org/html/rfc5280) или базовая HTTP-аутентификация). Если сервер не предоставляет параметры доступа исходному сайту (посредством HTTP-заголовка {{httpheader("Access-Control-Allow-Origin")}}), изображение будет "[испорчено](/ru/docs/Web/HTML/How_to/CORS_enabled_image#security_and_tainted_canvases)" и его использование будет ограничено.Если этот атрибут не задан, то CORS при загрузке изображения не используется (т.е. без отправки HTTP-заголовка {{httpheader("Origin")}}), ограничивая его использование в элементе {{HTMLElement("canvas")}}. Если задан неправильно, то он обрабатывается так, как если бы использовалось значение `anonymous`. Для получения дополнительной информации смотрите "[Настройки атрибутов CORS](/ru/docs/Web/HTML/Reference/Attributes/crossorigin)".
- `decoding`
  - : Предоставляет рекомендации браузеру по декодированию изображения. Допустимые значения:
    - `sync`: Декодировать изображение синхронно для одновременного отображения с другим контентом;
    - `async`: Декодировать изображение асинхронно, чтобы уменьшить задержку отображения другого контента;
    - `auto`: Режим по умолчанию, который указывает на отсутствие предпочтений к режиму декодирования. Браузер решает, что лучше для пользователя.
- `height`
  - : Внутренняя высота (см. {{glossary("Intrinsic size", "Внутренний размер")}}) изображения в пикселях.
- `importance` {{experimental_inline}}
  - : Указывает сравнительную важность ресурса. Приоритет выбирается с помощью значений:
    - `auto`: Указывает на **отсутствие предпочтений**. Браузер может использовать собственную эвристику для определения приоритета изображения;
    - `high`: Указывает браузеру, что изображение имеет **высокий** приоритет;
    - `low`: Указывает браузеру, что изображение имеет **низкий** приоритет.
- `intrinsicsize` {{experimental_inline}}
  - : Этот атрибут говорит браузеру игнорировать действительный {{glossary("Intrinsic size", "внутренний размер")}} изображения и делать вид, что это размер, указанный в атрибуте. В частности, изображение будет растровым в этих измерениях, а `narutalWidth`/`naturalHeight` изображения будут возвращать значения, указанные в этом атрибуте. [Объяснение](https://github.com/ojanvafai/intrinsicsize-attribute), [примеры](https://googlechrome.github.io/samples/intrinsic-size/index.html).
- `ismap`
  - : Это атрибут логического типа, указывающий, что изображение является частью серверной карты ссылок. Если это так, то точные координаты клика отправляются на сервер.
    > [!NOTE]
    > Этот атрибут разрешён, только если элемент `<img>` является потомком элемента {{htmlelement("a")}} с валидным (соответствующий требованиям) атрибутом [`href`](/ru/docs/Web/HTML/Reference/Elements/a#href).
- `loading` {{experimental_inline}}
  - : Указывает на то, как браузер должен загрузить изображение:
    - `eager`: Загружает изображение немедленно независимо от того, находится оно в области просмотра или нет (является значением по умолчанию).
    - `lazy`: Откладывает загрузку изображения до того момента, пока оно не достигнет подсчитанного расстояния области просмотра, определяемого браузером. Данное значение помогает избежать использования ресурсов сети и хранилища, необходимых для обработки изображения, пока это действительно не понадобится. В большинстве случаев использование этого аргумента улучшает производительность.
      > [!NOTE]
      > Загрузка откладывается только тогда, когда включён JavaScript. Это анти-трэкинг мера. Если бы пользовательский клиент поддерживал опцию отложенной загрузки изображения при отключённом JavaScript, то сайт имел бы возможность отслеживать приблизительную позицию области просмотра в течение сессии пользователя, размещая изображения на странице таким образом, чтобы сервер мог отслеживать, сколько изображений загружено и когда.
- `referrerpolicy` {{experimental_inline}}
  - : Строка, указывающая, какой реферер (referrer) использовать при выборке ресурсов:
    - `no-referrer`: Заголовок {{httpheader("Referer")}} не будет отправлен;
    - `no-referrer-when-downgrade`: Заголовок {{httpheader("Referer")}} не отправляется, когда происходит переход к источнику без {{glossary("TLS")}} ({{glossary("HTTPS")}}). Это поведение по умолчанию для {{glossary("user agent", "пользовательских агентов")}}, если не указано иное;
    - `origin`: Заголовок {{httpheader("Referer")}} будет содержать схему адресации ресурса (HTTP, HTTPS, {{glossary("FTP")}} и т.д), {{glossary("host", "хост")}} и {{glossary("port", "порт")}};
    - `origin-when-cross-origin`: Переход на другие источники ограничит включённые реферальные данные схемой адресации ресурса, {{glossary("host", "хостом")}} и {{glossary("port", "портом")}}, в то время как переход из того же источника будет включать полный путь реферала;
    - `unsafe-url`: Заголовок {{httpheader("Referer")}} будет включать источник и путь, но не фрагмент {{glossary("URL")}}, пароль или имя пользователя. Этот метод небезопасен, потому что будет утечка источников и путей от ресурсов, защищённых {{glossary("TLS")}}, к незащищённым источникам.
- `sizes`
  - : Список из одного или нескольких строк, разделённых запятыми, указывающих набор размеров источника. Каждый размер источника состоит из:1. Условия медиа-запроса. Должно быть пропущено для последнего элемента. 2. Значения размера источника.Значения размера источника устанавливаются исходя из предполагаемых размеров изображения. {{glossary("user agent", "Пользовательские агенты")}} используют текущий размер источника, чтобы выбрать один из источников, предоставленных атрибутом `srcset`, если эти источники описываются с помощью дескриптора ширины '`w`' (сокращение от width). Выбранный размер источника влияет на {{glossary("intrinsic size", "внутренний размер")}} изображения (отображаемый размер изображения, если не применены стили CSS). Если атрибут `srcset` отсутствует или не содержит значений с дескриптором '`w`', то атрибут `sizes` не будет иметь никакого эффекта.
- `src`
  - : {{glossary("URL")}} изображения. Этот атрибут является обязательным для элемента `<img>`. В браузерах, поддерживающих `srcset`, `src` обрабатывается как изображение-кандидат с дескриптором плотности пикселей `1x`, если только изображение с этим дескриптором уже не определено в `srcset` или если `srcset` не содержит дескрипторы '`w`'.
- `srcset`
  - : Список из одной или нескольких строк, разделённых запятыми, указывающих набор возможным источников изображения для использования {{glossary("user agent", "пользовательскими агентами")}}. Каждая строка состоит из:1. {{glossary("URL")}} изображения. 2. Необязательного, пробела, сопровождаемого:
    - дескриптором ширины или положительным целым числом, за которым сразу же следует '`w`'. Дескриптор ширины делится на размер источника, полученный из атрибута `sizes`, для расчёта эффективной плотности пикселей;
    - дескриптором плотности пикселей, который является положительным числом с плавающей точкой за которым сразу же следует '`x`'.Если не указано ни одного дескриптора, то источнику присваивается дескриптор по умолчанию: `1x`.Нельзя смешивать дескрипторы ширины с дескрипторами плотности пикселей в одном атрибуте `srcset`. Повторение дескрипторов (например, два источника в одном `srcset` с одинаковым дескриптором '`2x`') так же является недопустимым.{{glossary("user agent", "Пользовательские агенты")}} выбирают любой из доступных источников на своё усмотрение. Это предоставляет им значительную свободу действий для адаптации их выбора на основе таких вещей, как предпочтения пользователя или {{glossary("bandwidth", "пропускная способность")}}. Смотрите наше руководство "[Адаптивные изображения](/ru/docs/Web/HTML/Guides/Responsive_images)" для примера.

- `width`
  - : Внутренняя ширина (см. {{glossary("intrinsic size", "Внутренний размер")}}) изображения в пикселях.
- `usemap`
  - : Неполный {{glossary("URL")}} (начиная с '`#`') [карты-изображения](/ru/docs/Web/HTML/Reference/Elements/map), связанной с элементом.
    > [!NOTE]
    > Вы не можете использовать этот атрибут, если элемент `<img>` является потомком элемента {{htmlelement("a")}} или {{HTMLElement("button")}}.

### Устаревшие атрибуты

- `align`
  - : Выравнивание изображения относительно окружающему его контексту. Этот атрибут больше не должен быть использован - вместо этого используйте CSS-свойства {{cssxref("float")}} и/или {{cssxref("vertical-align")}}. Вы можете так же использовать CSS-свойство {{cssxref("object-position")}} для позиционирования изображения внутри границ элемента `<img>`. Допустимые значения:
    - `top`: Аналог `vertical-align: top` или `vertical-align: text-top`;
    - `middle`: Аналог `vertical-align: -moz-middle-with-baseline`;
    - `bottom`: Отсутствует значение по умолчанию, аналог `vertical-align: unset` или `vertical-align: initial`;
    - `left`: Аналог `float: left`;
    - `right`: Аналог `float: right`.
- `border`
  - : Ширина рамки вокруг изображения. Вы должны использовать CSS-свойство {{cssxref('border')}} вместо этого атрибута.
- `hspace`
  - : Отступ слева и справа от изображения в пикселях. Вы должны использовать CSS-свойство {{cssxref('margin')}} вместо этого атрибута.
- `longdesc`
  - : Ссылка на более подробное описание изображения. Возможными значениями являются {{glossary("URL")}} или [`id`](/ru/docs/Web/HTML/Reference/Global_attributes#id) элемента.
    > [!NOTE]
    > Этот атрибут упомянут в последней версии от {{glossary("W3C")}}, [HTML 5.2](https://www.w3.org/TR/html52/obsolete.html#element-attrdef-img-longdesc), но был удалён из [живого стандарта HTML](https://html.spec.whatwg.org/multipage/embedded-content.html#the-img-element) от {{glossary("WHATWG")}}. У него неопределённое будущее; авторы должны использовать альтернативы {{glossary("WAI")}}-{{glossary("ARIA")}}, такие как [aria-describedby](https://www.w3.org/TR/wai-aria-1.1/#aria-describedby) или [aria-details](https://www.w3.org/TR/wai-aria-1.1/#aria-details).
- `name`
  - : Имя для элемента. Вы должны использовать атрибут [`id`](/ru/docs/Web/HTML/Reference/Global_attributes#id) вместо этого атрибута.
- `vspace`
  - : Отступ сверху и снизу от изображения в пикселях. Вы должны использовать CSS-свойство {{cssxref('margin')}} вместо этого атрибута.

## Взаимодействие с CSS

`<img>` является [замещаемым элементом](/ru/docs/Web/CSS/CSS_images/Replaced_element_properties); по умолчанию он имеет значение свойства {{cssxref("display")}} равное `inline`, но его размеры по умолчанию определяются внутренними значениями (см. {{glossary("Intrinsic Size", "внутренний размер")}}) встроенного изображения. Вы можете установить на изображение такие свойства, как {{cssxref("border")}}/{{cssxref("border-radius")}}, {{cssxref("padding")}}/{{cssxref("margin")}}, {{cssxref("width")}}/{{cssxref("height")}} и так далее.

Однако, часто бывает полезно установить для изображений свойство {{cssxref("display")}} в значение `block`, так что вы имеете максимальный контроль над стилизацией (например, `margin: 0 auto` не работает на изображениях с `display: inline`, легче размещать изображения в контексте с окружающими элементами, когда они являются [блочными](/ru/docs/Glossary/Block-level_content)).

У `<img>` нет базовой линии, когда изображения используются в ситуации со строчным форматированием (`display: inline`) вместе с {{cssxref("vertical-align")}}`: baseline`, нижняя граница изображения будет размещена на базовой линии контейнера.

Вы можете использовать свойство {{cssxref("object-position")}} для позиционирования изображения внутри границ элемента `<img>` и свойством {{cssxref("object-fit")}} регулировать размеры изображения внутри этих границ (например, должно ли изображение помещаться в границы элемента или заполнить элемент полностью, даже если потребуется обрезка).

В зависимости от типа, изображение может иметь собственную (внутреннюю) ширину и высоту. Для некоторых типов изображений тем не менее {{glossary("Intrinsic Size", "внутренние размеры")}} не обязательны. {{glossary("SVG")}}-изображения, например, могут не иметь внутренних размеров, если для корня их элемента {{SVGElement("svg")}} не заданы `width` и `height`.

## Примеры

### Альтернативный текст

Следующий простой пример встраивает изображение с альтернативным текстом в страницу для улучшения доступности.

```html
<img
  src="/shared-assets/images/examples/web-docs-sprite.svg"
  alt="Логотип MDN - изображение динозавра с текстом MDN web docs" />
```

{{ EmbedLiveSample('Альтернативный_текст', '100%', '70') }}

### Изображение-ссылка

Этот пример основан на предыдущем и показывает как превратить изображение в ссылку. Это очень просто сделать так — вы вставляете тег `<img>` внутрь элемента {{HTMLElement("a")}}. Также вы должны изменить альтернативный текст, чтобы он описывал назначение ссылки.

```html
<a href="https://developer.mozilla.org">
  <img
    src="/shared-assets/images/examples/web-docs-sprite.svg"
    alt="Посетить сайт MDN" />
</a>
```

{{ EmbedLiveSample('Изображение-ссылка', '100%', '70') }}

### Использование атрибута srcset

В этом примере мы добавляем атрибут `srcset`, содержащий ссылку на версию логотипа в высоком разрешении; оно будет загружено вместо изображения в `src` на устройствах с высоким разрешением. Изображение указанное в атрибуте `src`, считается `1x` кандидатом в {{glossary("user agent", "пользовательских агентах")}}, которые поддерживают `srcset`.

```html
<img src="mdn-logo-sm.png" alt="MDN" srcset="mdn-logo-HD.png 2x" />
```

### Использование атрибутов srcset и sizes

Атрибут `src` игнорируется в {{glossary("user agent", "пользовательских агентах")}}, которые поддерживают `srcset`, когда добавлены дескрипторы '`w`'. Когда условие медиавыражения `(max-width: 600px)` совпадает с состоянием устройства, будет загружено изображение шириной 200px (оно то самое, которое наиболее близко соответствует 200px, указанным в медиавыражении), иначе будет загружено другое изображение.

```html
<img
  src="clock-demo-thumb-200.png"
  alt="Часы"
  srcset="clock-demo-thumb-200.png 200w, clock-demo-thumb-400.png 400w"
  sizes="(max-width: 600px) 200px, 50vw" />
```

## Проблемы безопасности и приватности

Хотя у элементов `<img>` есть множество безобидных применений, они могут иметь нежелательные последствия для безопасности и приватности пользователя. Смотрите "[Заголовок Referer: проблемы приватности и безопасности](/ru/docs/Web/Security/Referer_header:_privacy_and_security_concerns)" для получения дополнительной информации.

## Доступность

### Создание значимых альтернативных описаний

Значение атрибута `alt` должно чётко и кратко описывать содержимое изображения. Он не должен описывать наличие самого изображения или название файла изображения. Если атрибут `alt` намеренно пропущен, потому что изображение не имеет текстового эквивалента, рассмотрите альтернативные способы представления содержимого, которое изображение пытается передать.

#### Плохо

```html example-bad
<img alt="image" src="penguin.jpg" />
```

#### Хорошо

```html example-good
<img alt="Пингвин на пляже." src="penguin.jpg" />
```

Когда у изображения отсутствует атрибут `alt`, некоторые программы чтения с экрана могут объявить вместо него имя файла изображения. Это может привести к путанице, если имя файла не соответствует содержимому изображения.

- [Дерево решений атрибута alt • Изображения • Веб-руководство WAI по доступности](https://www.w3.org/WAI/tutorials/images/decision-tree/).
- [Альтернативные тексты: максимальное руководство — Axess Lab](https://axesslab.com/alt-texts/).
- [Как создать отличный альтернативный текст: введение | Deque](https://www.deque.com/blog/great-alt-text-introduction/).
- [MDN Понимание WCAG, Руководство 1.1. объяснения](/ru/docs/Web/Accessibility/Understanding_WCAG/Perceivable#Guideline_1.1_—_Providing_text_alternatives_for_non-text_content).
- [Понимание критерия успешного исхода 1.1.1 | W3C Понимание WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv-all.html).

### Атрибут title

Атрибут [`title`](/ru/docs/Web/HTML/Reference/Global_attributes#title) не является приемлемой заменой атрибута `alt`. Кроме того, избегайте повторения значения атрибута `alt` в атрибуте `title`, объявленном на том же изображении.

Атрибут [`title`](/ru/docs/Web/HTML/Reference/Global_attributes#title) также не должен использоваться в качестве подписи, сопровождающей альтернативное описание изображения. Если изображению нужна подпись, используйте элемент {{HTMLElement("figure")}} вместе с элементом {{HTMLElement("figcaption")}}.

- [Использование HTML-атрибута title - обновлено | The Paciello Group](https://developer.paciellogroup.com/blog/2013/01/using-the-html-title-attribute-updated/).

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- [Изображения в HTML](/ru/docs/Learn_web_development/Core/Structuring_content/HTML_images).
- [Адаптивные изображения](/ru/docs/Web/HTML/Guides/Responsive_images).
- Элементы {{HTMLElement("picture")}}, {{HTMLElement("object")}} и {{HTMLElement("embed")}}.
- Связанные с изображениями CSS-свойства: {{cssxref("object-fit")}}, {{cssxref("object-position")}}, {{cssxref("image-orientation")}}, {{cssxref("image-rendering")}}, и {{cssxref("image-resolution")}}.
