Introduction :
TypeScript is built on top of JavaScript and provides extra features like static typing and better error checking. However, browsers and Node.js cannot directly run TypeScript code. We need to convert it into JavaScript first, and this process is called compilation. TypeScript uses a compiler called tsc to do this job.

Explanation :
When we run the tsc command, the compiler reads our TypeScript files and checks them for syntax and type errors. For example, if we assign a string to a variable that is supposed to hold a number, TypeScript can show an error.

After checking the code, the compiler converts it into JavaScript. During this process, TypeScript-specific features like type annotations and interfaces are removed because JavaScript does not need them at runtime.

Example :
let age: number = 22;
function greet(name: string): string {
return `Hello, ${name}`;
}

After compilation : (javascript)
let age = 22;
function greet(name) {
return `Hello, ${name}`;
}

Another important part is the 'tsconfig.json' file. It contains the compiler settings for our project. We can use it to choose the JavaScript version, enable strict type checking, set the output folder, and decide which files should be included or excluded.

We can generate this file using:
tsc --init

Conclusion :
In short, tsc checks our TypeScript code and converts it into JavaScript so it can run in a JavaScript environment. The tsconfig.json file helps us control how this conversion happens and keeps the project's compiler settings organized.
