# TypeScript

## Task
[News API](https://newsapi.org/) - is a simple HTTP REST API for searching and retrieving news from all over the web.

## Requirements
1. Copy the code [sources](https://github.com/Pulya10c/news-JS)
2. Add [TypeScript](https://www.typescriptlang.org/) to your project
3. Configure ESLint to work with TypeScript
4. Configure Webpack to work with TypeScript
5. Migrate provided application from JavaScript to TypeScript
6. Necessary to use
    * Enum
    * Interface
    * Type
    * Generic
    * Union
    * Private, public
    * Partial, pick, readonly
    * Type any is forbidden to use
7. Adaptive layout, design is up to you


## Layout and design requirements 
* the layout of the application corresponds to the proposed one or  improved version
* the layout is adaptive. The minimum page width  is 320px, the maximum page width is 1920px
* the footer contains a link to your github, date (month, year), course [logo](https://rs.school/images/rs_school_js.svg) with [course link](https://rs.school/js-en/)

## Your task is done when
1. `Typescript` is added to your application
   * added `npm` package `Typescript`
   * created `tscongig.json` file
2. `ESLint` and `Webpack` configured to work with `Typescript`
3. `ESLint` uses the plugin [`typescript-eslint/recommended`](https://www.npmjs.com/package/@typescript-eslint/eslint-plugin)
4. Your copy of application works in Google Chrome
   * Files with `*.js` extension renamed to files with `*.ts` extension
   * Created all necessary interfaces to work with [API](https://newsapi.org/)
5. Code has strict typing
   * all variable, functions' and methods' parameters has type, as well as specified returning type
   * the interfaces are using in the code
   * enums, generics, partial and so on are created and are using in the code
6. Next flags are presented in the configuration file 
    * `"noImplicitAny": true`
    * `"strict": true`
7. The rule `no-explicit-any` is switched on
8. The layout is not breaking during the resize of the page, page elements are on the appropriate place (is not out of content)


### Scoring criteria (task is checked by mentor) max 170 points
- [ ] [Commit names according to the guideline](https://docs.rs.school/#/en/git-convention) **+10**
- [ ] The application fully migrated to Typescript **+50**
- [ ] Configured ESLint, there are no errors **+10**
- [ ] There is no 'any' **+10**
- [ ] There are flags `"noImplicitAny": true` and `"strict": true` in the configuration file **+10**
- [ ] Webpack is configured in order to typescript **+10**
- [ ] Adaptive layout **+20**
- [ ] Add own design or improvements (in the PR should be information what exactly) **+20**
- [ ] There are no significant comments related to the code **+30**

### Penalties
- [ ] There is 'any' in the code **-20**
- [ ] There is no type for some variables, parameters and so on **-20**
- [ ] There are no mandatory flags in the configuration file **-20**
- [ ] The layout is not adaptive **-20**
