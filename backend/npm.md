**NPM (Node Package Manager)**

----
- npm init
- npm whoami
    - npm adduser
- You can tell npm about your project in  a file called package.json
    - npm init --scope=<'username'>
- The first thing that most people do with npm is install a dependency. Dependencies are fetched from the registry, and unpacked in the 'node_modules' folder.
    - To install a module, use the `npm install <modulename>` command
- npm isn't just for installing stuff. It also shows you what you have installed (your dependencies)
    - ` npm ls `
- _npm test_
    - npm can be used as a task runner with its "scripts" property. Almost every module and project will have a test script that runs to make sure everything is good. 
        - First, create a file called `test.js`. (This would be where I'd write my tests, this is npm class, not testong class). **The test has to exit without throwing an error, or  else the test fails.**
        - Then, edit your `package.json` file to make your scripts section look like this instead: 
        ```
        "scripts": {
            "test": "node test.js"
        },
        ```
- Package Niceties (make sure to have a readme, github repo link and some sort of description)
- Publish
    - Packages get into the registry by using the `npm publish` command
- `npm dist-tag add <pkg>@<version> [<tag>]`

- **Outdated**

    - What do we do when someone else updates their package?
        - The first step is to detect this. We can detect compatible releases programmtically with the `npm outdated` command

**Update**
- It's fine to explicitly check for outdated modules, and then run `npm install` to pull them in
    - However, if you want ot be a bit more lazy about it, there's a special npm command that will update all of your deps to the max version you allow in your package.json
    - That command is: `npm update`

**Rm**
- ` npm ls `: will print to stdout all the versions of packages that are installed, as well as their dependencies, in a tree-structure
    - `npm rm @linclark/pkg`

**finale**









