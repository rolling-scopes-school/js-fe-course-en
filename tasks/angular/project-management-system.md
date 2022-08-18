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

- На приветственной странице должны отображаться общие сведения о команде, проекте, курсе.
- В верхнем правом углу должны быть доступны 2 кнопки log in и sign up.
- При наличии неистёкшего токена пользователь автоматически должен быть перенаправлен на главный роут приложения.
- При истечении срока жизни токена - пользователь автоматически должен быть перенаправлен на "Welcome page".
- Нажатие на кнопку Login / Sign up автоматически перенаправляет нас на роут с формой для Login / Sign up.

### Header

- На всех роутах доступных при наличии токена должен присутствовать sticky header ( момент, когда он становится sticky (при наличии на странице скролла) должен быть анимирован (например его цвет может потемнеть или высота слегка уменьшится)).
- В хэдере должны быть кнопки: edit profile, logout, create new board, тогглер локализации.
  Edit profile должен отправлять нас на роут с формой для edit profile. Требования к форме такие же как и ко всем формам в приложении. Должна быть кнопка удаления юзера. В случае этого действия => "confirmation modal" => пользователя должно разлогинить и пользователь должен быть удалён из базы данных.
- create new board - открывает модальное окно с формой для создания борды.
- Требования к форме такие же как и ко всем формам в приложении.

### Footer

- footer со ссылками на гитхабы авторов приложения, год создания приложения, [логотип курса](https://rs.school/images/rs_school_js.svg) со [ссылкой на курс](https://rs.school/angular/). footer отображается на всех страницах приложения.

### Login / Sign up

- Поля форм должны быть реализованы в соответствии с api backend приложения. Должна быть реализована валидация.
- Ошибки со стороны BE - (Not found, unhandled rejection, etc) должны отображаться пользователю в user-friendly формате (toast, pop-up или что-то подобное, на ваше усмотрение).
- При успешном логине пользователь должен быть перенаправлен на "Main route"

### Main route

- Отображает борды списком.
- Борды отображаются с маленьким превью из доступной информации (title). По клику на элемент переходим на board item (Board route). Также должна присутствовать кнопка для удаления борды.
- При попытке удаления борды мы должны получить confirmation modal в котором должны подтвердить серёзность наших намерений. confirmation modal должен быть универсальным компонентом (одним на всё приложение).
- глобальный поиск(опционально): поиск таска по номеру таска, названию, пользователям, которые в нём участвуют и по тексту описания задачи.

### Board route

- Должны присутствовать кнопки для создания колонки.
- Если к борде привязана хотябы одна колонка - отображаем также и кнопку создания таски.
- Для создания колонки и таска используется форма отображаемая в модальном окне.
- Требования к модальному окну и формам описаны ранее.
- Таск не может быть НЕ привязан к колонке.
- Мы можем создать несколько колонок. Мы можем создать неограниченное количество тасок. При переполнении количеством тасок колонки - скролл внутри колонки.
- Если все колонки не помещаются на экран, страница может иметь горизонтальный скролл.
- С помощью drag-n-drop мы можем менять колонки местами.
- С помощью drag-n-drop мы можем менять очерёдность тасок в рамках колонки.
- С помощью drag-n-drop мы можем менять принадлежность таски к колонке.
- ❗ Рекомендуется использовать существующую библиотеку для реализации функционала drag-n-drop ❗.
- По клику на таск открываем модальное окно с формой edit task. Требования к форме и окну как везде.
- На таске должна присутствовать кнопка delete task. При нажатии: confirmation modal -> удаление.
- Вверху колонки должен быть title. При нажатии на него он из текста должен превращаться в input, слева от которого будут кнопки cancel и submit. После ввода текста в input и нажатия submit - title колонки должен поменяться.
- На колонке должна присутствовать кнопка delete. По нажатию - confirmation modal - при апруве - удаление.
- Должна быть кнопка "вернуться" для возвращения к main route
- ВНИМАНИЕ! Удаление колонки автоматически удаляет привязанные к ней таски из BD.

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

