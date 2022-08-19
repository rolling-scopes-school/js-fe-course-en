#  Project Management System

**Project management system** is an application that helps you achieve goals, either individually or as a part of a team.

## Notes

There are many competitors on the market for our future application. Although this is not scary, we decided to research
them before making our own. The marketing department figured out the main competitors: *Trello, Jira, Redmine, Bitrix24, 
Yandex Tracker, Asana, GanttPro, Github projects.*

## Application prototype

Pay attention, we leave the final set of tools and design up to you to not limit your possibilities and imagination.

Design, prototype, as well as the implementation of the application itself to your own taste.

## Backend

Use https://github.com/vitaly-sazonov/kanban-rest as a backend.
There is the description of the steps to get started, as well as a list of available requests in the repository.

- You will need to deploy the backend yourself to demonstrate the working application.
- During the implementation of an application, you may run the backend in any environment that is convenient for you, for example, a local machine.

## Application structure

Regardless of the application type, it should contain:

- welcome page
- user login
- projects management page
- project management page
- additional functionality (for example, the ability to view all the tasks of the selected user)

## Repository requirements

- use private school repository for this task
- branch name is **project-management-app**
- the commit history should reflect the development process of the application. [Commit requirements](https://docs.rs.school/#/git-convention)
- the demo version of the application is hosted on `gh-pages`, `netlify`, `heroku` or other similar hosting.
- after completing the task, create a pull request **Merging a Pull Request is not required**
- add a link to the backend folder to the description of the pull request if the backend has not been deployed.

## Technical requirements

- localization (at least 2 languages). The application should be able to change the language by clicking on the slider in the header
- semantic layout
- the application should work in the latest version of the Google Chrome browser
- forms should contain validation for compliance with the expected type (email, password, etc.)
- you may use css frameworks, any component libraries, html and css preprocessors
- it is necessary to use the backend for the correct operation of the application and the interaction between several users
- ❗ it is forbidden to copy the code of other students, demos, examples that are given in the assignment. This ban applies to html, css, js code. You can use small code snippets from Stack Overflow, other self-found sources on the Internet, with the exception of github repositories of course students.

## Application design requirements

- you are not limited in creativity, but limited by the user's capabilities
- the application quality is characterized by elaboration of details, attention to typography (no more than three fonts per page, font size of at least 14 px, optimal [font and background contrast] (https://snook.ca/technical/colour_contrast/colour.html)) , carefully selected content
- adaptive layout. The minimum page width of the application is 320px
- interactivity of elements users can interact with, changing the appearance of the element itself and the type of the cursor on hover, using different styles for the active and inactive state of the element, smooth animations
- the unity of styles of all pages of the application - the same fonts, button styles, indents, the same elements on all pages of the application have the same appearance and layout. Item colors and background images may vary. In this case, colors should be from the same palette, and background images from the same collection.

## Description of function blocks
The user (team member) can set tasks, perform tasks, view tasks, delete their own tasks, be responsible (assigned) in other people's tasks.

### Welcome page(route)

- The welcome page should display general information about the developer, project, course.
- In the upper right corner should be present 2 buttons Log in and Sign up
- If there is an unexpired token, the user should be redirected to the main route of the application automatically.
- When the token expires - the user should be redirected to the "Welcome page" automatically.
- Pressing the Log in / Sign up button redirects the user to the route with the Login / Sign up form automatically.

### Header
- All routes available with a token should have a sticky header (the moment when it becomes sticky (if there is a scroll on the page) should be animated (for example, its color become darken or its height will slightly decrease)).
- There are buttons in the header: edit profile, logout, create new board, localization switcher.
- Edit profile should redirect user to a route with a form for edit profile. The requirements for the form are the same as for all forms in the application. There should be a 'Delete User' button. In case of this action should be shown a  "confirmation modal" than the user should be logged out, and the user should be removed from the database.
- Create new board - opens a modal window with a form for creating a board. Requirements for the form are the same as for all forms in the application.

### Footer

- footer should contain link to the author's  github, the year the application was created, [course logo](https://rs.school/images/rs_school_js.svg) with [link to the course](https://rs.school/angular/).
- footer is displayed on all pages of the application.
- 
### Login / Sign up

- Form fields should be implemented in consistency with the API backend of the application. Validation should be implemented.
- Errors from the BE side - (Not found, unhandled rejection, etc) should be displayed in a user-friendly format (toast, pop-up or something like this - up to your decision).
- Upon successful login, the user should be redirected to the "Main route"

### Main route

- Displays the boards with lists.
- Boards are displayed with a small preview of the available information (title). By clicking on the element, the user redirects to the board item (Board route). There should be a button to remove the board.
- When a user trying to delete the board, he/she should receive a confirmation modal to verify the user really wants to delete the board (to avoid deleting the board by mistake). The confirmation modal should be a generic component (one for the application).
- global search (optional): search for a task by task number, name, users assigned to it and by the text of the task description.

### Board route

- There should be button to create a column.
- If there is at least one column in the board, you should display the task creation button.
- To create a column and a task, you should display a form in the modal window.
- Requirements for the modal window and forms are described before.
- A task cannot be NOT bound to a column.
- The user can create multiple columns. The user can create an unlimited number of tasks. When overflowing with the number of tasks of the column - display scroll inside the column.
- If all columns do not fit on the screen, the page may have a horizontal scroll.
- The user can swap columns using drag-n-drop.
- The user can change the order of tasks columns using drag-n-drop.
- The user change the belonging of the task to the column using drag-n-drop.
- ❗ It is recommended to use the existing library to implement the drag-n-drop functionality ❗.
- By clicking on the task, you should open a modal window with the edit task form. The requirements for the form and window are the same as everywhere.
- There should be a 'delete task' button on the task. By clicking on 'delete task' should be open the confirmation modal, only after user confirm the deleting - delete the task.
- At the top of the column should be displayed the title. When you click on it, it should convert text into input, there should be 'cancel' and 'submit' buttons to the left of input. After entering text in the input and clicking submit - the title of the column should be updated with entered text.
- The column should have a 'delete column' button. By clicking on 'delete column' should be open the confirmation modal, only after user confirm the deleting - delete the column.
- ATTENTION! Deleting a column removes the tasks associated with it from the BD automatically.
- There should be a "back" button to return to the main route

## Критерии оценивания

**Максимальный балл за задание 780** (CHECK!!!!!)

## Check criteria

Для удобства проверки необходимо записать и разместить на YouTube небольшое (5-7 мин) видео для проверяющих с объяснением, как реализован каждый из перечисленных в критериях оценки пункт. Ссылку на видео добавить в pull-request.

### Welcome route - max 70 баллов

- [ ] На приветственной странице должны отображаться общие сведения о команде, проекте, курсе. **10 баллов**
- [ ] В верхнем правом углу должны быть доступны 2 кнопки log in и sign up. **10 баллов**
- [ ] При наличии неистёкшего токена пользователь автоматически должен быть перенаправлен на главный роут приложения. **20 баллов**
- [ ] При истечении срока жизни токена - пользователь автоматически должен быть перенаправлен на "Welcome page". **20 баллов**
- [ ] Нажатие на кнопку Login / Sign up автоматически перенаправляет нас на роут с формой для Login / Sign up. **10 баллов**

### Login / Sign up  - max 80 баллов

- [ ] Логин/log out есть на всех страницах **20 баллов**
- [ ] Поля форм должны быть реализованы в соответствии с api backend приложения. Должна быть реализована валидация. **50 баллов**
- [ ] При успешном логине пользователь должен быть перенаправлен на "Main route" **10 баллов**

### Main route max 100 баллов

- [ ] Функционал создания борды **20 баллов**
- [ ] Отображает борды списком. **10 баллов**
- [ ] Борды отображаются с маленьким превью из доступной информации (title, description, etc). По клику на элемент переходим на board item (Board route). Также должна присутствовать кнопка для удаления борды.  **10 баллов**
- [ ] При попытке удаления борды мы должны получить confirmation modal в котором должны подтвердить серёзность наших намерений. confirmation modal должен быть универсальным компонентом (одним на всё приложение).  **10 баллов**
- [ ] глобальный поиск: поиск таска по номеру таска, названию, пользователям, которые в нём участвуют и по тексту описания задачи.  **20 баллов**
- [ ] Реализован функционал редактирования профиля пользователя.  **30 баллов**

### Board route  max 260 баллов

- [ ] Должны присутствовать кнопки для создания колонки.   **10 баллов**
- [ ] Если к борде привязана хотябы одна колонка - отображаем также и кнопку создания таски.   **10 баллов**
- [ ] Для создания колонки и таска используется форма отображаемая в модальном окне.   **30 баллов**
- [ ] При переполнении количеством тасок колонки - скролл внутри колонки. **20 баллов**
- [ ] Страница на данном роуте не должна иметь скролла.  **10 баллов**
- [ ] С помощью drag-n-drop мы можем менять колонки местами.  **30 баллов**
- [ ] С помощью drag-n-drop мы можем менять очерёдность тасок в рамках колонки.  **30 баллов**
- [ ] С помощью drag-n-drop мы можем менять принадлежность таски к колонке.  **50 баллов**
- [ ] по клику на таск открываем модальное окно с формой edit task. Требования к форме и окну как везде.  **30 баллов**
- [ ] на таске должна присутствовать кнопка delete task. При нажатии: confirmation modal -> удаление.  **10 баллов**
- [ ] вверху колонки должен быть title. При нажатии на него он из текста должен превращаться в input, слева от которого будут кнопки cancel и submit. После ввода текста в input и нажатия submit - title колонки должен поменяться.   **20 баллов**
- [ ] на колонке должна присутствовать кнопка delete. По нажатию - confirmation modal - при апруве - удаление. **10 баллов**

### Общие требования max 90 баллов

- [ ] Ошибки со стороны BE - (Not found, unhandled rejection, etc) должны отображаться пользователю в user-friendly формате (toast, pop-up или что-то подобное, на ваше усмотрение). **50 баллов**
- [ ] Локализация **20 баллов**
- [ ] Backend задеплоен **10 баллов**
- [ ] sticky-Header  **10 баллов**

### Дополнительный функционал 30 баллов

- [ ] Реализован дополнительный функционал, не предусмотренный текущими требованиями **30 баллов**

### Штрафы

- [ ] Присутствие ошибок и ворнингов в консоли  **- 20 балла**
- [ ] Наличие в консоли результатов выполнения console.log - **- 20 балла**
- [ ] коммиты после дедлайна **- 100 баллов**

