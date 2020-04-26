# Ojek Belanja 🏍 [![CircleCI](https://circleci.com/gh/zainfathoni/obel.svg?style=shield&circle-token=1000aed8de1cb706801f05d5e9b1dc368bf13a46)](https://circleci.com/gh/zainfathoni/obel) [![codecov](https://codecov.io/gh/zainfathoni/obel/branch/master/graph/badge.svg?token=KBOL05Mq5P)](https://codecov.io/gh/zainfathoni/obel)

## Available Scripts

In the project's root directory, you can run:

### Installation

1. Make sure [yarn](https://yarnpkg.com) is installed in your local machine.
2. Clone this project and run `yarn` in the project's root directory.

### Development

#### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

#### `yarn storybook`

Launches [Storybook](https://storybook.js.org/) for isolated component rendering.
Try it yourself! You will be amazed!

Just run it when you want to develop your components in isolation, so you can have a full control over the props and get immediate result of the components' rendering and action calls.

### Building

#### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

#### `yarn build:storybook`

Builds the Storybook into a standalone application in the `storybook-static` folder.

#### `yarn serve`

Serves the built assets from the `yarn:build` command above.

### Testing

#### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

#### `yarn test:coverage`

Generates the tests coverage in the project.
After running it, open the `index.html` file under the `coverage/lcov-report/` folder to see the visual representation of the code coverage.

#### `yarn test:e2e:run`

Builds the app, serves it, then run Cypress for end-to-end testing with the Headless Chrome.

#### `yarn test:e2e:dev`

Start the app in development mode,then run Cypress for end-to-end testing with the Chrome Browser.
You can use it to get to certain states in the application, as a substitution for the absence of Hot Module Reloading in Create React App.

#### `yarn validate`

Runs `test:coverage` and `test:e2e:run` in parallel to validate the project's correctness in the Continuous Integration process.

### Formatting

#### `yarn format`

Manually triggers Prettier format towards all `js`, `json`, & `css` files.
By default it has to be run automatically on save in your IDE (for Visual Studio Code users, the configurations are already included in this project).

It also will be run each time before you commit (pre-commit hook).
This way, we can prevent unformatted file to be committed to the repository.

## Contributing

### Agile Methodology

We are using Kanban methodology with the Kanban Board represented by the Project Boards of this GitHub repository.
Please refer to this [Professional SCRUM Developer Glossary](https://www.scrum.org/resources/professional-scrum-developer-glossary) for any unknown terms mentioned below.

> Note: Yes, it is a **SCRUM** glossary, not a **Kanban** glossary. However, even though SCRUM and Kanban are technically different, they share similar concepts. Which is why we can use the same glossary references for both of them.

For each issue, I will define at least four of these specifications:

1. 🗣 User Story
2. 🆗 Acceptance Criteria
3. ✅ Tasks

#### 1. User Story

It's where I define the main objectives that I'm trying to achieve.
It could be as simple as clicking a button and navigate to another page, but it also could be as complex as a registration flow for the user.

#### 2. Acceptance Criteria

It contains the scenarios related to the defined **User Story** above.
It should covers all cases which are need to be covered in the tests, including the edge cases.

#### 3. Deliverables

It contains a collecttion of the tasks needed to be delivered before the work is eligible to be merged.
The possible values are:

- **Components**\
  The composable components to build the whole functionalities
  - **Logic**\
    The interaction logic of the component
  - **Styling**\
    The visual appearance of the component
  - **Utilities**\
    The generic utility functions reusable across components
- **Tests**\
  The mandatory tests to be written to increase confidence to refactor the application in the future
  - **End-to-End Tests**\
    Testing the whole app functionalities using `cypress` in the `cypress/e2e` folder
  - **Integration Tests**\
    Testing the integration of complex components using `@testing-library/react` in the `__tests__` folder
  - **Visual Tests**\
    Testing the components' visual interaction using `storybook` in the `__stories__` folder
  - **Unit Tests**\
    Test utility functions using plain JavaScript testing to cover edge cases untested with the Integration Tests

### Technical Constraints

#### Git Fundamentals

Since we are using GitHub as our main collaboration tool, it's mandatory for each of us to understand the fundamentals of Git. I need you to be familiarized with these Git operations and their fundamental concepts:

- `commit`
- `branch`
- `merge`
- `rebase`
- `reset`
- `revert`
- `clone`
- `fork`
- `bisect`

If you don't know what those Git operations mean, just ping me in the group chat so I can help you explaining them.

##### Git Learning Resources

Here are a few free resources that might be useful to help you learning Git fundamentals:

- [Git Best Practices.pptx](https://drive.google.com/open?id=1UsWALDH3aDwAXNLAYLRjk2uvCE7DbS0F)\
  A presentation slide that I used to explain some of those concepts into my subordinates in my past workplace.
- [Think Like (a) Git](http://think-like-a-git.net/)\
  A website explaining the basic concepts of Git `commit` & `branch` in a simple way.
- [Learn Version Control with Git](https://www.git-tower.com/learn/git/ebook)\
  A comprehensive Git tutorial by [Git Tower](https://www.git-tower.com), a paid Git client.
  Also available in the [video format](https://www.git-tower.com/learn/git/videos).
- [GitHub Learning Lab](https://lab.github.com/)\
  An interactive tutorial by GitHub for learning basic Git operations, including `fork`.
- [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)
  A comprehensive Git tutorial by [Atlassian](https://www.atlassian.com).
  Its [Collaborating](https://www.atlassian.com/git/tutorials) section is pretty useful to help us understand the complexity (or the simplicity 😁) of collaboration through Git.

#### Git Commits Signing

Since I have never met most of the collaborators prior to this project initiation, I want to make sure that all of them are [accountable of the codes they contributed](https://nvisium.com/blog/2017/06/21/securing-github-commits-with-gpg-signing.html). By getting invited to collaborate this repository, you should have been able to do [Git Commits Signing].

Therefore, I decide that it is mandatory for the Pull Requests to be merged to only contains commits with verified signatures.
If you accidentally committed an unsigned commit, you can try to [rewrite the Git commit history](https://www.atlassian.com/git/tutorials/rewriting-history).
Just reach out to me, I will be glad to help you if you get that kind of problem.

#### Forking

It's completely fine to [fork this repository](https://help.github.com/articles/fork-a-repo/) so you could play around with your own pace, as long as you don't use it directly for a project in production, but make sure that you know what you're doing, because it means that you have to make sure that your fork repository is [properly synchronized](https://help.github.com/articles/syncing-a-fork/) to my upstream repository.

To verify that you set up your local machine correctly with your fork repository and my upstream repository, just run the `git remote -v` command and you should see something like this.

```bash
$ git remote -v
origin    https://github.com/YOUR_USERNAME/obel.git (fetch)
origin    https://github.com/YOUR_USERNAME/obel.git (push)
upstream  https://github.com/zainfathoni/obel.git (fetch)
upstream  https://github.com/zainfathoni/obel.git (push)
```

#### Creating Pull Requests

If you create a Pull Request directly from your fork's branch, it will be too tedious for me to clone all your fork repositories just to contribute to the Pull Requests.
While I think it's still simple enough for you to add another Git remote repository (which is this repository) as an upstream repository. So I recommend you to push that branch into a branch in this repository and try to create another Pull Request from the branch in this repository instead.

It's probably not common in most open source projects in GitHub, where you could just create Pull Requests from your own fork repository branches.
Honestly, I do it all the time.
But I think it's necessary for this project to have this kind of convention, because in this project I don't expect you to work on the issues by yourself, I am trying to assist you in doing your work, while in those open source projects you're expected to work on your stuffs by yourself independently.

#### Branch Naming Convention

I would like to have all branches in this repository except `master` and `dev` (if any) to be namespaced properly by adding prefixes separated by `/` in the branch name.

Inspired by some of [existing Git Workflows out there](https://www.atlassian.com/git/tutorials/comparing-workflows), I decided to have this convention:

| Branch Template                   | Example                     | Purpose                                            |
| --------------------------------- | --------------------------- | -------------------------------------------------- |
| `feature/[issue-id]-[issue-slug]` | `feature/14-top-navigation` | For new development tasks related to an issue      |
| `bugfix/[issue-id]-[bug-slug]`    | `bugfix/10-nav-link`        | For bug fixes related to an issue                  |
| `chore/[issue-id]-[chore-slug]`   | `chore/180-update-readme`   | For supporting system setup                        |
| `personal/[username]`             | `personal/ri7nz`            | For all your initiatives, undocumented tasks, etc. |

## License

See the [LICENSE](LICENSE) file for license rights and limitations (MIT).
