# What is a Node module?
>Node modules can be thought of as JavaScript libraries or a certain part of the overall codebase. For example, a collection of functions which you want to keep together and also seperate from the rest of your codebase. This is the idea of seperation of concerns and also having a module be responsible for one and only one thing/part of the application. Modules can then be combined to create coherent and complete applications. Node has built in modules as well as external modules that are on the npm community, and ones that can be created as well. 


# What is the main difference between exports and module.exports?
* exports-is a convenience variable so module authors can write less code. Exports in not returned by require(), module.exports is. Exports will not export an object that is not (named/defined in an instance of).

* module.exports-the object reference that gets returned from the require() call. Empty by default and can be defined by a reference to a JavaScript object.

# Why is using exports recommended?
>Using exports is recommended because it is a reference to module.exports and does not reassign the object module.exports. When working with a mix of primitives and not just a specific object type, it is recommended to use exports. If working with a specific object type, module.exports is in ideal usage.
