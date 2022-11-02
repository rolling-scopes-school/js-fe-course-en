# Online-zoo

Online-zoo is a platform that contains information about animals from various zoos with webcams. 
It is assumed that a user can open the page with zoo resources, observe one of the animals, or make a donation that will be used to purchase food. As part of the task, we should make an adaptive layout and interactivity of the main page, and the page with donations.

**[PetStory-online](https://www.figma.com/file/ypzT9idgAILaSRVRmDAJxn/online-zoo-3-weeks)**  
Link text: https://www.figma.com/file/ypzT9idgAILaSRVRmDAJxn/online-zoo-3-weeks

## Task completion steps

**[Week 1](#week-1)**: Fixed page layout `desktop_petstory`.
- At this stage, you should create a fixed layout of `desktop_petstory` page. With a fixed layout, the page looks the same with a window width of 1600px. The task should be checked at the same window width.
- 
**[Week 2](#week-2)**: Fixed page layout `desktop_donate`.
- At this stage, you should create a fixed layout of the `desktop_donate` page. With a fixed layout, the page looks the same with a window width of 1600px. The task should be checked at the same window width.

**[Week 3](#week-3)**: Adding adaptive layout.
- At this stage, you should adapt the previously created pages according to the layout for different window widths from the maximum to 320px inclusive. In this case, it will be necessary to adapt decorative elements.


**[Week 4](#week-4)**: Adding additional functionality.
- at this stage, additional functionality is added to the previously made pages: menu, slider, pagination, and popup.

## Task verification

- - The task will be checked by the cross-check flow. **There will be 4 checks in total, at each stage of the task.** [How to perform cross-check](https://docs.app.rs.school/#/platform/cross-check-flow).
    - [Cross-check evaluation criteria. Week 1](#cross-check-evaluation-criteria-week-1).
    - [Cross-check evaluation criteria. Week 2](#cross-check-evaluation-criteria-week-2)
    - [Cross-check evaluation criteria. Week 3](#cross-check-evaluation-criteria-week-3)
    - [Cross-check evaluation criteria. Week 4](#cross-check-evaluation-criteria-week-4)

## Creation of a copy of the layout

The first thing to do is the creation of your copy of the Figma designs. To do so:

- authorize on [Figma](https://www.figma.com/);
- navigate to the [layout](https://www.figma.com/file/ypzT9idgAILaSRVRmDAJxn/online-zoo-3-weeks);
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


- Create a public repository named online-zoo on your GitHub account.
- You may use the example of project structure below. Since the project will contain several pages (2), at the same level as `assets` there will be the `pages` directory. Inside `pages`, in the `main` folder (same as the page name), the `.html`, `.css` and `.js` files related to this page will be stored. The `assets` directory will still contain images, icons, and font files if any. The folders inside `assets` will be named depending on the content: `images`, `icons`, `fonts`. Example below:
- ![online-zoo folder structure](online-zoo-folder-structure.jpg)
- You should deploy your task using gh-pages or by any other means.
- The commit history should reflect the development process of the application. Commit names should match the [commit requirements](https://docs.rs.school/#/git-convention)

### Additional requirements for the repository to complete the third and fourth parts of the task
- a job can be run on the same branch `online-zoo` or on a new branch.
- if the job is running on a new branch:
  - a new branch is created from the `online-zoo` branch, for example, online-zoo-part2`;
  - in the new branch, work is being done on the task;
  - when a part of the task is completed, a Pull Request is raised from the `online-zoo-part2`(`online-zoo-part3`, ...) to the `online-zoo` branch, followed by a merge. The title and content of this PR don't matter;
- a new deployment of your work is created in a branch `gh-pages` from the `online-zoo`.
- the open **Pull Request** is updated to the branch `main` from the branch `online-zoo`. This PR is not merged.

## Useful links

Fonts can be found here:

[Arial, google fonts](https://www.fonts.com/font/monotype/arial?QueryFontType=Web&src=GoogleWebFonts)  
[Georgia, google fonts](https://www.fonts.com/font/microsoft-corporation/georgia?QueryFontType=Web&src=GoogleWebFonts)

You can connect fonts by either downloading local files or connecting fonts via URL to google fonts. If you can't find or download the font you need, just replace it with a font with the same serif type.

## <a id="week-1"></a> Week 1

All pages are created for a screen width of **1600px**.

### Technical requirements

Maximum score: **70** 

#### General
All layout background elements should stretch to the full available screen width if the width is greater than 1600px. In this case, the guides must be kept in their original size, 1160px. The features of this project are:
-	custom sizes,
-	additional visual elements.

To create vertical margins, it's best to use vertical margins on higher-order boxes as much as possible. Keep in mind that vertical margins can collapse.

To create multi-column structures or elements that have a relative horizontal layout, one of the following properties should be used:
- display: flex
- display: grid
- display: inline-block

❗Maintaining padding between elements is more important than the size of these elements. You can often see rough values (like 369px x 548px), but this only means that the dimensions were calculated taking into account the distance between the guides and the padding between the elements.
#### Landing (70 pints)
1.	 **Header** (`<header>` contains only logo, navigation bar)
      - The logo is on the left. Clicking on the logo works like clicking on `About`, redirects us to the current page, 
   to petstory (Landing).
      - Interactive navigation bar. Clicking on menu items for which no page exists may do nothing.
      - The element `About` should be highlighted by default. And it should stop being interactive when other menu items are clicked.
      - Clicking on `Donate` takes us to the donate page.
      - Clicking on `Designed by ©` takes us to the original [Figma](https://www.figma.com/file/jfEFwkXVj1WRq7sUHDr8os/PetStory-online).
      - There should be one element per page `<h1>`. It should contain the text `PetStory Online`.
      - You don't need to make the header sticky. When scrolling, it remains in its position.


2.	**Watch your favorite animal online** block
      -	The background is a picture.
      -	The button `Watch online` should be interactive. When pressed, nothing happens.


3.	**The Backstage** block
      -	Image and text - two-column layout.


4.	**Pets** block
      - The left and right buttons should be clickable. When pressed, nothing happens.
      - Animal cards should be interactive.
      - ❗ When you hover over the cursor, there should be an animation of the exit of the text from the bottom of 
      the picture, where there will be information about the name of the animal and location with a darkened background.
      The picture itself, but not the card, should grow 10px in each direction from the center.
      - The button `Choose your favorite` should be interactive. When pressed, nothing happens.

5.	**Pick and feed a friend** block
      -	The text `Emergency support Fund` should be a link. Clicking redirects us to *donate*.
      -	The button `Feed a friend now` should be interactive. Clicking redirects us to *donate*.


6. 	**Testimonials** block
      - The progress bar should be interactive. We start in the extreme left position. When pressed, nothing happens.
      - The button `Leave feedback` should be interactive. When pressed, nothing happens.
      - 
7. 	**Footer** ( `<footer>` contains menus, logos, donation and social media buttons):
      -	Clicking on the logo works like clicking on About, which takes us to the top of the current page, to *petstory (Landing)*.
      -	The button `Donate for volunteers` should be interactive. Clicking redirects us to *donate*.
      -	Interactive social media panel. Clicks on social networks (icon + text) can simply lead to the main pages of the corresponding resources.
      -	Email - field `input` with type `email`.
      -	The button `submit` should be in the *mistake* position. If the field `email` passes validation, it goes into the *default* state.
      -	Interactive navigation bar. Clicking on menu items for which no page exists may do nothing.
      -	The element `About` should be highlighted. And it should stop being interactive.
      -	❗If it is not possible to select the required text thickness, use close [saturation values](https://developer.mozilla.org/ru/docs/Web/CSS/font-weight) , +-100.


## <a id="cross-check-evaluation-criteria-week-1"></a> Cross-check evaluation criteria. Week 1
Open at **1600px** screen width. If the screen is smaller, you can zoom in, or you can set the page width to 1600px and watch with horizontal flat scrolling enabled. If the screen is wider, you can make the area narrower or narrow the window.
❗The score cannot drop below **0** per page. Also, there can be no more penalty points than for the absence of a block (For example, if there is a block header, and there are more penalty points than 20, then we remove 20). Unless specified separately in the requirements, then for all non-repeating blocks or elements at rest (without hover) the following is true:
-	The padding from the borders of elements (or sets of elements) to the edges of the block, horizontally or vertically,
differs by more than 20px: **-5** once per global block (header, main, footer).
-	The padding within a set or grid between elements, horizontally or vertically, differs by more than 10px: **-5** once per block.
-	Missing element or picture, both background and element picture: **-5** once per block. If the image or element is 
present on the page, has the correct size and padding, but the design is broken: **-2** once for each block.
-	The background color of a block or element is very different from the design (Difference in one of the RGB channels
by more than 34. For example, #bbb and #ddd is not an error, more is an error): **-2** once for each block.
-	Font or font-family is not included, or the difference in font size is more than 4px: **-2** once per block.
**Landing** page created : **+70** . Otherwise, if the page doesn't exist, set it to **0** and move on to the next page.
1.	No **Header** block : **-20** .
      -	No logo: **-5** . There is a logo, but it doesn't work as a link to petstory (Landing): **-2** .
      -	No navigation bar: **-10** . The navigation bar is there, but not interactive: **-5**.
      -	There is no element `About`, or it is not highlighted: **-2**.
      -	There is no element `Map`, or it is not interactive: **-2**.
      -	There is no element `Zoos`, or it is not interactive: **-2**.
      -	There is no element `Donate`, or it's not interactive, or it doesn't work as a link to donate : **-2**.
      -	There is no element `Contact Us`, or it is not interactive: **-2** .
      -	There is no element `Designed by ©`, or it's not interactive, or it doesn't work as a link to the original Figma page : **-2**.
      -	No element `<h1>`: **-5** . There is an element, but there is more than one: **-2**.
      -	It is recommended not to make the header "sticky". If it is "sticky", then we do not reduce points.
2.	There is no **Watch your favorite animal online** block: **-10**.
      -	No button `Watch online`: **-5**. The button is there, but not interactive: **-2**.
      -	❗If the button `watch online` has the text "wath online" - we do not consider it an error, we do not remove points.
      -	No background image: **-5**.
3.	There's no **The Backstage** block: **-10**.
      - No picture of the plant on the right: **-5**.


4. 	There's no **Pets** block: **-30**.
      - No right button: **-5** . No left button: **-5** . There are buttons, but they are not interactive: **-2** .
      - No animal card: **-5** each. The card is there, but not interactive, or there is no animation of the text on a
darkened background (the background can be a gradient): **-2** for each. Below are examples of animations that we count as correct:
        - The picture is darkened (a translucent background is superimposed, or the picture itself becomes translucent) 
        and a hidden inscription pops up (light or dark does not matter, the main thing is that it is readable against 
        the background of the picture). The inscription can be on top of the picture, in the center, or even at 
        a slight distance from the bottom.
        - The picture is dimmed and the text under the picture floats up, while the original state of the text can either 
        be preserved or not.
        - The description text moves out along with the background.
        - On top of the picture without darkening, the text pops up from under the picture to the top, and the block 
        with the text itself being darkened (in this case, the color of the text may turn white, for example).
      - It is recommended to use animation with 10px zoom in each direction. If the value of the increase is different,
   or there is no increase, we do not reduce the points.
      - The speed of the animation does not matter, but there must be a non-zero value for the animation
   time. We do not reduce points at any speed.
      - No button `Choose your favorite`: **-5**. The button is there, but not interactive: **-2**.
      - No plant picture on the left: **-5**. No picture of the plant on the right: **-5**.
5. No block **Pick and feed a friend**: **-10**.
      - No button `Feed a friend now`: **-5**. The button is there, but not interactive: **-2**.
      - The text `Emergency support Fund` is not a link, or does not work as a link to donate: **-2**.
      - It is recommended to make arrows of the same size. If the arrows are of different sizes, we do not reduce points.
6. No **Testimonials** block : **-10**.
      -	No button `Leave feedback`: **-5**. The button is there, but not interactive: **-2**.
      -	No progress bar: **-5**. Broken strip design: **-2**.
      -	It is recommended to make the progress bar through input type range, and style accordingly. If the element is 
not completed through the input type range, then we do not remove points.
      -	No picture of the plant on the right: **-5**.
7.	No block **Footer** : **-20**.
      - No logo: **-5**. There is a logo, but it doesn't work as a link to _petstory (Landing)_: **-2**.
      - No button `Donate for volunteers`: **-5**. The button is there, but not clickable, or doesn't work as a link to donate: **-2**.
      - At least one social media icon is missing: **-5** for the entire set of elements.
      - All social network icons are there, but at least one is not interactive: **-2** for the entire set of elements.
      - No field `<input>` "Input your email" : **-5** . The field exists, but the type is not specified email: **-2**.
      - It is recommended to mark `<input>` with the required attribute. No points are deducted for its absence.
      - It is recommended to wrap the entire field in an element `<form>`. No points are deducted for its absence.
      - No button `Submit`: **-5** . The button is there, but not interactive: **-2**.
      - It is recommended that the button `Submit` use the _default_  style until the input field is focused. If the default 
      button style is active or mistake, no points are deducted.
      - There is no element `About`, or it is not highlighted: **-2** .
      - There is no element `Map`, or it is not interactive: **-2** .
      - There is no element `Zoos`, or it is not interactive: **-2** .
      - There is no element `Contact Us`, or it is not interactive: **-2** .

## <a id="week-2"></a> Week 2
All pages are created for a screen width of **1600px**.
### Technical requirements
Maximum score: **30**
#### General
All layout background elements should stretch to the full available screen width if the width is greater
than 1600px. In this case, the guides must be kept in their original size, 1160px. The features of this project
are:
-	custom sizes,
-	additional visual elements.

To create vertical margins, it's best to use vertical margins on higher-order boxes as much as possible. Keep in mind that vertical margins can collapse.

To create multi-column structures or elements that have a relative horizontal layout, one of the following properties must be used:
- display: flex
- display:grid
- display: inline-block

❗Maintaining padding between elements is more important than the size of these elements. You can often see rough
values (like 369px x 548px), but this only means that the dimensions were calculated taking into account the
distance between the guides and the padding between the elements.

#### Donate (30 points)

1.	**Header** ( `<header>` contains only logo, navigation bar)
      - The logo is on the left. Clicking on the logo works like clicking on `About`, redirects us to the current page, 
      to _petstory (Landing)_.
      - Interactive navigation bar. Clicking on menu items for which no page exists may do nothing.
      - Clicking on takes `About` us to _petstory (Landing)_.
      - Clicking `Donate` may not do anything. Or it can transfer to the donate page .
      - Clicking on `Designed by ©` takes us to the original [Figma](https://www.figma.com/file/jfEFwkXVj1WRq7sUHDr8os/PetStory-online) page .
      - There should be one `<h1>` element per page . It should contain text `PetStory Online`.
      - You don't need to make the header sticky. When scrolling, it remains in its position.


2. Block **Pick and feed a friend**
      -	The area within 20px of the yellow dot should be clickable. When pressed, nothing happens.
      -	Another amount is a `input` field type  `number` with [hidden arrows](https://www.w3schools.com/howto/howto_css_hide_arrow_number.asp).
The `$` sign should always be present inside a field. There should be a 4 characters limit.
      -	`Monthly` and `Once` are mutually exclusive fields `input` of type `radio`.
      -	❗The field `Once` should be enabled by default. Thus, when opening the page, or reloading.
      -	The button `Feed a friend now` should be interactive. When pressed, nothing happens.


3.	**Footer** ( `<footer>` contains menus, logos, donation and social media buttons):
      - Clicking on the logo works like clicking on About, takes us to the top of the current page, to _petstory (Landing)_ .
      - The button `Donate for volunteers` should be interactive. Pressing may not do anything. Or it can transfer to the _donate_ page .
      - Interactive social media panel. Clicks on social networks (icon + text) can simply lead to the main pages of the corresponding resources.
      - Email - field `input` with type `email`.
      - The button `submit` should be in the _mistake_ position . If the field `email` passes validation, it goes into the _default_ state .
      - Interactive navigation bar. Clicking on menu items for which no page exists may do nothing.
      - Clicking on takes `About` us to _petstory (Landing)_ .
      - ❗If it is not possible to select the required text thickness, use close [saturation values](https://developer.mozilla.org/ru/docs/Web/CSS/font-weight) , +-100.


## <a id="cross-check-evaluation-criteria-week-2"></a> Cross-check evaluation criteria. Week 2
**Donate** page created : +**30** . Otherwise, if the page does not exist, set to **0** .
1. No **Header** block : **-20** .
      -	No logo: **-5** . There is a logo, but it doesn't work as a link to _petstory (Landing)_ : **-2** .
      -	No navigation bar: **-10** . The navigation bar is there, but not interactive: **-5** .
      -	Element missing `About` or not working as a _petstory (Landing)_ link : **-2** .
      -	There is no element `Map`, or it is not interactive: **-2** .
      -	There is no element `Zoos`, or it is not interactive: **-2** .
      -	There is no element `Donate`, or it is not highlighted: **-2** .
      -	There is no element `Contact Us`, or it is not interactive: **-2** .
      -	There is no element `Designed by ©`, or it's not interactive, or it doesn't work as a link to the original Figma page : **-2** .
      -	No element `<h1>`: -5 . There is an element, but there is more than one: -2 .
      -	It is recommended not to make the header «sticky".

2. No block **Pick and feed a friend** : **-30** .
      -	An area within a 20px radius of at least one yellow dot is non-interactive: **-5** for the entire block.
      -	No field `<input>` "Another amount" : **-5** . The field exists, but the type is not specified number: **-2** .
      -	No field `<input>` "Monthly" : **-5** . The field exists, but the type is not specified radio: **-2** .
      -	No `<input>` "Once" field: **-5** . The field is present, but the type is not specified radio, or it is not 
selected as the default value: **-2** .
      -	There are `Monthly` and `Once` fields, but they are not mutually exclusive: **-5** .
      -	No button  `Feed a friend now`:  **-5** . There is a button, but it is not interactive:  **-2** .

3. No block **Footer** : **-20** .
      -	No logo: **-5** . There is a logo, but it doesn't work as a link to _petstory (Landing)_ : **-2** .
      -	No button `Donate for volunteers`: **-5** . The button is there, but not clickable, or doesn't work as a link to _donate_ : **-2** .
      -	At least one social media icon is missing: **-5** for the entire set of elements.
      -	All social network icons are there, but at least one is not interactive: **-2** for the entire set of elements.
      -	No field `<input>`c"Input your email" : **-5** . The field exists, but the type is not specified `email`: **-2** .
      -	It is recommended to mark `<input>`cwith the required attribute. No points are deducted for its absence.
      -	It is recommended to wrap the entire field in an element `<form>`. No points are deducted for its absence.
      -	No button `Submit`: **-5** . The button is there, but not interactive: **-2** .
      -	It is recommended that the Submit button uses the _default_ style until the input field is focused. 
If the default button style is active or mistake , no points are deducted.
      -	Element missing `About` or not working as a _petstory (Landing)_ link : **-2** .
      -	There is no element `Map`, or it is not interactive: **-2** .
      -	There is no element `Zoos`, or it is not interactive: **-2** .
      -	There is no element `Contact` Us, or it is not interactive: **-2** .


## <a id="week-3"></a> Week 3
The rendered pages adapt to the following device screen width:
-	1600px (to be done)
-	1000px
-	640px
-	320px

### Technical requirements
Maximum score:: **100**

#### General
The transition points can be arbitrary. We will not evaluate how correctly and conveniently they are selected. Below 
are recommendations for those who have not yet completed the task:
1. `(max-width: 1600px) or (max-width: 1599px)` - Transition between fixed and responsive column states.
      - Optional (max-width: 1599px) or (max-width: 1440px) or (max-width: 1280px) or (max-width: 1220px)
2. `(max-width: 1000px)` - Change left/right buttons layout in the block Pets. Please note that the cards may be different 
when the screen width is changed, the sequence of cards (names, pictures) does not play a role. Changing the number of 
reviews in the block `Testimonials`, while the text itself does not play a role in the review, only the size is important.
   - Optional (max-width: 999px) or (max-width: 980px) or (max-width: 768px)
3. `(max-width: 640px)` - Replacing the menu in the header with a burger menu. The header becomes fixed. Loss or
transformation of some elements, and change of location in blocks `The backstage`, `Pick` and `feed a friend`. Changing the 
number, size and indentation of animal cards in the block `Pets`. Changing the location of reviews in the block `Testimonials`.
   -- Optional (max-width: 639px) or (max-width: 600px)
4. (max-width: 320px) - Loss or transformation of some elements, and repositioning in blocks `The backstage`, `Pick` and 
`feed a friend`. Changing the number, size and indentation of animal cards in the block `Pets`. Changing the location 
of reviews in the block `Testimonials`.


   #### General notation:
1. The **specified** elements are the elements that are specified in the requirements, and for which penalty points are 
indicated for this type of error. In addition, if we have already indicated an error for elements, for example, a header
or footer, and it is identically repeated for other sizes or pages, we do not remove points again.
2. **Indents** between elements are the vertical and horizontal indents between adjacent elements, usually in the same
list or in the same grid.
3. Element **spacing** is a designation of padding from an element to the edges of the screen or other elements. For text,
indents are taken into account on the left and top of the first line (text start point), if the text is left-aligned, 
or in headings. As for the transition from the position when all elements are aligned to the left, to the central position,
then here you can see the indents of the block itself, and the presence of properties for positioning the content in the center.
4. The **appearance** of elements is a designation of the appearance of elements. For example, if there is a transition 
from a small round button to a large square button, then attention is focused on the correspondence of the appearance to 
what is given in the design.
5. The **number** of elements is a requirement to match the number of elements in the design. For example, when switching
to a smaller screen size, the number of elements decreases from 6 to 4x. The number of elements greater than or less than 4, 
in this case, will be considered an error.

❗Pay attention to these points:
1. Changing elements with a change in concept is best done through hiding / showing elements. For example, replacing 
pictures of arrows with others in the Pick and feed a friend. Also, in some cases, it will be easier to work with them in js.
2. Burger menu may not be active. If nothing happens when you click on it, then we will not deduct points.
3. On the _Donate_ page , the field Another amount can be located in the center of the page, this is not an error, we do 
not remove points.
❗Features of checking adaptability in DevTools
1. Open developer tools
      - To do this, press the key `F12` or click the right mouse button and select the item `Inspect` from the menu that appears.
      - in the upper right corner of the developer toolbar, click on the icon `Toggle device toolbar`
      - select from the top bar `Responsive`
2. Make sure the mode `Responsive` doesn't have a vertical scrollbar (it doesn't exist by default). If there is a scrollbar, 
it should be removed. For this
      - in the top panel of the device toolbar, switch the device type from `Desktop` to `Mobile`
      - if the device type is not displayed, in the top panel of the device toolbar, click on the three dots on the right 
   and select `Add device type`


## <a id="cross-check-evaluation-criteria-week-3"></a> Cross-check evaluation criteria. Week 3
1. After setting a certain width, when checking the sizes and padding between elements, inside a set of elements or a grid, 
horizontally or vertically, we consider the difference to be more than 10px. You can use the `PixelPerfect` extension.
2. We check the pages for responsiveness, each, except for repeated `Zoos`.


### Landing page
Open the **Landing** page and resize the window. If at the same time the page behaves adaptively, i.e. changes the design 
and arrangement of elements, set **+60** . Otherwise, if the page is static, and keeps the size of 1600px, set it to **0** , 
and move on to rendering the next page.

#### Set the Landing to 1000px. We look at the differences (> 10px) and remove points (but not more than -30) if the following points are violated:
- Indents between menu items in the header: **-5** .
- Location of elements in the block `Watch your favorite animal online`: **-5** .
- Location of elements in the block `The Backstage`: **-5** .
- ❗Not missing a plant in the block `The Backstage`: **-5** . The plant can disappear abruptly, it can smoothly go off the edge of the screen.
- Position or indents between animal cards in the block `Pets`: **-5** . In this case, the sequence (order) of the cards 
is not taken into account.
- Position or padding between right/left buttons in the block `Pets`: **-5** .
- Location or type of plants on the right or left in the block `Pets`: **-5** .
- Quantity, location or indents between reviews in a block `Testimonials`: **-5** . At the same time, what kind of text 
in the reviews is not taken into account.
- Button position `leave feedback` in the block `Testimonials`: **-5** .
- Location or type of plant on the right side of the block `Testimonials`: **-5** .
- Indents between icons and names of social networks in the footer: **-5** .
- Indents between menu items in the `footer`: **-5** .
- ❗The following items are checked only for the _Donate_ page ! There was a mistake with indents on the _Landing_ page , 
so if the padding from the edge is 43px, not 30px, we don’t deduct points.
- Arrangement of elements inside the form `Subscribe to our news` in the footer: **-5** .
- Button `donate for volunteers` position in the footer: **-5** .


#### Set the Landing to 640px. We look at the differences (> 10px) and remove points (but not more than -30) if the following points are violated:
-	Menu not converted to burger menu in header: **-5** .
-	❗The header did not become fixed: **-10** .
-	Location of elements in the block `Watch your favourite animal online`: **-5** .
-	Location of elements in the block T`he Backstage`: **-5** .
-	❗No plant appeared in block `The Backstage`: **-5** . The plant may appear abruptly, may smoothly exit from the edge of the screen.
-	Quantity, arrangement or indents between cards of animals in the block `Pets`: **-5** .
-	Position or indents between right/left buttons in the block `Pets`: **-5** .
-	Type of plants on the right or left in the block `Pets`: **-5** .
-	Location of elements in the block `Pick and feed a friend`: **-5** .
-	❗Type of arrows in the block `Pick and feed a friend`: **-5** .
-	Type, position or indents between reviews in the block `Testimonials`: **-5** .
-	Button position `leave feedback` in the block `Testimonials`: **-5** .
-	Type of plant on the right in the block `Testimonials`: **-5** .
-	❗The form `Subscribe to our news` in the footer did not disappear: `-5` . It should hide
-	Button` donate for volunteers` position in the footer: **-5** .
-	Position or indents between social media icons in the footer: **-5** .
-	❗If names are visible next to the icons of social networks, this is not a mistake, we do not remove points.
-	Indents between menu items in the footer: **-5** .


#### Set the Landing to 320px. We look at the differences (> 10px) and remove points (but not more than -30) if the following points are violated:
- No burger menu in header: **-5** .
- Location of elements in the block `Watch your favourite animal online`: **-5** .
- Location of elements in the block `The Backstage`: **-5** .
- ❗We do not evaluate the accuracy of the location of the plant in the block `The Backstage`, and we do not remove points
for the fact that it is not there. However, if the plant runs over the text: **-5** .
- Quantity, arrangement or indents between cards of animals in the block `Pets`: **-5** .
- ❗The location of the elements in the block `Pets` is not evaluated. On a design with a width of 320px, an error was 
made with indents, and if the column with cards is not centered, but 10px from the edge, this is not a mistake, we do not deduct points.
- ❗The left/right buttons in the block did not disappear `Pets`: **-5** .
- Type of plants on the right or left in the block `Pets`: **-5** .
- Location of elements in the block `Pick` and `feed a friend`: **-5** .
- Type of arrows in the block `Pick` and `feed a friend`: **-5** .
- Position or indents between reviews in a block `Testimonials`: **-5** .
- Button `leave feedback` position in the block `Testimonials`: **-5** .
- Location or type of plant on the right side of the block `Testimonials`: **-5** .
- Location or appearance of the main logo in the `footer`: **-5** .
- Position or indents between social media icons in the `footer`: **-5** .
- Button `donate for volunteers` position in the `footer`: **-5** .
- Indents between menu items in the `footer`: **-5** .

####  We check for compliance with the general design requirements and remove points (but not more than -30) if the following points are violated:
We perform the following steps step by step:
1. We stretch the page to a width greater than 1600px, or reduce the scale.
2. Change the page width to sizes from 1599px to 1001px.
3. Change the page width to sizes from 999px to 641px.
4. Change the page width to sizes from 639px to 321px.
5. Less than 320px - do not look!

And we evaluate:
- At some point narrowing down to 338px, a horizontal scrollbar appears: **-30** once.
- When checking boundary values, at least one element is missing, in addition to the **specified** or background elements,
or there is an extra one: **-5** once for each gap.
- There are elements other than the specified or background elements that are cut off or go off the edge of the 
screen even though they fit within the borders in the design: **-5** once per gap.
- At some point, elements other than the **specified** or background elements run over other elements, although all 
designs have a padding between them: **-5** once per gap.

### Donate Page
Open the **Donate** page and resize the window. If at the same time the page behaves adaptively, i.e. changes the design 
and arrangement of elements, set **+40** . Otherwise, if the page is static, and keeps the size of 1600px, set it to **0** ,
and move on to rendering the next page.

#### Set Donate to 1000px. We look at the differences (> 10px) and remove points (but not more than -20) if the following points are violated:
-	Indents between menu items in the `header`: **-5** .
-	Location of elements in the block `Pick and feed a friend`: **-5** .
-	Field location `Another amount`: **-5** .
-	Arrangement of elements inside the form `Subscribe to our news` in the `footer`: **-5** .
-	Button `donate for volunteers` position in the `footer`: **-5** .
-	Indents between icons and names of social networks in the `footer`: **-5** .
-	Indents between menu items in the `footer`: **-5** .

#### Set Donate to 640px. We look at the differences (> 10px) and remove points (but not more than -20) if the following points are violated:
-	Menu not converted to burger menu in `header`: **-5** .
-	❗The header did not become fixed: **-10** .
-	Location of elements in the block `Pick and feed a friend`: **-5** .
-	❗The form `Subscribe to our news` in the `footer` did not disappear: **-5** . It should hide
-	Button `donate for volunteers` position in the `footer`: **-5** .
-	Position or indents between social media icons in the `footer`: **-5** .
-	❗If names are visible next to the icons of social networks, this is not a mistake, we do not remove points.
-	Indents between menu items in the `footer`: **-5** .

####  Set Donate to 320px. We look at the differences (> 10px) and remove points (but not more than -20) if the following points are violated:
-	No burger menu in `header`: **-5** .
-	Location of elements in the block `Pick` and `feed a friend`: **-5** .
-	Type or location of the main logo in the `footer`: **-5** .
-	Position or indents between social media icons in the `footer`: **-5** .
-	Button `donate for volunteers` position in the `footer`: **-5** .
-	Indents between menu items in the `footer`: **-5** .


#### We check for compliance with the general design requirements and remove points (but not more than -20) if the following points are violated:
We perform the following steps step by step:
1.	We stretch the page to a width greater than 1600px, or reduce the scale.
2.	Change the page width to sizes from 1599px to 1001px.
3.	Change the page width to sizes from 999px to 641px.
4.	Change the page width to sizes from 639px to 321px.
5.	Less than 320px - do not look!
 And we evaluate:
- At some point narrowing down to 338px, a horizontal scrollbar appears: **-20** once.
- When checking boundary values, at least one element is missing, in addition to the **specified** or background elements,
or there is an extra one: **-5** once for each gap.
- There are elements other than the **specified** or background elements that are cut off or go off the edge of the screen 
even though they fit within the borders in the design: **-5** once per gap.
- At some point, elements other than the **specified** or background elements run over other elements, although all designs
have a padding between them: **-5** once per gap.

## <a id="week-4"></a> Week 4
Adding JavaScript.
Maximum score: **100**

### Technical requirements


#### General
We will not check and evaluate the quality of the design. Spelling errors are also ignored. Some terms:
1. Carousel (carousel) implies a smooth scrolling of elements from left to right, or vice versa. Thus, should be animation.
2. Popup (pop-up) - a modal window that pops up on top of the screen, and does not allow the user to use the rest of the 
application until he closes it.
3. ❗When we check conditions for different screen widths, we don't just stretch the screen to the desired width, but do a page reload!

#### Landing & Donate
1.	The menu in `header` as soon as the navigation bar turns into a burger menu (for a screen width of 640px or less).
      - Should open on click.
      - When opened, a menu appears, as in the [layout](https://www.figma.com/file/ypzT9idgAILaSRVRmDAJxn/). However, 
      the layout lacks a close button (such as a cross, or other visual element) in the upper right corner, so you should
      to add it to your taste. You can take it from the review popup design.
      - The area under the open menu is darkened to the entire available screen height (a translucent background is superimposed).
      - Clicking on the cross or clicking on the shaded area should close the menu.
      - When closed, the darkened area below the menu should disappear.


#### Landing
1. **Carousel** in a block `Pets` for screen widths of 1600px, 1000px and 640px.
      - The blocks should be flipped to the right / left by pressing the corresponding button endlessly. Thus, sequential 
      generation and removal of blocks, or replacement with existing ones and rearranging them back and forth.
      [Basic slideshow, including automatic](https://www.w3schools.com/howto/howto_js_slideshow.asp)
      [Carousel Example: pure js arrow carousel](https://codepen.io/tuesta/pen/QoMqBY)
      - The order of the pictures is generated randomly! At the same time, in one slide, all pictures should be unique.
      - In the block where 6 cards of animals are displayed, flipping should occur at once 6 elements at a time. With a
   smaller number, a smaller number of elements inside will be flipped.
      - It is important to check the condition to ensure that our blocks perform exactly one movement at a time. This 
   means that while the animation is going on, the user cannot click on the button several times in a row. And if there is such an opportunity, then the animation happens once, and only when you click after the completion of the first animation, the second one will occur.
2. **Carousel** in a block `Testimonials` for screen widths of 1600px and 1000px.
      - At least 11 testimonials should be generated. They can be any text, as well as names and photos of users. Unlike 
   the carousel in the _Pets_ block , reviews are only generated once. Or you will always have the same set
      - In total there will be 8 values in the intervals. Or a range of values from 0 to 7: 0, 1, 2, 3, 4, 5, 6, 7.
      - The progress bar should be tied to a specific intermediate interval.
      [Progress bar example](https://codepen.io/juanbrujo/pen/uIqaw)
      - A shift by one will mean the appearance of only one new review.
      - Scrolling through reviews should also occur by moving the slider on the progress bar. In the leftmost position
   of the slider, the first reviews will be visible. In the extreme right position of the slider, the latest reviews 
   will be visible. It is recommended to reduce the size of the orange slider to 1/8 (12.5%) of the total length of the 
   strip. You can leave it the way it is.
      - When moving from 1600px to 1000px, the number of intervals may increase by 1. Or it may remain in the amount of 
   8 values. Count on the option.
3. **Popup** when clicking on a review in a block `Testimonials` for screen widths of 640px and 320px.
      - The popup should be opened by clicking on the review.
      - When you open it, a review appears, as in the design, as well as a cross in the upper right corner. 
   There will be an outer area around the review that overlaps the page. In this case, it is desirable that the darkening 
   be done with a semi-transparent shadow around the feedback itself. If an opaque white background is used, or a partial 
   background transferred from the design along with the dimensions, this will not be considered an error.
      - Clicking on the cross, or clicking on the shaded outer area should close the popup. If the review is shown against 
   the background of a white cropped rectangle (as in the figma design), in which the review and the cross are located, 
   and clicking on the white block around the review does not close the popup, then we check the area around the white block. 
   In this case, it should be dimmed and close the popup on click. This decision is not a mistake.
      - When closed, the darkened area under the popup should disappear.



#### Donate
1.	**Amount panel** in a block `Pick and feed a friend` for screen widths of 1600px, 1000px, 640px or less.
- When you click on the circle on top of the amount, it should become highlighted, and the previous active circle should become inactive.
- The specified amount when clicking on the circle should be written in the `Another amount` field.
- The required field `Another amount` should be limited to 4 characters of type number.
- At the start of the page display, the number 100 should be entered, and the corresponding element (3rd from the right) should be highlighted.
- If you enter a number in the `Another amount` field that matches one of the amounts in the Amount bar at the top, the 
corresponding circle should become highlighted.
- Animation at this point can not be added


## <a id="cross-check-evaluation-criteria-week-4"></a> Cross-check evaluation criteria. Week 4
1. When checking, deviations of elements or blocks from the design are not taken into account, except for the elements 
that are **specified** in the TR, and we do not remove points for design errors.
2. Points within one task cannot fall below 0. For example, the task indicates +10 , and during the check you counted -18 .
Then, the output score for the task will be 0 . 
3. ❗If you set a new screen width and check the items, and the animation or functionality does not behave correctly, 
make sure you do a page reload. If after that errors still occur - only then we remove points.


#### Landing & Donate
Menu (burger menu) in **header**.
1. Open at a screen width of **640px** or less so that the main navigation menu is hidden and the burger menu is visible.
If the burger menu opens, put **+10** . If the menu does not open on click, set **0** for this item and move on to the next one. 
Points are deducted if:
      -	Missing dimming or close button (cross or other visual element): **-5** . And the points below are also taken into account.
      -	Clicking the close button (cross or other visual element) or dimmed menu area does not close the menu: **-5** .
      -	Checking `About` and `Donate`. Menu items don't work as links: **-5** .

#### Landing
**Carousel** in a block `Pets`.
1. Open at a screen width of 1600px or more so that the 6 animal cards are visible, and the arrows on the side of them.
If the carousel is done and responds to pressing the right / left buttons, set +30 . If the carousel does not respond -
put **0** for this item and move on to the next one. Points are deducted if:
   - From the moment of loading, we press the "left" button several times, at least 5 times, we look for all the cards 
   to be flipped constantly. If a boundary condition appears and the button disappears or stops working 
   (cards stop scrolling when pressed): **-5** .
   - From the moment of loading, we press the "right" button several times, at least 5 times, we look for the cards 
   (all, or one column) to be flipped constantly. If a boundary condition appears and the button disappears or stops 
   working (cards stop scrolling when pressed): **-5** .
   - There is no animation or the animation time is 0: **-10** . Its appearance is a smooth flipping of the image from
   right to left, or from left to right. In this case, the animation speed is not regulated, but it must be non-zero.
   ❗For the lack of animation on smaller screen sizes, we do not take points again!
   - While the slide is static (not during animation), the cards are repeated: **-5** .
   - We check the condition of random generation. When you press the button left and right, or vice versa, a new set of
   cards will be generated each time. If their state is preserved: **-5** .
   - Try to reload the page, maybe a couple of times, and scroll left and right. If after the reboot you see the same
   order of cards on the right or left as before the reboot: **-5** . The starting (very first) set of cards can remain the same.
   - We try to click on the button very quickly several times so that the clicks fit at the moment while the animation 
   is happening. If this starts a new animation in the middle of the current one, or the next animation starts without 
   pressing the button: **-5** .

2. Open at a screen width of 1000px or more so that 6 animal cards are visible and the arrows are between the top 
and bottom row. We check the conditions from point 1, and remove points only for **new** errors that have appeared on 
this window width. The conditions must be met for two rows as if it were one row.
3. Open at a screen width of 640px or more so that 4 animal cards are visible and the arrows are between the top and 
bottom row. We check the conditions from point 1, and remove points only for **new** errors that have appeared on this window width.
The conditions must be met for two rows as if it were one row. We also check the accuracy of the animation: the shift 
is not by 6 cards, but by 4.


**Carousel** in a block `Testimonials`.
1. Open at a screen width of 1600px or more so that 4 reviews are visible. If the carousel is disabled and reacts to 
the movement of the slider **+20** . If the carousel does not respond - put **0** for this item and move on to the next one.
Points are deducted if:
      - When the number of intervals is from 0 to 6 (or breakpoints from 1 to 7), as well as 10 intervals 
   (or 11 breakpoints) and more: **-5** .
      - Scrolling in the opposite direction shows other (not those that were before this action, i.e. newly generated)
   reviews: **-5** . Reviews should be kept.
      - There is no animation or the animation time is 0: **-10** . The animation should be, while its appearance 
   can be arbitrary, the main thing is that when we release the slider, the animation ends on the correct feedback.
   This is the creative part of the task, because animation speed, or its acceleration when scrolling through several
   reviews at once, is not regulated. However, the presence of a non-zero animation is mandatory.
   ❗For the lack of animation on smaller screen sizes, we do **not** take points again!
2. Open at a screen width of 1000px or more so that 3 reviews are visible instead of 4. We check the conditions from point 1, 
and remove points only for **new** errors that have appeared on this window width.❗When moving from 1600px to 1000px, 
the number of intervals may increase by 1. Or it may remain in the amount of 8 values. Count on the option.


**Popup** when you click on a review in the `Testimonials`.
1. Open at a screen width of 640px or less so that the 3 shortened reviews are visible. If the popup appears in its 
entirety, put **+10** . If nothing happens by clicking the review (the review does not open) - put **0** for this item 
and proceed to the next one. Points are deducted if:
      - ❗The design of a review or a block with a review is not taken into account when evaluating. Dimensions can be as
   in the layout, or they can be arbitrary. We don't deduct points for the visual component! The only important thing is
   the presence of the recall itself, the cross and the blackout.
      - Missing outer (shaded) region or cross: **-5** . And also take into account the point below.
      - When clicking on the outer (darkened) area or cross, the popup does not close: **-5** .❗Please note that if the 
   review is shown against the background of a white cropped rectangle (as in the figma design), in which the review and 
   the cross are located, and clicking on the white box around the review does not close the popup, then we check the
   area around the white box. If, when you click on the area around the white block or the cross, the popup does not 
   close, only then we deduct points.

#### Donate
**Amount panel** in block `Pick and feed a friend`.
1. Open at a screen width of 1600px or more so that you can see the maximum Amount value of $5000. If the panel is made 
and responds to pressing the buttons on the strip, set **+30** . If the panel does not respond - put 0 for this item. 
Points are deducted if:
      - When you click on the circle on top of the amount, it should become highlighted, and the previous active circle 
   should lose highlighting.
      - The clicked circle is not highlighted: **-5** .
      - the previous active circle has not lost its highlight: **-5** .
      - The **specified** amount when clicking on the circle is not recorded in the field `Another` amount: **-5** .
      - The required field `Another` amount should be limited to 4 characters of type number. If not limited, or not 
      limited to four characters: **-5** .
      - At the start of the page display, the number _100_ should  be entered, and the corresponding element
   (3rd from the right) should be highlighted. If not: **-5** .
      - If you enter a number in the `Another` amount field that matches one of the amounts in the `Amount` bar at the 
   top, the corresponding circle should become highlighted. If not: **-5** .
      - If you enter a number in the `Another` amount field that does not match any of the amounts in the `Amount` above,
   none of the circles should be highlighted. If not: **-5** .
      - Animation may not be, this is not a mistake, we do not remove points.
2. Open at a screen width of 1000px or more so that you can see the maximum `Amount` value of $2000. We check the conditions 
from point 1, and remove points only for **new** errors that have appeared on this window width.
3. Open at a screen width of 640px or more so that you can see the maximum Amount value of $500. We check the conditions
from point 1, and remove points only for **new** errors that have appeared on this window width.

