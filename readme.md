
### Lessons, information, advice, etc...

## Global vs. Local dependencies 

"I recommend against using global packages ever, and definitely not for TypeScript in a TypeScript project. I recommend installing it as a local dev dependency in each project.
There are two reasons for this:
1. Turn key solution.  User should be able to npm install and get everything they need without additional steps.
2. Versioning.  If your project works with TypeScript 1.x it may not work with 2.x, or it may work 3.3 but not 3.5, etc.  If the user just does npm install typescript they'll get latest, and if you require a specific version of TypeScript it may conflict with whatever version they already had installed globally.
While the TypeScript folder is ~50MB on disk, NPM does local caching so for many users that isn't 50MB bytes on the wire, it is just a local disk copy in many cases.  As a dev dependency, it shouldn't make it into any production bundles/builds.  Overall, I think it is a bad idea to try to save 50MB on disk in exchange for versioning hell for developers." - @Micah


## Debugging React

A great example from Retsam that demonstrates the problem of declaring a function inside an App. Generating undesired closures when singular pieces of state are desired. https://codesandbox.io/s/damp-darkness-5879w
