---
aliases:
  - WEB Modern Javascript, modules
Lec: 
tags: 
Subject: Javascript
related: "[WEB Modern Javascript, modules](.md)"
---

# Modern Javascript Modules

## How we develop modern javascript applications

1. First we write our code as modules or pieces.
2. Then we use ==bundlers== to collect our modules into one file
3. Then ==Transpile , polyfilling== our code to work on all browsers
4. Then It goes to Production

## Modules

### What are modules?

- Small building blocks that when put together build complex applications
- Reusable piece of code that encapsulate implementation details
- can be a standalone file

### What are dependencies?

- modules that we import into our code, so that our code is ==dependent on them==

### Why use modules?

1. abstract code
2. isolate each componenet
3. organized code
4. make code more reusable

### What are the differences between ES6 moduls, and regular script file

| ==ES6 modules==                    | ==Regular Scripts==               |
| ---------------------------------- | --------------------------------- |
| variables scoped to module         | global variables                  |
| files load asynchronously          | synchronously unless defer, async |
| strict mode always                 | sloppy mode                       |
| always hoisted                     | not hoisted                       |
| Top-Level this refers to undefined | top level this refers to window   |
| allows imports and exports         | Doesn't allow                     |

### How ES6 modules are imported?

==First,== We [Parse](app://obsidian.md/+Parsing) all modules, Happens in [synchronous](app://obsidian.md/Synchronous%20vs%20Asynchronous) way

#### Why synchronous?

1. So that we can hoist it
2. this way we know imports before execution
3. So that Bundlers can delete all pieces of code that are not used during execution.  
   ==Then,== We Download the code of imports asynchronously  
   ==After That==, We link our imports to exports of downloaded modules.  
   ==Then==, We Execute our modules

Now it is ready to execute our main file  
![How ES6 Modules are imported.png](app://f682576da403249c8bbc4c1fdf6f787d93af/mnt/Media/D/Learning/5.zettelkasten%20Notes/z9.Attachments/How%20ES6%20Modules%20are%20imported.png?1697106444211)

