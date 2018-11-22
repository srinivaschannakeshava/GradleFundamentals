# <img src="https://projects.eclipse.org/sites/default/files/Logo-200-200.png" alt="drawing" width="40"/> Gradle Fundamentals 
<hr>

- Build by conventions
- Groovy DSL 
- Supports dependencies - maven and ivy
- Suports multi project builds
- Customizable
- Maintainable

### Why Gradle ? Why not ANT or Maven?
- ANT 
    - Hard to read
    - lack of conventions(Everything needs to be defined)
    - Very Large and non maintainable
- Maven
    - Written in XML 
    - Becomes very large in some cases and unmaintainable
    - Hard to understand on whats going on

### Notes
- Gradle plugins provides tasks - 

> example :  
> ```sh
>  apply plugin : 'java'
> ```
> provides certain tasks ex:- assemble, build, compile , clean, jar

### Gradle commands
- ``` gradle tasks  ``` - lists the tasks available
-
