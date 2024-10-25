# Christmas Shop

## Project's Description

Christmas holidays are just around the corner! It's time to shop for gifts... but where?  
Christmas Shop is a project where you will need to create a website consisting of two pages, make it responsive, and add interactivity.  
It's time to create a cozy place for buying interesting gifts!

## Key skills

- Valid semantic responsive web design;
- Easy-to-maintain readable code;
- Exporting styles and graphics from Figma;
- Using JavaScript to implement the functionality specified in the task.

## Project Work Stages

The task consists of three parts:

- [Christmas Shop. Part-1: Fixed Layout](christmas-shop-part1.md)
  - In this part of the task, you need to create the 'Home' and 'Gifts' pages based on the layout, which should display correctly when the window width is at least 1440px;
  - The validity of the work is checked, as well as its compliance with the layout.
- [Christmas Shop. Part-2: Responsive Design](christmas-shop-part2.md)
  - In this part of the task, it is necessary to add responsiveness to the pages created in the first stage, up to and including a width of 380px;
  - The validity of the work is checked, its alignment with the layout at the corresponding page width, layout responsiveness, and the absence of horizontal scroll bars.
- [Christmas Shop. Part-3: Adding Functionality](christmas-shop-part3.md)
  - In this part of the task, we use JavaScript to add interactivity to the pages;
  - The implemented functionality is being checked.

The duration of each part of the task is 1 week.  
The form of evaluation for each part of the task is a cross-check review.

[Design in Figma](https://www.figma.com/design/zTB01BwWZVoXYK5atH3eZT/Cristmas-Shop)  
[Graphic materials](img-compressed.zip)

## Creating your own copy of the layout

Start the task by creating your own copy of the layout. To do this:

- Log in to [Figma](https://www.figma.com/);
- Open the layout;
- On the left panel, click on the arrow next to the layout name, and select the option "Duplicate to your drafts";
- At the top left, open the settings, and choose "Back to files";
- Open the copy of the layout with the label "Drafts".

## Code quality recommendations

Recommendations are provided for reference; strict adherence to them is not expected and will not be checked.

- Code quality guide
  - [General principles](../code-principles/generic-principles.md)
  - [HTML and CSS recommendations - beginner level](../code-principles/html-and-css.md)
  - [HTML and CSS recommendations - advanced level](../code-principles/html-and-css-extended.md)

## Technical requirements

1. The layout is valid, semantic, and matches the design.
2. The application is displayed correctly and functions properly in the latest version of Google Chrome.
3. Using HTML preprocessors and template engines (e.g. `Pug`) **is not allowed**.
4. Using CSS frameworks (e.g., `Bootstrap`) **is not allowed**.
5. Using JS frameworks (e.g., `Angular`, `React`, `Vue`, etc.) **is not allowed**.
6. Using outdated libraries (e.g. `JQuery`, etc.) or pre-built libraries (e.g. `Swiper`, etc) to implement functionality **is not allowed**.
7. Using `TypeScript` **is not allowed**.
8. Using CSS preprocessors (`SASS`, `SCSS`), [modern-normalize](https://github.com/sindresorhus/modern-normalize) is allowed.
9. Using a style reset with `reset.css` is not recommended.
10. Adding layout as an image by taking a screenshot of a part of the layout and pasting it into the markup is not allowed. Please use tags and characters for layout, and use images only for adding pictures and icons, not for layout elements (buttons, blocks, sections).
11. The code must be readable, without minification or obfuscation. You are allowed to use bundlers, such as [Vite](https://vitejs.dev/) or [Webpack](https://webpack.js.org/), but please enable [source maps](https://web.dev/articles/source-maps). Gulp is unmaintained and should not be used.

## Repository Requirements

- Task should be done in private school's repository. 
- Create new branch `christmas-shop` from `main`. Create a folder `christmas-shop` in the created branch. Place your code in this folder.
- The `main` branch should be empty (contain only files like README.md, .gitignore or .github folder)
- Use `gh-pages` for deployment 
- Since the task is divided into three parts, christmas-shop will have three versions:
  1.  The `christmas-shop` branch will contain the first part of the assignment. When starting the second part, create a branch `christmas-shop-part2` from the `christmas-shop` branch to continue from where you left off in the first part
  2.  Upon completing the second part of the assignment, create a Pull Request from the `christmas-shop-part2` branch to the `christmas-shop` branch, check for conflicts, and perform the Merge
  3.  For the third part, repeat the first 2 steps with a different branch name (`christmas-shop-part3`)
  4.  Please note: Pull Requests with subsequent merges are only done from the current development branch into the initial branch of this task. Merging into the `main` branch is not performed!
- The internal structure of the project is at your discretion. The simplest option is separate pages, each with its own styles and js. When submitting the work, please ensure that the provided submission link opens the main page of the deployed project

## Commit Requirements

- Commit history should reflect the application development process.
- [Give commit names according to the guideline](https://docs.rs.school/#/en/git-convention)

## Requirements for Pull Requests

- Name the Pull Request according to the task title
- [Provide the Pull Request description following the template](https://docs.rs.school/#/en/pull-request-review-process?id=pull-request-requirements-pr)  
  **No need to merge the Pull Request from the development branch into the `main` branch**.

## How to submit

After receiving the task but before the deadline, please go to the RS App at https://app.rs.school/. Select **Cross-Check: Submit**, choose the relevant task from the dropdown menu, and add the link to the deployed version of your created website in the **Solution URL** field. Then, click **Submit** button.

## Submit Recommendations

- It is recommended to submit the task as early as possible, as soon as the option becomes available in the rs app. After submission, you can continue working on the task until the deadline
- Since the project is being done in a private repository, there is no point in submitting a link to the repository or a pull request - the reviewer won't be able to see it. The private school repository is only visible to you, course admins, and your mentors when they become available
- Make sure that the deployed link you provide opens in incognito mode of the browser

## Task Evaluation

- Each part of the assignment is assessed through a cross-check
- Instructions for conducting a cross-check: https://docs.rs.school/#/en/cross-check-flow?id=cross-check

