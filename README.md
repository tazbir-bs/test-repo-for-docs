# Taxi Hailing Service

Welcome to our Taxi Hailing Service GitHub repository! This repository contains the source code for our innovative taxi hailing application. Below, you'll find essential information to help you understand, contribute to, and deploy the project.

## Code Review Checklist

Before submitting a pull request, please make sure to go through the following checklist:

1. **Code Quality**: Ensure that your code adheres to our coding standards and best practices.
2. **Documentation**: Update or create documentation for any new features, APIs, or changes to existing functionality.
3. **Unit Tests**: Write unit tests for your code and ensure that existing tests pass.
4. **Code Structure**: Verify that your code is well-organized and follows the project's directory structure.
5. **Security**: Check for security vulnerabilities and follow secure coding practices.
6. **Comments**: Include meaningful comments in your code to enhance readability.
7. **Compatibility**: Ensure your changes do not break existing functionality and are compatible with the current codebase.
8. **Pull Request Description**: Provide a clear and concise description of your changes in the pull request.

## How to Run the Project Locally

To run the Taxi Hailing Service locally, follow these steps:

### Prerequisites

- Node.js installed
- npm or yarn package manager installed
- MongoDB installed and running

### Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/taxi-hailing-service.git
   cd taxi-hailing-service
   ```

2. **Install Dependencies**:
   ```bash
   npm install  # or yarn install
   ```

3. **Configure Environment Variables**:
   Create a `.env` file based on the provided `.env.example` and fill in the necessary values.

4. **Start the MongoDB Server**:
   Ensure your MongoDB server is running.

5. **Run the Application**:
   ```bash
   npm start  # or yarn start
   ```

6. **Access the Application**:
   Open your browser and navigate to `http://localhost:3000` (or the specified port in your `.env` file).

## High-Level Feature List

Our Taxi Hailing Service includes the following key features:

- User Registration and Authentication
- Real-time Taxi Booking
- Driver Tracking and Availability
- Fare Estimation
- Payment Integration
- User Ratings and Reviews

For a detailed list of features and functionalities, please refer to our [feature documentation](docs/features.md).

## Live Architectural Diagram

View our live architectural diagram [here](https://your-diagram-link.com).

## Deployment Guide

To deploy the Taxi Hailing Service in a production environment, follow these deployment steps:

1. **Set Up a Database**: Configure and connect the application to a production-ready database.

2. **Update Environment Variables**: Update the environment variables in the production environment.

3. **Build and Deploy**:
   ```bash
   npm run build
   # Deploy the built files to your hosting platform
   ```

4. **Ensure Security Measures**: Implement security best practices, such as HTTPS, firewalls, and secure configurations.

5. **Monitor and Scale**: Set up monitoring tools and scale the application as needed based on usage.

For detailed deployment instructions, refer to our [deployment guide](docs/deployment.md).


<a name="code-style"></a>
## Some code style guidelines

- Use stage-2 and higher JavaScript (modern) syntax for new projects. For old project stay consistent with existing syntax unless you intend to modernise the project.

  _Why:_

  > This is all up to you. We use transpilers to use advantages of new syntax. stage-2 is more likely to eventually become part of the spec with only minor revisions.

- Include code style check in your build process.

  _Why:_

  > Breaking your build is one way of enforcing code style to your code. It prevents you from taking it less seriously. Do it for both client and server-side code. [read more...](https://www.robinwieruch.de/react-eslint-webpack-babel/)

- Use [ESLint - Pluggable JavaScript linter](http://eslint.org/) to enforce code style.

  _Why:_

  > We simply prefer `eslint`, you don't have to. It has more rules supported, the ability to configure the rules, and ability to add custom rules.

- We use [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript) for JavaScript, [Read more](https://www.gitbook.com/book/duk/airbnb-javascript-guidelines/details). Use the javascript style guide required by the project or your team.

- We use [Flow type style check rules for ESLint](https://github.com/gajus/eslint-plugin-flowtype) when using [FlowType](https://flow.org/).

  _Why:_

  > Flow introduces few syntaxes that also need to follow certain code style and be checked.

- Use `.eslintignore` to exclude files or folders from code style checks.

  _Why:_

  > You don't have to pollute your code with `eslint-disable` comments whenever you need to exclude a couple of files from style checking.

- Remove any of your `eslint` disable comments before making a Pull Request.

  _Why:_

  > It's normal to disable style check while working on a code block to focus more on the logic. Just remember to remove those `eslint-disable` comments and follow the rules.

- Depending on the size of the task use `//TODO:` comments or open a ticket.

  _Why:_

  > So then you can remind yourself and others about a small task (like refactoring a function or updating a comment). For larger tasks use `//TODO(#3456)` which is enforced by a lint rule and the number is an open ticket.

- Always comment and keep them relevant as code changes. Remove commented blocks of code.

  _Why:_

  > Your code should be as readable as possible, you should get rid of anything distracting. If you refactored a function, don't just comment out the old one, remove it.

- Avoid irrelevant or funny comments, logs or naming.

  _Why:_

  > While your build process may(should) get rid of them, sometimes your source code may get handed over to another company/client and they may not share the same banter.

- Make your names search-able with meaningful distinctions avoid shortened names. For functions use long, descriptive names. A function name should be a verb or a verb phrase, and it needs to communicate its intention.

  _Why:_

  > It makes it more natural to read the source code.

- Organize your functions in a file according to the step-down rule. Higher level functions should be on top and lower levels below.

  _Why:_

  > It makes it more natural to read the source code.

<a name="enforcing-code-style-standards"></a>

### Enforcing code style standards

- Use a [.editorconfig](http://editorconfig.org/) file which helps developers define and maintain consistent coding styles between different editors and IDEs on the project.

  _Why:_

  > The EditorConfig project consists of a file format for defining coding styles and a collection of text editor plugins that enable editors to read the file format and adhere to defined styles. EditorConfig files are easily readable and they work nicely with version control systems.

- Have your editor notify you about code style errors. Use [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier) and [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier) with your existing ESLint configuration. [read more...](https://github.com/prettier/eslint-config-prettier#installation)

- Consider using Git hooks.

  _Why:_

  > Git hooks greatly increase a developer's productivity. Make changes, commit and push to staging or production environments without the fear of breaking builds. [read more...](http://githooks.com/)

- Use Prettier with a precommit hook.

  _Why:_

  > While `prettier` itself can be very powerful, it's not very productive to run it simply as an npm task alone each time to format code. This is where `lint-staged` (and `husky`) come into play. Read more on configuring `lint-staged` [here](https://github.com/okonet/lint-staged#configuration) and on configuring `husky` [here](https://github.com/typicode/husky).

<a name="logging"></a>

## Logging


- Avoid client-side console logs in production

  _Why:_

  > Even though your build process can (should) get rid of them, make sure that your code style checker warns you about leftover console logs.

- Produce readable production logging. Ideally use logging libraries to be used in production mode (such as [winston](https://github.com/winstonjs/winston) or
  [node-bunyan](https://github.com/trentm/node-bunyan)).

      _Why:_
      > It makes your troubleshooting less unpleasant with colorization, timestamps, log to a file in addition to the console or even logging to a file that rotates daily. [read more...](https://blog.risingstack.com/node-js-logging-tutorial/)

<a name="api"></a>

Thank you for your interest in our Taxi Hailing Service! If you have any questions or encounter any issues, please don't hesitate to open an issue or reach out to our support team. Happy coding!
