
# Q: 1 Understanding Project Management in NodeJS

## Explain the following topics in your own words with clear headings and simple examples wherever applicable:

## a. Package Managers

### What is a package manager?
A package manager is a tool that helps developers install, update, and manage external libraries or modules in a project.
For example: Instead of manually downloading a library like express, you can run:
```
npm install express
```
and it’s automatically added to your project.


### Why do we need package managers in backend development?
We need package managers in backend development because:
* They save time by automating installation of libraries.
* Ensure consistency across environments (development, testing, production).
* Handle versioning so you can use the correct library version.


### Problems faced if package managers are not used
* Manual downloading of libraries → time-consuming.
* Difficult to track versions → may cause compatibility issues.
* Sharing projects becomes hard → teammates won’t know which libraries to install.


## b. NPM (Node Package Manager)

### What is NPM?
NPM is the default package manager for Node.js. It comes bundled when you install Node.js.


### Why is NPM important for Node.js applications?
NPM is important for Node.js applications because:
* Provides access to thousands of open-source libraries.
* Makes dependency management easier.
* Helps in project initialization and automation (scripts).


### How NPM helps in managing dependencies
When you install a library, NPM records it in .
For example:
```
npm install mongoose
```
this adds `mongoose` under `"dependencies"` in `package.json`.

NPM ensures the same versions are installed when someone else runs:
```
npm install
```


## c. Backend Project Initialization

### What is the command used to initialize a backend (Node.js) project?
The command used to initialize a backend (Node.js) project is:
```
npm init
```


### Explain what npm init and npm init -y do
`npm init` starts an interactive setup asking details like project name, version, description, entry point, etc.
`npm init -y` skips questions and creates a  file with default values.


## d. Files and Folders Created After Project Initialization

### Explain the purpose and importance of:
### package.json
### node_modules
### package-lock.json

**1. `package.json`**
* Purpose: Stores metadata about the project (name, version, author, dependencies, scripts).
* Importance: Acts as the "blueprint" of the project.
Example snippet:
```
{
  "name": "my-app",
  "version": "1.0.0",
  "dependencies": {
    "express": "^4.18.2"
  }
}
```

2. **`node_modules`**
• 	Purpose: Contains all installed libraries and their dependencies.
• 	Importance: Without it, your project won’t run.
• 	Example: Installing `express` creates a `node_modules/express`folder .

3. **`package-lock.json`**
• 	Purpose: Locks the exact versions of installed packages.
• 	Importance: Ensures consistency across different environments.
• 	Example: If `express` is installed as `4.18.2`, the lock file ensures everyone gets the same version.

#### Also mention:
### Which files/folders should not be pushed to GitHub and why
* `node_modules`
It's huge in size and can be regenerated using `npm install`.
* Reason: Avoids unnecessary clutter and reduces repository size.

### Which files must be committed and why
* `package.json` 
It defines dependencies and project info.
* `package-lock.json`
It ensures exact versions are installed.
* Source code files (`.js`, `.ts`, etc.) → Actual logic of your project.