# How do you import a module?
* To include modules in your programs and consume modulesModules in NodeJS is done by filenames and path. For instance 
const someModule = require('../../someModuleToBeImported')

# What JavaScript statement do you use to export a module?
* To create and export modules in NodeJS we use exports. 
exports.example = (example1) => return example1;

# Are there other ways to export a module?
> Using module.exports is another way to export modules, however, this is local for each module, not global. Exports is an alias for module.exports, this means that whatever you assign to exports is also available on module.exports, however, if you assign something directly to exports, then you loose the shortcut to module.exports. 

# What are ES6 modules and how do they differ from the module we created in this checkpoint?
>ES6 modules use import and export declarations. Babel converts the import/export of ES6 modules to CommonJS(requre and export) by default. So even using ES6 module syntax, CommonJS will be used under the hood if running code in NodeJS. 

>Require-dynamic loading where the loaded module name isn't predefined /static, or where a module can be loaded conditionally if it is truly required. Loading is synchronous, which means if you have multiple require statements they will be loaded and processed one by one.

>ES6 Imports-Named imports can be used to selectively load only the pieces needed, which can save memory. Import can be asynchronous. 

# Create a Github repository called Terminal Command and add the code from this checkpoint. Implement the touch and mkdir commands to the terminal-commands module: