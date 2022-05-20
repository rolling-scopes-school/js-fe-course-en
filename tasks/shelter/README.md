# Shelter

Shelter is the project in which you will create a markup with two pages, make it adaptive and interactive.

**[Shelter. Figma](https://www.figma.com/file/tKcmzkARtMUFQAR9VLdLkl/shelter-dom)**

## Stages of task completion

**[Week 1](#week-1)**: Static markup of the `main` page.  
**[Week 2](#week-2)**: Static markup of the `pets` page.

- at these stages, you should create a static markup for the two pages. With the fixed layout, the pages look identical if the window width is at least 1280px.

**[Week 3](#week-3)**: Responsive markup.

- at this stage, you should adapt the previously created pages according to the layout for different window sizes up to 320px.

## Task verification

- The task will be checked by the cross-check flow. **There will be 3 checks in total, at each stage of the task.** [How to perform cross-check](https://docs.app.rs.school/#/platform/cross-check-flow).
  - [Cross-check evaluation criteria. Week 1](#cross-check-evaluation-criteria-week-1).
  - [Cross-check evaluation criteria. Week 2](#cross-check-evaluation-criteria-week-2).
  - [Cross-check evaluation criteria. Week 3](#cross-check-evaluation-criteria-week-3).

## Creation of a copy of the layout

The first thing to do is create your copy of the Figma designs. To do so:

- authorize on [Figma](https://www.figma.com/);
- navigate to the [layout](https://www.figma.com/file/tKcmzkARtMUFQAR9VLdLkl/shelter-dom);
- on the top toolbar, click on the arrow next to the layout name;
- in the menu that appears, select _"Duplicate to your drafts"_;
- in the main menu (upper left button) select _"Back to files"_;
- open a copy of the layout which is marked as _"In Drafts"_;

## Technical requirements

The PerfectPixel extension for Google Chrome can be used for comparison with designs. _[PerfectPixel for Google Chrome](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)_

Compatible browsers: **Google Chrome, Mozilla Firefox**. We primarily develop for Google Chrome. Then we check to see if Mozilla Firefox is breaking our styles.

It's **prohibited** to use CSS frameworks (bootstrap, foundation, etc.).  
It's **prohibited** to use JS frameworks (Angular, React, Vue, etc.).  
It's **prohibited** to use legacy libraries (jQuery, etc.).  
It's **allowed** to use up-to-date libraries with a set of helper functions (lodash). You can use Lodash as well as utils for the creation of a slider, pagination, and popups. However, it's recommended to use pure JavaScript.
It's **allowed** to use icon fonts and CSS preprocessors (SCSS).
It's **recommended** to use [normalize.css](https://necolas.github.io/normalize.css/).

Please pay attention to the following points:

- The main blocks should be exactly located on the given screen width, as in the Figma designs.
- Images and logos (if any) should be located within a logical container with the correct centering and positioning approach. A slight deviation from the layout is allowed in favor of a grid or column structure.
- Icons and pictures should keep the ideal distance to the beginning of the corresponding text.
- Icons and pictures should keep their proportions.
- If the correct font is used, check the height of the text - it should match the source. The width may vary. But the common practice is to add the `letter-spacing` property to the text of headings, mottos, or quotes.
- If there are several objects in a row of visually the same width, then the width of the blocks containing them must be the same. The difference in image sizes does not matter, what matters is the matching of block sizes. If the width of the blocks in the layout is different, then you still need to make it the same.
- Some elements should be interactive. The layout contains separately designed blocks describing what the button or element looks like with and without the hover effect.

"Interactive" means that a button or element has a visual effect or animation (at your discretion based on the layout: cursor animation, background color change, dimming, underline, font change) during some user action, for example, on hover. It is not necessary to use JavaScript to handle custom events in this task. Usually, this effect is implemented using the `:hover` pseudo-class and the following properties:

- `cursor: pointer`,
- `background`,
- `text-decoration: underline`,
- `color`.

## Repository requirements

- Create a public repository named shelter on your GitHub account.
- You may use the example of project structure below. Since the project will contain several pages (2), at the same level as `assets` there will be the `pages` directory. Inside `pages`, in the `main` folder (same as the page name), the `.html`, `.css` and `.js` files related to this page will be stored. The `assets` directory will still contain images, icons, and font files if any. The folders inside `assets` will be named depending on the content: `images`, `icons`, `fonts`. Example below:
- ![shelter folder structure](shelter-folder-structure.jpg)
- You should deploy your task using gh-pages or by any other means.
- The commit history should reflect the development process of the application. Commit names should match the [commit requirements](https://docs.rs.school/#/git-convention)

## Useful links

Fonts can be found here:

[Arial, google fonts](https://www.fonts.com/font/monotype/arial?QueryFontType=Web&src=GoogleWebFonts)  
[Georgia, google fonts](https://www.fonts.com/font/microsoft-corporation/georgia?QueryFontType=Web&src=GoogleWebFonts)

You can connect fonts by either downloading local files or connecting fonts via URL to google fonts. If you can't find or download the font you need, just replace it with a font with the same serif type.

## Week 1

The original width of the provided layout is 1280px. The width of the wrapper or guide columns is 1200px. The sizes of internal blocks are recommended to be set in relative values (%, vw) in order not to rewrite CSS styles for fluid layout.

When the window width is above 1280px, the layout should remain centered, and not stretch to the full width of the window. To fill the free space, you can either stretch the backgrounds of the corresponding blocks to the entire width of the window, or use any of the colors present in the [designs](https://www.figma.com/file/tKcmzkARtMUFQAR9VLdLkl/shelter-dom):

![small-bg-example-1280](https://user-images.githubusercontent.com/73646765/161041203-e22754f4-7bf0-4679-982a-aa6de81783e7.jpg)

#### Desktop version of the Main page (60 points)

JPG: **[shelter. main-1280. JPG](shelter-main-1280px.jpg)**

1. **Header** (`<header>` contains only the logo and navigation bar)

- Interactive navigation bar:
  - `About the shelter` element should be highlighted by default;
  - highlighted `About the shelter` element may not have hover effects.
- Clicking on `Our pets` takes us to the _our pets_ page.
- Clicking on `Help the shelter` redirects us to the _Help_ block located on the same page (anchor link).
- Clicking on `Contacts` takes us to the _Footer_ block located on the same page (anchor link).
- The logo is located on the left. The logo consists of text elements (i.e. not a picture). Clicking on the logo leaves us on the current page.
- There must be one `<h1>` element on the page. You can make it with the text `Cozy House`.
- There is no need to make the header "sticky". It means what when scrolling, it remains in its position.

2. **Not only** block

- The `Make a Friend` button should be clickable.
- Clicking on `Make a Friend` takes us to the _Our Friends_ block located on the same page (anchor link).
- The background of the blocks can be made with a gradient.
- The image of the dog and the text are different blocks that should not overlap.

3. **About** block

- Carefully look at what kind of quotes are here.

4. **Our Friends** block

- Buttons "left" and "right" should be interactive.
- Pet cards should be interactive when hovering over any area of the card. Hovering over a card changes the cursor, highlights the `Learn more` button, and changes the background.
- `Learn more` buttons should be interactive.
- The `Get to know the rest` button should be interactive.
- Clicking on `Get to know the rest` takes us to the _our pets_ page.

5. **Help** block

- Arrangement of elements: necessarily 5 elements on top and 4 elements on the bottom.

6. **In addition** block

- Interactive block with bank account number. The number should be a link that doesn't lead anywhere.

7. **Footer** (`<footer>` contains contacts, address and image):

- Clicking on an email or its icon should open the mail service.
- Clicking on the phone or its icon should open dialing.
- Clicking on a location should open a page with google maps in a separate window with any location you choose.
- The image of the dog, address and contacts are different blocks that should not overlap.
- The background of the block can be made with a gradient.

## Cross-check evaluation criteria. Week 1

Open the application at 1280px screen width. If the screen is smaller, you can zoom in, or you can set the page width to 1280px and observe with the visible horizontal scrollbar. If the screen is wider, you can make the area narrower or narrow the window. If the vertical scroll is present, in some cases the width may not match the one that displays the value in the dev tools (the offset can be up to 17px). When checking, keep this in mind and make sure that the width is set correctly.

The task is checked exclusively according to the criteria specified below. If you see some kind of defect or mistake in the work that does not match a criterion, the score should not be decreased. But you can highlight it in the comments.

If during the check, you don't know whether to lower the score or not, then you shouldn't. For example, if wrong numbers are entered in the **You can also make a donation** block inside the button, then this will not be considered a mistake, the score shouldn't be reduced.

❗ The score cannot go below **0** per page. Unless otherwise stated in the requirements, all non-repeating blocks or elements without `hover` should meet the following criteria:

- Indents from the borders of elements (or sets of elements) to the edges of the block, horizontally or vertically, differ by more than 20px: **-1** for each block.
- Margins within a set or grid between elements, horizontally or vertically, differ by more than 10px: **-1** per block.
- The background color of the block or element differs from the design (does not apply to the position of the gradient or stretched image): **-1** for each block.
- Missing element or picture, both background and element picture: **-1** for each block.
- font-family is not included, or difference in font size is more than 4px: **-1** per block.

The _Main page_ is created **+60**.

1. The **Header** block is absent: **-10**.

- There's no logo: **-2**.
- No navbar: **-5**. The navigation bar is present, but not interactive: **-1**. It is recommended to use `<nav>`.
- The `About the shelter` element is not highlighted: **-1**.
- The `Our pets` element does not work as a link to the _our pets_: **-1** page.
- The `Help the shelter` element does not work as an anchor link to the _Help_ block: **-1**.
- The `Contacts` element does not work as an anchor link to the _Footer_ block: **-1**.
- There is no `<h1>` element on the page: **-2**. There is an `<h1>` element, but there is more than one: **-1**.
- The background significantly differs from what is on the designs (does not mean a shifted image or gradient): **-1**.

2. The **Not only** block is absent: **-5**.

- The `Make a Friend` is absent: **-2**. The button is present, but not interactive, or does not work as an anchor link to the _Our Friends_: **-1** block.
- The background significantly differs from what is on the designs (does not mean a shifted image or gradient): **-1**.
- There's no image of a dog: **-2**. There is a image of a dog, but it is significantly shifted, or overlapped on the text or other blocks: **-1**.

3. The **About** block is absent: **-5**.

- There's no image of a cat and a dog: **-2**. There is a image of a dog, but it is significantly shifted, or overlapped on the text or other blocks: **-1**.
- Header text has incorrect dimensions: **-2**.
- The quotation marks are not in the correct form: **-1**.

4. The **Our Friends** block is absent: **-20**.

- There's no "left" button: **-2**. The button is present, but it is not interactive: **-1**.
- There's no "right" button: **-2**. The button is present, but it is not interactive: **-1**.
- There're no pet cards: **-10**. The pet cards are present, but at the same time:
  - The grid structure of the elements is broken: **-2**.
  - The number of cards does not match the designs: **-2**.
  - The structure of the cards is broken (for example, text or a button is located above the image): **-2**.
  - Cards are not interactive: **-2**.
  - `Learn more` buttons don't change color when hovering over the card: **-2**.
- There's no `Get to know the rest` button: **-2**. The button is present, but not interactive, or doesn't work as a link to the _our pets_ page: **-1**.

5. The **Help** block is absent: **-5**.

- The grid structure of the elements is broken (not 5 elements from above, 4 from below): **-2**.
- Image of one or more icons missing: **-2**.
- The structure is broken (e.g. text above or icon below) in one or more elements: **-1**.

6. The **In addition** block is absent: **-5**.

- There's no bank account button: **-2**. The button is present, but not interactive, or is not a link: **-1**.
- There's no image of a dog: **-2**. There is a image of a dog, but it is significantly shifted, or overlapped on the text or other blocks: **-1**.

7. The **Footer** block is absent: **-10**.

- The grid structure of the elements is broken: **-2**.
- The `email` element does not work as a link to a mail service: **-2**.
- The `phone` element does not work as a call service link: **-2**.
- At least one `location` element does not work as a link to google maps: **-1**.
- There's no image of a dog: **-2**. There is a image of a dog, but it is significantly shifted, or overlapped on the text or other blocks: **-1**.
- The background significantly differs from what is on the designs (does not mean a shifted image or gradient): **-1**.

## Week 2

#### Desktop version of the Our Pets (40 points)

JPG: **[shelter. Pets page. JPG](shelter-pets-1280px.jpg)**

1. **Header** (`<header>` contains only the logo and navigation bar)

- Interactive navigation bar:
  - `Our pets` element should be highlighted by default;
  - highlighted `Our pets` element may not have hover effects.
- Clicking on `About the shelter` takes us to the the _main page_
- Clicking on `Help the shelter` redirects us to the _Help_ block located on the _main page_ (anchor link).
- Clicking on `Contacts` takes us to the _Footer_ block located on the same page (anchor link).
- The logo is located on the left. The logo consists of text elements (i.e. not a picture). Clicking on the logo takes us to the _main page_.
- There must be one `<h1>` element on the page. You can make it with the text `Cozy House`.
- There is no need to make the header "sticky". It means what when scrolling, it remains in its position.

2. **Our Friends** block

- Four-column layout.
- Pet cards should be interactive when hovering over any area of the card. Hovering over a card changes the cursor, highlights the `Learn more` button, and changes the background.
- It is not necessary to open a modal window when clicking at this stage.
- Pagination should be clickable on available buttons. This means that from position (1) we cannot go further to the left, i.e. to the smaller side. Gray buttons must have the attribute `disabled`, `data-disabled` or a modifier class.

3. **Footer** (`<footer>` contains contacts, address and image):

- Clicking on an email or its icon should open the mail service.
- Clicking on the phone or its icon should open dialing.
- Clicking on a location should open a page with google maps in a separate window with any location you choose.
- The image of the dog, address and contacts are different blocks that should not overlap.
- The background of the block can be made with a gradient.

## Cross-check evaluation criteria. Week 2

The _Our pets_ page is created **+40**.

1. The **Header** block is absent: **-10**.

- There's no logo: **-2** The logo is present, but does not work as a link to the _Main page_: **-1**.
- No navbar: **-5**. The navigation bar is present, but not interactive: **-1**. It is recommended to use `<nav>`.
- The `About the shelter` element does not work as a link to the _Main page_: **-1**.
- The `Our pets` element is not highlighted: **-1**.
- The `Help the shelter` element does not work as an anchor link to the _Help_ block of the _Main page_: **-1**.
- The `Contacts` element does not work as an anchor link to the _Footer_ block of the same page: **-1**.
- There is no `<h1>` element on the page: **-2**. There is an `<h1>` element, but there is more than one: **-1**.
- The background significantly differs from what is on the designs (does not mean a shifted image or gradient): **-1**.

2. The **Our Friends** block is absent: **-20**.

- There're no pagination buttons: **-10**. There is a button, but:
  - Buttons are of the same color or background: **-2**.
  - The buttons are in the wrong order: **-2**.
  - Buttons "left" interactive: **-1**.
  - Buttons "right" are not interactive: **-1**.
  - There is no number on the page circle, or the number is different from one: **-1**.
  - The page circle is interactive: **-1**.
- There're no pet cards: **-10**. The pet cards are present, but at the same time:
  - The grid structure of the elements is broken: **-2**.
  - The number of cards does not match the designs: **-2**.
  - The structure of the cards is broken (for example, text or a button is located above the image): **-2**.
  - Cards are not interactive: **-2**.
  - `Learn more` buttons don't change color when hovering over the card: **-2**.

3. The **Footer** block is absent: **-10**.

- The grid structure of the elements is broken: **-2**.
- The `email` element does not work as a link to a mail service: **-2**.
- The `phone` element does not work as a call service link: **-2**.
- At least one `location` element does not work as a link to google maps: **-1**.
- There's no image of a dog: **-2**. There is a image of a dog, but it is significantly shifted, or overlapped on the text or other blocks: **-1**.
- The background significantly differs from what is on the designs (does not mean a shifted image or gradient): **-1**.

## Week 3

Pay attention to additions:

- **[Repository requirements](#repository-requirements)**
- **[First paragraph in a section: Cross-check evaluation criteria. Week 1](#cross-check-evaluation-criteria-week-1)**

### Task verification features

The task will be evaluated by resizing the Google Chrome browser window, or by connecting device emulation through the developer panel (DevTools -> Toggle Device Toolbar). Evaluation the project on real mobile devices or tablets is **not required**.

❗ Убедитесь, что при проверке у вас отсутствует вертикальная полоса прокрутки, т.к. она "съедает" часть пространства отзывчивой верстки своей шириной. Чтобы ее отключить, необходимо выбрать режим эмуляции `Responsive`, а так же установить тип устройства `Mobile`. Если тип устройства не отображается, в верхней панели `device toolbar` нажмите на три точки справа и выберите `Add device type`.

![responsive](shelter-responsive.png)

**«responsive»** - это размеры, заданные в относительных величинах от ширины окна или родительского блока, которые плавно меняют свои значения при уменьшении или увеличении окна браузера. Главное, чтобы при наложении картинки, например, в 768px на макет шириной 768px, размеры или отступы совпадали.

❗ Страница не должна разваливаться, что значит, что отступы, размеры блоков, и прочее, не должны уходить за правый край экрана и не должен появляться горизонтальный скролл, до порогового значения (меньше 320px).

## 1280px <= width

Выполняются требования верстки [week 1](#week-1) проекта: либо блоки продолжают свой цвет на всю доступную область окна, а сама обертка (1200px) центрируется (при этом градиент также может менять ширину), либо макет занимает максимальную ширину в 1280px и центрируется с равными отступами справа и слева, белого или любого другого цвета из макета (при проверке, если трудно будет смотреть целостность на большом экране, в панели разработчика можно задать элементу body свойство background-color любого контрастного цвета).

## 768px <= width < 1280px

### Main Page

1. **Header** (`<header>` содержит только логотип и панель навигации)

- Логотип прибивается ближе к верху страницы.
- Отступы слева от логотипа и справа от меню навигации должны быть заданы жестко, как на макете `768px`.
- Хедер "липким" делать не нужно. Т.е. при скролле он остается на своей позиции.

2. Блок **Not only**

- Заголовок с текстом "Not only people need a house" должен быть расположен как указано на макете. Т.е. перенос строк должен быть соответствующим макету. Для этого можно сделать дополнительную обертку, которую и центрировать относительно основных блоков. Только отступы могут быть `responsive`, но отступ слева должен совпадать с отступом последующего блока текста.
- Блок с текстом "We offer to give..." должен быть центрирован с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Кнопка "Make a Friend" должна быть центрирована и иметь жесткие размеры, как на макете `768px`.
- Картинка собаки может быть `responsive`, но смещение должно оставаться в правую сторону пропорциональным, т.е. отступы до правого края могут быть так же `responsive`.

3. Блок **About**

- Заголовок с текстом "About the shelter..." должен быть расположен как указано на макете. Т.е. перенос строк должен быть соответствующим макету. Для этого можно сделать дополнительную обертку, которую и центрировать относительно основных блоков. Только отступы могут быть `responsive`, но отступ слева должен совпадать с отступом последующего блока текста.
- Блоки с текстом "Currently..." и "We feed our..." должны быть центрированы с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Картинка кошки и собаки ее отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

4. Блок **Our Friends**

- Заголовок блока должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Вместо трех блоков с питомцами, теперь должно быть два. Блоки с питомцами имеют жесткие размеры, как на макете `assets`. При этом отступы между блоками, стрелками слайдера или краями экрана могут быть `responsive`.
- Кнопка "Get to know the rest" должна быть центрирована и иметь жесткие размеры, как на макете `768px`.

5. Блок **Help**

- Заголовок блока должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Элементы расположены сеткой, 3 х 3. Либо сетка увеличивается пропорционально размерам экрана, либо отступы между элементами и краями экрана можно сделать `responsive`. Структура сетки меняться не должна.

6. Блок **In addition**

- Блок с текстом "You can..." должен быть расположен как указано на макете. Т.е. перенос строк должен быть соответствующим макету. Для этого можно сделать дополнительную обертку, которую и центрировать относительно основных блоков. Только отступы могут быть `responsive`, но отступ слева должен совпадать с отступом последующего блока текста.
- Блок с текстом "Name of the bank..." должен быть расположен как указано на макете. Для этого можно сделать дополнительную обертку, которую и центрировать относительно основных блоков. Только отступы могут быть `responsive`, но отступ слева должен совпадать с отступом последующей кнопки.
- Кнопка с номером счета в банке должна быть расположена, как указано на макете, и иметь жесткие размеры, как на макете `768px`. Для этого можно сделать дополнительную обертку, которую и центрировать относительно основных блоков. Только отступы могут быть `responsive`, но отступ слева должен совпадать с отступом последующего блока текста.
- Блок с текстом "Legal information..." должен быть центрирован с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Картинка собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

7. **Footer** (`<footer>` содержит контакты, адрес и изображение):

- Тут идет сетка из двух колонок. Обратите внимание, что сам блок с сеткой должен быть центрирован. Т.е. расстояние слева до первой колонки совпадает с расстоянием справа до второй колонки. При этом сами колонки и отступы могут быть `responsive`.
- Картинка собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

### Pets Page

1. **Header** (`<header>` содержит только логотип и панель навигации)

- Логотип прибивается ближе к верху страницы.
- Отступы слева от логотипа и справа от меню навигации должны быть заданы жестко, как на макете `768px`.
- Хедер должен быть "липким". Т.е. при скролле он всегда показан на странице сверху, сохраняя свою позицию.

2. Блок **Our Friends**

- Заглавный текст должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Сетка становится 2 х 3. Блоки с питомцами имеют жесткие размеры, как на макете `assets`. При этом отступы между блоками или краями экрана могут быть `responsive`.
- Блок с кнопками должен быть центрирован. Размеры кнопок и расстояния между ними заданы жестко, как на `assets`, или как на макете `768px`. Отступы до краев экрана могут быть `responsive`.

3. **Footer** (`<footer>` содержит контакты, адрес и изображение):

- Тут идет сетка из двух колонок. Обратите внимание, что сам блок с сеткой, должен быть центрирован. Т.е. расстояние слева до первой колонки совпадает с расстоянием справа до второй колонки. При этом сами колонки и отступы могут быть `responsive`.
- Картинка собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

## 320px <= width < 768px

### Main Page

1. **Header** (`<header>` содержит только логотип и бургер меню)

- Меню навигации преобразовывается в так называемое бургер меню, которое будет открываться по нажатию и предлагать привычную нам панель навигации. Логотип дублируется в открытом меню, хотя на макете этого не видно. Однако, если вы сделали так, что меню открывается, а логотип с основной страницы пропадает - это не ошибка, баллы сниматься не будут.
- Отступ слева от логотипа может быть `responsive`. Отступ справа от меню навигации должен быть задан жестко, как на макете `320px`.
- Хедер "липким" делать не нужно. Т.е. при скролле он остается на своей позиции.

2. Блок **Not only**

- Заголовок с текстом "Not only people need a house" должен быть центрирован с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Блок с текстом "We offer to give..." должен быть центрирован с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Кнопка "Make a Friend" должна быть центрирована и иметь жесткие размеры, как на макете `320px`.
- Картинка собаки может быть `responsive`, но смещение должно оставаться в правую сторону пропорциональным, т.е. отступы до правого края могут быть так же `responsive`.

3. Блок **About**

- Заголовок с текстом "About the shelter..." должен быть центрирован с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Блоки с текстом "Currently..." и "We feed our..." должны быть центрированы с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Картинка кошки и собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

4. Блок **Our Friends**

- Заголовок блока должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Вместо двух блоков с питомцами, теперь должен быть один. Блок с питомцами имеет жесткие размеры, как на макете `assets`. При этом отступы между стрелками слайдера или краями экрана могут быть `responsive`.
- Кнопка "Get to know the rest" должна быть центрирована и иметь жесткие размеры, как на макете `320px`.

5. Блок **Help**

- Заголовок блока должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Элементы расположены сеткой, 2 х 5. Либо сетка увеличивается пропорционально размерам экрана, либо отступы между элементами и краями экрана можно сделать `responsive`. Структура сетки меняться не должна. Последний, девятый элемент сетки должен находиться в сетке слева.

6. Блок **In addition**

- Блок с текстом "You can..." должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Блок с текстом "Name of the bank..." должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Кнопка с номером счета в банке должна быть центрирована. Сама кнопка, как и отступы до краев экрана, могут быть `responsive`.
- Блок с текстом "Legal information..." должен быть центрирован с равными отступами по краям. Блок с текстом и отступы могут быть `responsive`.
- Картинка собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

7. **Footer** (`<footer>` содержит текст, логотип и панель навигации):

- Одна единственная колонка. Отступы всех элементов до краев экрана должны совпадать. Сама колонка должна быть центрирована. При этом, как сама колонка, так и отступы до краев экрана, могут быть `responsive`.
- Картинка собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

### Pets Page

1. **Header** (`<header>` содержит только логотип и бургер меню)

- Меню навигации преобразовывается в так называемое бургер меню, которое будет открываться по нажатию и предлагать привычную нам панель навигации. Логотип дублируется в открытом меню, хотя на макете этого не видно. Однако, если вы сделали так, что меню открывается, а логотип с основной страницы пропадает - это не ошибка, баллы сниматься не будут.
- Отступ слева от логотипа может быть `responsive`. Отступ справа от меню навигации должны быть задан жестко, как на макете `320px`.
- Хедер должен быть "липким". Т.е. при скролле он всегда показан на странице сверху, сохраняя свою позицию.

2. Блок **Our Friends**

- Заголовок блока должен быть центрирован. Блок с текстом и отступы могут быть `responsive`.
- Сетка становится 1 х 3. Блоки с питомцами имеют жесткие размеры, как на макете `assets`. При этом отступы между блоками или краями экрана могут быть `responsive`.
- Блок с кнопками должен быть центрирован. Размеры кнопок и расстояния между ними заданы жестко, как на `assets`, или как на макете `320px`. Отступы до краев экрана могут быть `responsive`.

3. **Footer** (`<footer>` содержит контакты, адрес и изображение):

- Одна единственная колонка. Отступы всех элементов до краев экрана должны совпадать. Сама колонка должна быть центрирована. При этом, как сама колонка, так и отступы до краев экрана, могут быть `responsive`.
- Картинка собаки и отступы могут быть `responsive`. Главное, чтобы картинка была центрирована.

## width < 320px

Минимальная ширина макета = 320px. После порогового значения расположение верстки значения не имеет. Структура верстки остается такой же, как при ширине 320px. Если в какой-то момент при уменьшении ширины экрана верстка "ломается", это не ошибка.

## Cross-check evaluation criteria. Week 3

❗ **Важное замечание #1**: При изменении ширины с использованием инструментов разработчика (dev tools) и наличии вертикальной полосы прокрутки, расхождение может составлять до 17px (стандартная ширина вертикальной полосы прокрутки). В таком случае надо либо изменить ширину на величину этого расхождения, либо перейти в [task verification features](#task-verification-features), чтобы вертикальной полосы прокрутки не было.  
❗ **Важное замечание #2**: При масштабировании экрана (например, zoom+ 125%) реальная ширина может отличаться на 1-2 пикселя. Например, реальное значение может быть 767 или 769, хотя инструменты разработчика будут показывать 768. Поэтому надо сдвинуть до точки перехода, несмотря на отличие.  
❗ **Важное замечание #3**: Единственненный блок, в котором элементы не обязательно должны соблюдать структуру - это блок `Help`. Если элементы идут как перечисляемые элементы, то при проверке на резиновую верстку, отступы от края блока до элементов, а также количество в ряду не учитываются и баллы не снижаются. Также не оценивается, центрируются ли элементы или прибиты к левому краю. Однако нарушение размеров учитывается, будьте внимательны!  
❗ **Важное замечание #4**: Проверка полного соответствия макетам по Perfect Pixel происходит только на соответствующих контрольных точках - 1280px, 768px, 320px. На всех промежуточных величинах допускается отсутствие точного следования отступам и размерам, но рекомендуется следовать принципам расположения тех или иных элементов, не отмеченных в конкретных требованиях.

---

❗ **Ознакомьтесь с некоторыми определениями**:

- **Нарушение отступов** - это ситуация, когда расстояние между элементами, или расстояние от элемента до края контейнера, в котором он содержится, отличается от заданного на макете более чем на 10 пикселей по высоте или ширине.
  Рассмотрим ситуацию на примере блока `our friends`. Вы, скорее всего, будете знать примерное расстояние между элементами на глаз. Однако, вас смущает отступ кнопки "влево" от края экрана слева. Расстояние от кнопки "влево" до левой границы блока 40px на ширине экрана 1280px. Значит, выставив ширину 1280px, смотрим расстояние. Если оно отличается на величину до 10px включительно (например 50px или 30px) - баллы не снимаем. Однако, если отступы больше этих значений (например 51px или 29px) - снимаем указанное количество баллов.
- **Нарушение размеров** - это ситуация, когда размеры элементов (кнопок, картинок, карточек животных, иконок) отличаются от заданного на макете более чем на 10 пикселей по высоте или ширине. Проверку проводим таким же образом, как и при нарушении отступов, и если отличия большие, снимаем указанное количество баллов.
- Длину текста и слов по ширине, а также порядок переноса слов по строкам, мы **не учитываем при проверке**.
- **Уникальная ошибка** - это новая найденная ошибка в проверяемом блоке. Независимо от того, сколько раз эта ошибка повторяется в проверяемом блоке, указанное количество баллов снимается только 1 раз.  
  Например, съехала кнопка во всех карточках животных. Снимать баллы будем лишь один раз, т.к. скорее всего сломан общий стиль. Если карточка со съехавшей кнопкой одна (а в остальных кнопка находится на своем месте) - все равно снимаем указанное количество баллов. Т.е. нет разницы, ошибка в одном повторяющемся элементе, или в нескольких.

### Общая проверка поведения приложения при изменении ширины окна

Хоть при растягивании экрана на 4k, хоть при уменьшении до 320px не должна теряться целостность приложения. При плавном изменении размера мы не учитываем точных подсчетов расположения элементов. На данном этапе в браузере **Google Chrome** проверяется:

- отсутствие горизонтальной полосы прокрутки на любой ширине экрана до 320px включительно;
- элементы не должны выходить за боковые границы экрана\* при любой ширине экрана до 320px включительно.

  Если, оба условия в браузере **Google Chrome** выполняются (сайт ведет себя отзывчиво, элементы и общая структура меняет размеры вместе с изменением ширины, не появляется горизонтальная полоса прокрутки и элементы не выходят за боковые стороны окна), то ставим **+50** за каждую страницу. В сумме за 2 страницы ставим **+100**.
  Если на странице появляется горизонтальная полоса прокрутки или происходит заход контента за боковую границу экрана, ставим **0** за страницу.\*\*

  После проверки отзывчивости верстки в браузере Google Chrome выполняется аналогичная проверка в браузере **Mozilla Firefox**, при которой:

- если при изменении размера окна браузера от максимума до 320px появляется горизонтальная полоса прокрутки, или контент выходит за пределы экрана, **снимается -20**.
- если при изменении размера окна браузера от максимума до 320px горизонтальная полоса прокрутки не появляется, контент не выходит за пределы экрана, но появляются какие-то другие проблемы в верстке (отличные от тех, что были в Google Chrome) - **снимается -5 за каждую** с описанием проблемы, но **не более -20**.

  Максимальное количество баллов, которое можно вычесть при наличии ошибок во время проверки в браузере **Mozilla Firefox** - **-20**.\*\*\*

  \* _на ширине экрана <768px за боковую границу экрана может заходить бургер-меню. Т.к. это нормальная практика, ошибкой это не считается, если при этом на странице не появляется горизонтальная прокрутка._  
  \*\* _если во время общей проверки за страницу выставляется 0, дальнейшие критерии, относящиеся к этой странице, не проверяются._  
  \*\*\* _дальнейшая проверка происходит только в браузере Google Chrome_

### 1280px <= width (максимально -10 баллов за страницу)

При проверке на больших экранах допустимо:
**1) фоны блоков растягиваются на всю ширину окна**, при этом сам контент находится в центре экрана и соответствует макету;
**2) верстка занимает максимальную ширину 1280px** и соответствует макету, центрируется с равными отступами слева и справа, свободное пространство заполнено любым цветом;

Для любого из случаев выше **считается ошибкой**, если контент не центрируется, т.е. прижат к правой или левой стороне. В случае такой ошибки **снимается -10** баллов за страницу.
Если контент центрирован, проверяется соответствие макету 1280px, для этого:

- выставляем ширину окна в 1280px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -10 суммарно**.

**3) контент растягивается по всей ширине окна**:

В этом случае производится дополнительная проверка следующих условий:

#### Main Page

Смотрим, выполняются ли следующие условия резиновой верстки:

- Фон растянут на `Header` и блок `Not only`.
- Картинка собаки в блоке `Not only` не пересекается с текстом.
- Все параграфы с текстом справа от картинки кошки и собаки выравнены по левому краю в блоке `About the shelter`.
- В блоке `Our friends` текст, слайдер и кнопка снизу центрированы.
- Все параграфы с текстом и ссылка с номером карты справа от картинки собаки выравнены по левому краю в блоке `In addition`.
- Иконки и текст в обоих колонках выравнены по левому краю своих колонок в блоке `Footer`.

Если условия нарушены, снимается **-5** за каждый пункт.  
Если блоки или элементы выходят за рамки экрана, или накладываются друг на друга, снимается **-5** за каждую уникальную ошибку.

Выполняется проверка соответствия макету main-1280, для чего:

- выставляем ширину окна в 1280px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -10 суммарно, включая снижение баллов за нарушение условий резиновой верстки**.

#### Pets Page

Смотрим, выполняются ли следующие условия резиновой верстки:

- `Header` всегда видимый, и находится сверху страницы, в том числе при скролле.
- В блоке `Our friends` находится 8 карточек питомцев, 2 ряда по 4 элемента.
- В блоке `Our friends` все элементы и блоки с элементами центрированы. Если в пагинации найден недочет или неточность верстки, прежде чем снижать балл, убедитесь, что после того, как вы выставили ширину и сделали **перезагрузку страницы**, проблема все еще существует.
- При открытии страницы, в пагинации должно быть число "1", а кнопки слева неактивны.
- Иконки и текст в обеих колонках выравнены по левому краю своих колонок в блоке `Footer`.

Если условия нарушены, снимается **-5** за каждый пункт.  
Если блоки или элементы выходят за рамки экрана, или накладываются друг на друга, снимается **-5** за каждую уникальную ошибку.

Выполняется проверка соответствия макету our-pets-1280, для чего:

- выставляем ширину окна в 1280px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -10 суммарно, включая снижение баллов за нарушение условий резиновой верстки**.

### 768px <= width < 1280px (максимально -15 баллов за страницу)

#### Main Page

Смотрим, выполняются ли следующие условия резиновой верстки:

- Фон растянут на `Header` и блок `Not only`.
- Картинка собаки снизу в блоке `Not only` не пересекается с текстом.
- Все параграфы с текстом выравнены по левому краю в блоке `Not only`. Сами блоки центрированы.
- Кнопка "Make a friend" центрирована.
- Все параграфы с текстом выравнены по левому краю в блоке `About the shelter`. Сами блоки центрированы.
- В блоке `Our friends` текст, слайдер и кнопка снизу центрированы.
- В блоке `Our friends` в слайдере 2 карточки питомцев.
- Все параграфы с текстом, а также ссылка с номером карты, выравнены по левому краю в блоке `In addition`. Сами блоки центрированы.
- Иконки и текст в обеих колонках выравнены по левому краю своих колонок в блоке `Footer`.
- Картинка собаки снизу в блоке `Footer` не пересекается с текстом.

Если условия нарушены, снимается **-5** за каждый пункт.  
Если блоки или элементы выходят за рамки экрана, или накладываются друг на друга, снимается **-5** за каждую уникальную ошибку.

Выполняется проверка соответствия макету main-768, для чего:

- выставляем ширину окна в 768px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -15 суммарно, включая снижение баллов за нарушение условий резиновой верстки**.

#### Pets Page

Смотрим, выполняются ли условия резиновой верстки:

- `Header` всегда видимый, находится сверху страницы, в том числе при скролле.
- В блоке `Our friends` находится 6 карточек питомцев, 3 ряда по 2 элемента.
- В блоке `Our friends` все элементы и блоки с элементами центрированы. Если в пагинации найден недочет или неточность верстки, прежде чем снижать балл, убедитесь, что после того, как вы выставили ширину и сделали **перезагрузку страницы**, проблема все еще существует.
- При открытии страницы в пагинации должно быть число "1", а кнопки слева неактивны.
- Картинка собаки снизу в блоке `Footer` не пересекается с текстом.

Если условия нарушены, снимается **-5** за каждый пункт.  
Если блоки или элементы выходят за рамки экрана, или накладываются друг на друга, снимается **-5** за каждую уникальную ошибку.

Выполняется проверка соответствия макету our-pets-768, для чего:

- выставляем ширину окна в 768px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -15 суммарно, включая снижение баллов за нарушение условий резиновой верстки**.

### 320px <= width < 768px (максимально -15 баллов за страницу)

#### Main Page

Смотрим, выполняются ли следующие условия резиновой верстки:

- Фон растянут на `Header` и блок `Not only`.
- Меню в `Header` скрывается (становится бургер меню), в `Header` появляется бургер-иконка.
- Все параграфы с текстом и кнопка центрированы в блоке `Not only`.
- Картинка собаки снизу в блоке `Not only` не пересекается с текстом.
- Все параграфы с текстом центрированы в блоке `About the shelter`. При этом текст в параграфах, но не заголовке, выравнен по ширине параграфа.
- В блоке `Our friends` текст, карточка в слайдере, блок с кнопками слайдера и кнопка снизу центрированы.
- В блоке `Our friends` в слайдере 1 карточка питомца.
- Все параграфы с текстом, а также ссылка с номером карты, центрированы в блоке `In addition`. При этом текст в параграфах, но не заголовках и ссылке с номером карты, выравнен по ширине параграфа.
- Заголовки с текстом, иконка и адрес email, иконка и номер телефона и картинка собаки в самом низу центрированы в блоке `Footer`.
- Иконки локации и адреса выравнены по левому краю, а сам блок центрирован. Если локации и иконки целиком центрированы - это не ошибка, баллы не снимаем!

Если условия нарушены, снимается **-5** за каждый пункт.  
Если блоки или элементы выходят за рамки экрана, или накладываются друг на друга, снимается **-5** за каждую уникальную ошибку.

Выполняется проверка соответствия макету main-320, для чего:

- выставляем ширину окна в 320px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -15 суммарно, включая снижение баллов за нарушение условий резиновой верстки**.

#### Pets Page

Смотрим, выполняются ли условия резиновой верстки:

- `Header` всегда видимый, и находится сверху страницы, в том числе при скролле.
- Меню в `Header` скрывается (становится бургер меню), в `Header` появляется бургер-иконка.
- В блоке `Our friends` находится 3 карточки питомцев, 1 колонка с 3 элементами.
- В блоке `Our friends` все элементы и блоки с элементами центрированы. Если в пагинации найден недочет или неточность верстки, прежде чем снижать балл, убедитесь, что после того, как вы выставили ширину и сделали **перезагрузку страницы**, проблема все еще существует.
- При открытии страницы, в пагинации должно быть число "1", а кнопки слева неактивны.
- Заголовки с текстом, иконка и адрес email, иконка и номер телефона и картинка собаки в самом низу центрированы в блоке `Footer`.
- Иконки локации и адреса выравнены по левому краю, а сам блок центрирован. Если локации и иконки целиком центрированы - это не ошибка, баллы не снимаем!

Выполняется проверка соответствия макету our-pets-320, для чего:

- выставляем ширину окна в 320px
- проверяем отсутствие нарушений отступов или нарушений размеров.
  За каждую уникальную ошибку в нарушении отступов или нарушении размеров снимается **-3**, **но не более -15 суммарно, включая снижение баллов за нарушение условий резиновой верстки**.
