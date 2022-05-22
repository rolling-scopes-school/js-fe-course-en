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

The original width of the provided layout is 1280px. The width of the wrapper or guide columns is 1200px. The sizes of internal blocks are recommended to be set in relative values (%, vw) in order not to rewrite CSS styles for responsive layout.

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

❗ Make sure you don't have a vertical scroll bar when you check, because it "eats" part of the responsive layout space with its width. To disable it, you must select the `Responsive` emulation mode, as well as set the device type to `Mobile`. If the device type is not displayed, in the top bar of the `device toolbar`, click on the three dots on the right and select `Add device type`.

![responsive](shelter-responsive.png)

**"responsive"** are sizes given in relative values from the width of the window or parent block, which smoothly change their values when the browser window is reduced or enlarged. The main thing is that when imposing a picture, for example, at 768px on a layout with a width of 768px, the sizes or indents match.

❗ The page should not fall apart, which means that padding, block sizes, and so on, should not go beyond the right edge of the screen and there should not be a horizontal scroll, up to a threshold value (less than 320px).

## 1280px <= width

The layout requirements of [week 1](#week-1) of the project are met: either the blocks continue their color to the entire available area of the window, and the wrapper itself (1200px) is centered (the gradient can also change the width), or the layout takes a maximum width of 1280px and centered with equal indents on the right and left, white or any other color from the layout (when checking, if it will be difficult to see the integrity on a large screen, you can set the body element's background-color property of any contrasting color in the developer panel).

## 768px <= width < 1280px

### Main Page

1. **Header** (`<header>` only contains logo and navigation bar)

- The logo is nailed closer to the top of the page.
- Padding to the left of the logo and to the right of the navigation menu must be hardcoded, as in the `768px` layout.
- You don't need to make the header sticky. Those, when scrolling, it remains in its position.

2. **Not only** section

- The title with the text "Not only people need a house" should be positioned as indicated on the layout. Those, line wrapping must match the layout. To do this, you can make an additional wrapper, which is centered relative to the main blocks. Only indentation can be `responsive`, but the indentation on the left must match the indentation of the next block of text.
- The block with the text "We offer to give..." should be centered with equal margins on the edges. Block with text and padding can be `responsive`.
- The "Make a Friend" button should be centered and rigidly sized like the `768px` layout.
- The dog picture can be `responsive`, but the offset to the right must remain proportional, i.e. padding to the right margin can also be `responsive`.

3. **About** section

- The title with the text "About the shelter..." should be positioned as indicated on the layout. Those, line wrapping must match the layout. To do this, you can make an additional wrapper, which is centered relative to the main blocks. Only indentation can be `responsive`, but the indentation on the left must match the indentation of the next block of text.
- Blocks with the text "Currently..." and "We feed our..." should be centered with equal margins on the edges. Block with text and padding can be `responsive`.
- A picture of a cat and a dog, its indents can be `responsive`. The main thing is that the picture is centered.

4. **Our Friends** section

- The block header must be centered. Block with text and padding can be `responsive`.
- Instead of three blocks with pets, there should now be two. Pet blocks are rigidly sized, as in the `assets` layout. In this case, the indents between blocks, slider arrows or screen edges can be `responsive`.
- The "Get to know the rest" button should be centered and rigidly sized like the `768px` layout.

5. **Help** section

- The block header must be centered. Block with text and padding can be `responsive`.
- Elements are arranged in a grid, 3 x 3. Either the grid increases in proportion to the size of the screen, or the indents between the elements and the edges of the screen can be made `responsive`. The grid structure should not change.

6. **In addition** section

- The block with the text "You can..." must be positioned as indicated on the layout. Those, line wrapping must match the layout. To do this, you can make an additional wrapper, which is centered relative to the main blocks. Only indentation can be `responsive`, but the indentation on the left must match the indentation of the next block of text.
- The block with the text "Name of the bank..." should be located as indicated on the layout. To do this, you can make an additional wrapper, which is centered relative to the main blocks. Only padding can be `responsive`, but the left padding must match the next button padding.
- The button with the bank account number must be located as indicated on the layout and have a fixed size, as on the `768px` layout. To do this, you can make an additional wrapper, which is centered relative to the main blocks. Only indentation can be `responsive`, but the indentation on the left must match the indentation of the next block of text.
- The block with the text "Legal information..." should be centered with equal margins on the edges. Block with text and padding can be `responsive`.
- Dog picture and padding can be `responsive`. The main thing is that the picture is centered.

7. **Footer** (`<footer>` contains contacts, address and image):

- There is a grid of two columns. Please note that the grid box itself must be centered. Those, the distance to the left of the first column is the same as the distance to the right of the second column. In this case, the columns themselves and indents can be `responsive`.
- Dog picture and padding can be `responsive`. The main thing is that the picture is centered.

### Pets Page

1. **Header** (`<header>` содержит только логотип и панель навигации)

- The logo is nailed closer to the top of the page.
- Padding to the left of the logo and to the right of the navigation menu must be hardcoded, as in the `768px` layout.
- You don't need to make the header sticky. Those, when scrolling, it remains in its position.

2. **Our Friends** section

- Heading text should be centered. Block with text and padding can be `responsive`.
- Grid becomes 2 x 3. Pet blocks are rigidly sized like in the `assets` layout. In this case, the indents between blocks or screen edges can be `responsive`.
- Block with buttons should be centered. Button sizes and spacings are hardcoded, like on `assets`, or like on the `768px` layout. Padding to the edges of the screen can be `responsive`.

3. **Footer** (`<footer>` contains contacts, address and image):

- There is a grid of two columns. Please note that the grid box itself must be centered. Those, the distance to the left of the first column is the same as the distance to the right of the second column. In this case, the columns themselves and indents can be `responsive`.
- Dog picture and padding can be `responsive`. The main thing is that the picture is centered.

## 320px <= width < 768px

### Main Page

1. **Header** (`<header>` only contains logo and burger menu)

- The navigation menu is transformed into the burger menu, which will open on click and offer the familiar navigation bar. The logo is duplicated in the open menu, although this is not visible on the layout. However, if you made the menu open and the logo disappears from the main page - this is not a mistake, points will not be deducted.
- The indent to the left of the logo can be `responsive`. The padding to the right of the navigation menu must be hardcoded, as in the `320px` layout.
- You don't need to make the header sticky. Those, when scrolling, it remains in its position.

2. **Not only** section

- The title with the text "Not only people need a house" should be centered with equal margins around the edges. Block with text and padding can be `responsive`.
- The block with the text "We offer to give..." should be centered with equal margins on the edges. Block with text and padding can be `responsive`.
- The "Make a Friend" button should be centered and rigidly sized like the `320px` layout.
- The dog picture can be `responsive`, but the offset to the right must remain proportional, i.e. padding to the right margin can also be `responsive`.

3. **About** section

- The title with the text "About the shelter..." should be centered with equal margins around the edges. Block with text and padding can be `responsive`.
- Blocks with the text "Currently..." and "We feed our..." should be centered with equal margins on the edges. Block with text and padding can be `responsive`.
- Cat and dog picture and padding can be `responsive`. The main thing is that the picture is centered.

4. **Our Friends** section

- The block header must be centered. Block with text and padding can be `responsive`.
- Instead of two blocks with pets, there should be one for now. The pet block has rigid dimensions, as in the `assets` layout. In this case, the padding between slider arrows or screen edges can be `responsive`.
- The "Get to know the rest" button should be centered and rigidly sized like the `320px` layout.

5. **Help** section

- The block header must be centered. Block with text and padding can be `responsive`.
- Elements are arranged in a grid, 2 x 5. Either the grid increases in proportion to the size of the screen, or the indents between the elements and the edges of the screen can be made `responsive`. The grid structure should not change. The last ninth element of the grid should be in the grid on the left.

6. **In addition** section

- Block with text "You can..." should be centered. Block with text and padding can be `responsive`.
- The block with the text "Name of the bank..." should be centered. Block with text and padding can be `responsive`.
- The button with the bank account number must be centered. The button itself, as well as padding to the edges of the screen, can be `responsive`.
- The block with the text "Legal information..." should be centered with equal margins on the edges. Block with text and padding can be `responsive`.
- Dog picture and padding can be `responsive`. The main thing is that the picture is centered.

7. **Footer** (`<footer>` contains text, logo and navigation bar):

- One single column. The indents of all elements to the edges of the screen must match. The column itself must be centered. At the same time, both the column itself and the indents to the edges of the screen can be `responsive`.
- Dog picture and padding can be `responsive`. The main thing is that the picture is centered.

### Pets Page

1. **Header** (`<header>` only contains logo and burger menu)

- The navigation menu is transformed into the burger menu, which will open on click and offer the familiar navigation bar. The logo is duplicated in the open menu, although this is not visible on the layout. However, if you made the menu open and the logo disappears from the main page - this is not a mistake, the points will not be reduced.
- The indent to the left of the logo can be `responsive`. The padding to the right of the navigation menu must be hardcoded, as in the `320px` layout.
- You don't need to make the header sticky. Those, when scrolling, it remains in its position.

2. **Our Friends** section

- The block header must be centered. Block with text and padding can be `responsive`.
- Grid becomes 1 x 3. Pet blocks are rigidly sized like in the `assets` layout. In this case, the indents between blocks or screen edges can be `responsive`.
- Block with buttons should be centered. Button sizes and spacings are hardcoded, like on `assets`, or like on the `320px` layout. Padding to the edges of the screen can be `responsive`.

3. **Footer** (`<footer>` contains contacts, address and image):

- One single column. The indents of all elements to the edges of the screen must match. The column itself must be centered. At the same time, both the column itself and the indents to the edges of the screen can be `responsive`.
- Dog picture and padding can be `responsive`. The main thing is that the picture is centered.

## width < 320px

Minimum layout width = 320px. After the threshold value, the location of the layout does not matter. The layout structure remains the same as with a width of 320px. If at some point when the screen width is reduced, the layout "breaks", this is not a mistake.

## Cross-check evaluation criteria. Week 3

❗ **Important note #1**: When changing the width using the dev tools and having a vertical scrollbar, the discrepancy can be up to 17px (standard vertical scrollbar width). In this case, you must either change the width by the amount of this discrepancy, or go to [task verification features](#task-verification-features) so that there is no vertical scrollbar.
❗ **Important note #2**: When scaling the screen (for example, zoom+ 125%), the actual width may differ by 1-2 pixels. For example, the real value could be 767 or 769, although the developer tools will show 768. Therefore, you need to shift to the transition point, despite the difference.
❗ **Important note #3**: The only block in which elements do not have to follow a structure is the `Help` block. If the elements are listed as enumerated elements, then when checking for responsive layout, the indents from the edge of the block to the elements, as well as the number in the row, are not taken into account and the points are not reduced. It also does not evaluate whether elements are centered or nailed to the left. However, size violation is taken into account, be careful!
❗ **Important note #4**: Checking for full compliance with layouts by Perfect Pixel occurs only at the corresponding breakpoints - 1280px, 768px, 320px. At all intermediate values, the absence of exact following of indents and sizes is allowed, but it is recommended to follow the principles of the arrangement of certain elements that are not noted in specific requirements.

---

❗ **Check out some definitions**:

- A **padding violation** is a situation where the distance between elements, or the distance from an element to the edge of the container it is contained in, differs from the one set on the layout by more than 10 pixels in height or width.
  Consider the situation using the `our friends` section as an example. You will most likely know the approximate distance between elements by eye. However, you are confused by the indentation of the "left" button from the edge of the screen on the left. The distance from the "left" button to the left border of the block is 40px on a screen width of 1280px. So, setting the width to 1280px, we look at the distance. If it differs by up to 10px inclusive (for example, 50px or 30px) - do not remove points. However, if the indents are greater than these values ​​(for example, 51px or 29px), we remove the specified number of points.
- **Size Violation** is a situation when the dimensions of elements (buttons, pictures, animal cards, icons) differ from those specified on the layout by more than 10 pixels in height or width. The check is carried out in the same way as in case of violation of indents, and if the differences are large, we remove the specified number of points.
- The length of the text and words in width, as well as the order of word wrapping in lines, we **do not take into account when checking**.
- **Unique error** is the new error found in the block being checked. Regardless of how many times this error is repeated in the block being checked, the specified number of points is deducted only 1 time.
  For example, the button in all animal cards moved out. We will remove points only once, because most likely the general style is broken. If there is only one card with the button that has moved down (and in the rest the button is in its place), we still remove the indicated number of points. Those, there is no difference, the error is in one repeated element, or in several.

### General check of application behavior when window width is changed

Even if the screen is stretched to 4k, even if it is reduced to 320px, the integrity of the application should not be lost. With smooth resizing, we do not take into account the exact calculations of the location of elements. At this stage, the **Google Chrome** browser checks for:

- no horizontal scroll bar on any screen width up to 320px;
- elements should not go beyond the side borders of the screen\* for any screen width up to 320px.

  If both conditions in the **Google Chrome** browser are met (the site behaves responsively, the elements and the general structure change sizes along with the change in width, the horizontal scrollbar does not appear and the elements do not go beyond the sides of the window), then set **+ 50** per page. In total, we put **+100** for 2 pages.
  If a horizontal scrollbar appears on the page, or if the content goes beyond the side of the screen, set **0** per page.\*\*

  After checking the responsiveness of the layout in the Google Chrome browser, a similar check is performed in the **Mozilla Firefox** browser, in which:

- if when resizing the browser window from the maximum to 320px a horizontal scrollbar appears, or the content goes off the screen, **-20** is removed.
- if the horizontal scrollbar does not appear when the browser window is resized from the maximum to 320px, the content does not go off the screen, but some other layout problems appear (other than those in Google Chrome) - ** -5 is removed for each** with a description of the problem, but **no more than -20**.

  The maximum number of points that can be deducted if there are errors during the check in the browser **Mozilla Firefox** - **-20**.\*\*\*

  \* _when the screen width is <768px, the burger menu can go beyond the side border of the screen. Because this is normal practice, it is not considered an error if the horizontal scrolling does not appear on the page._
  \*\* _if a page is set to 0 during the general check, no further criteria related to that page are checked._
  \*\*\* _further check only happens in Google Chrome browser_

### 1280px <= width (maximum -10 points per page)

When checking on large screens, it is acceptable:
**1) block backgrounds are stretched to the full width of the window**, while the content itself is in the center of the screen and corresponds to the layout;
**2) the layout occupies a maximum width of 1280px** and matches the layout, is centered with equal indents on the left and right, the free space is filled with any color;

For any of the cases above, it is **considered an error** if the content is not centered, i.e. aligned to the right or the left side. In case of such an error **removed -10** points per page.
If the content is centered, it checks if it matches the 1280px layout, for this:

- set window width to 1280px
- check for indentation violations or size violations.
  For each unique error in indentation violation or size violation, **-3** is deducted, **but not more than -10 in total**.

**3) content is stretched across the entire width of the window**:

In this case, the following conditions are additionally checked:

#### Main Page

Check if the following conditions for responsive layout are met:

- `Header` and `Not only` section background is stretched.
- The picture of the dog in the `Not only` section does not intersect with the text.
- All paragraphs with text to the right of the cat and dog picture are left aligned in the `About the shelter` section.
- In the `Our friends` section, the text, slider and bottom button are centered.
- All paragraphs with text and a link with the card number to the right of the dog picture are left aligned in the `In addition` section.
- Icons and text in both columns are aligned to the left of their columns in the `Footer` section.

If the conditions are violated, **-5** is deducted for each item.
If blocks or elements go beyond the screen, or overlap each other, **-5** is deducted for each unique error.

Compliance with the main-1280 layout is checked, for which:

- set window width to 1280px
- check for indentation violations or size violations.
  For each unique mistake in violation of indents or violation of dimensions, **-3** is deducted, **but not more than -10 in total, including deduction of points for violating responsive layout conditions**.

#### Pets Page

Check if the following conditions for responsive layout are met:

- `Header` is always visible and is at the top of the page, including when scrolling.
- In the `Our friends` section there are 8 pet cards, 2 rows of 4 elements.
- In the `Our friends` section, all elements and blocks with elements are centered. If a pagination is found to have a flaw or layout inaccuracy, make sure the problem still exists after you set the width and **reload the page** before lowering the score.
- When opening the page, the number "1" should be in the pagination, and the buttons on the left are inactive.
- Icons and text in both columns are aligned to the left of their columns in the `Footer` block.

If the conditions are violated, **-5** is deducted for each item.
If blocks or elements go beyond the screen, or overlap each other, **-5** is deducted for each unique error.

A check is made to match our-pets-1280 layout, for this:

- set window width to 1280px
- check for indentation violations or size violations.
  For each unique mistake in violation of indents or violation of dimensions, **-3** is deducted, **but not more than -10 in total, including deduction of points for violating responsive layout conditions**.

### 768px <= width < 1280px (maximum -15 points per page)

#### Main Page

Check if the following conditions for responsive layout are met:

- `Header` and `Not only` section background is stretched.
- The picture of the dog below in the `Not only` ыусешщт does not intersect with the text.
- All paragraphs with text are aligned to the left in the `Not only` section. The blocks themselves are centered.
- "Make a friend" button is centered.
- All paragraphs with text are aligned to the left in the `About the shelter` section. The blocks themselves are centered.
- In the `Our friends` section, the text, slider and bottom button are centered.
- There are 2 pet cards in the `Our friends` section in the slider.
- All paragraphs with text, as well as a link with a card number, are left-aligned in the `In addition` section. The blocks themselves are centered.
- Icons and text in both columns are aligned to the left of their columns in the `Footer` section.
- The picture of the dog below in the `Footer` section does not intersect with the text.

If the conditions are violated, **-5** is deducted for each item.
If blocks or elements go beyond the screen, or overlap each other, **-5** is deducted for each unique error.

Compliance with the main-768 layout is checked, for which:

- set window width to 768px
- check for indentation violations or size violations.
  For each unique mistake in violation of indents or violation of dimensions, **-3** is deducted, **but not more than -15 in total, including deduction of points for violating responsive layout conditions**.

#### Pets Page

Check if the conditions for responsive layout are met:

- `Header` is always visible, located at the top of the page, including when scrolling.
- In the `Our friends` section there are 6 pet cards, 3 rows of 2 elements.
- In the `Our friends` section, all elements and blocks with elements are centered. If a pagination is found to have a flaw or layout inaccuracy, make sure the problem still exists after you set the width and **reload the page** before lowering the score.
- When opening the page, the pagination should have the number "1", and the buttons on the left are inactive.
- The picture of the dog below in the `Footer` section does not intersect with the text.

If the conditions are violated, **-5** is deducted for each item.
If blocks or elements go beyond the screen, or overlap each other, **-5** is deducted for each unique error.

The our-pets-768 layout check is performed, for this:

- set window width to 768px
- check for indentation violations or size violations.
  **-3** is deducted for each unique error in indentation or size violation, **but not more than -15 in total, including deduction for violation of responsive layout conditions**.

### 320px <= width < 768px (maximum -15 points per page)

#### Main Page

Check if the following conditions for responsive layout are met:

- `Header` and `Not only` section background is stretched.
- Menu in `Header` is hidden (becomes burger menu), burger icon appears in `Header`.
- All paragraphs with text and the button are centered in the `Not only` section.
- The picture of the dog below in the `Not only` section does not intersect with the text.
- All paragraphs with text are centered in the `About the shelter` section. In this case, the text in the paragraphs, but not the title, is aligned to the width of the paragraph.
- In the `Our friends` section, the text, the card in the slider, the block with the slider buttons and the bottom button are centered.
- There is 1 pet card in the `Our friends` section in the slider.
- All paragraphs with text, as well as a link with a card number, are centered in the `In addition` section. At the same time, the text in paragraphs, but not headings and a link with a card number, is aligned to the width of the paragraph.
- Headings with text, icon and email address, icon and phone number and dog picture at the very bottom are centered in the `Footer` section.
- Location and address icons are left aligned and the block itself is centered. If locations and icons are completely centered - this is not a mistake, we do not deduct points!

If the conditions are violated, **-5** is deducted for each item.
If blocks or elements go beyond the screen, or overlap each other, **-5** is deducted for each unique error.

The main-320 layout check is performed, for this:

- set window width to 320px
- check for indentation violations or size violations.
  For each unique mistake in violation of indents or violation of dimensions, **-3** is deducted, **but not more than -15 in total, including deduction of points for violating responsive layout conditions**.

#### Pets Page

Check if the conditions for responsive layout are met:

- `Header` is always visible and is at the top of the page, including when scrolling.
- Menu in `Header` is hidden (becomes burger menu), burger icon appears in `Header`.
- In the `Our friends` section there are 3 pet cards, 1 column with 3 elements.
- In the `Our friends` section, all elements and blocks with elements are centered. If a pagination is found to have a flaw or layout inaccuracy, make sure the problem still exists after you set the width and **reload the page** before lowering the score.
- When opening the page, the number "1" should be in the pagination, and the buttons on the left are inactive.
- Headings with text, icon and email address, icon and phone number and dog picture at the very bottom are centered in the `Footer` section.
- Location and address icons are left aligned and the block itself is centered. If locations and icons are completely centered - this is not a mistake, we do not deduct points!

The our-pets-320 layout check is performed, for this:

- set window width to 320px
- check for indentation violations or size violations.
  For each unique mistake in violation of indents or violation of dimensions, **-3** is deducted, **but not more than -15 in total, including deduction of points for violating responsive layout conditions**.
