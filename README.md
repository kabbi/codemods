# Codemods

An atom plugin to run js codemods on your selections, files, folders and whole projects. Uses `jscodeshift` runner and API.

![A little demo](https://cloud.githubusercontent.com/assets/1160550/16445466/76ca5396-3deb-11e6-95ba-07fd5300e505.gif)

**WARNING:**
Don't run transforms on the code when you can't revert it (using git, manual backups or anything else). Transform runner we use makes no backups and modifies the files in place (when applied to file or folder level, selection transforms are safer), and can potentially destroy large codebases. This mostly concerns codemods in general, not the atom plugin.

**TIP:**
Install `nuclide` package to get the cute console windows with `jscodeshift` output within atom, and a ton of other IDE-like functionality that nuclide provides.

Features:
- runs your own transforms on js code
- fetches transform files from `/transforms` folder in your project
- can run transforms on your files and selections
- displays jscodeshift output in nuclide console window

Roadmap:
- load transforms from `node_modules` folder (i. e. provide support to some transform packs that are distributed as npm packages, like [js-codemod](https://github.com/cpojer/js-codemod) or [react-codemod](https://github.com/reactjs/react-codemod))
- configure default transform search path
- better worker process lifecycle management
- run transforms on specific folder or whole project
- reduce installation time

Credits:
- [jscodeshift](https://github.com/facebook/jscodeshift) - codemod runner and API wrapper
