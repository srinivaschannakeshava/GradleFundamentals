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

- Defining and using tasks
    - Tasks
        - has a lifecycle
        - has properties
        - has actions
            - firstAction
            - lastAction
            - has dependencies
- Build Phases
    1. Init phase 
    2. Configuration phase - ex: description
    3. Execution phase - ex: doFirst,doLast

- Task Dependencies
    - dependsOn
    - mustRunAfter
    - shouldRunAfter
    - finalizedBy
- Typed Tasks 
    - Mainly for creating reussable tasks
    - Generic tasks already part of gradle.
    - Its used by injecting into the task 
- Building Java Project
    - ```gradle --daemon build ``` - this runs a gradle deamon uses the existing running jvm for building reducing the process time 
- Dependencies - your project has dependencies and they can be
    - Other project
    - External libraries
    - Internal libraries
    > These dependencies can be satisfied in various ways
    > - Other projects
    > - File system
    > - Maven repository
    > - Ivy repository
    - Configuration within gradle
       ``` Java plugin introduces
        - compile
        - runtime
        - testCompile
        - testRuntime ```
    - Transistive dependencies
    - Repositories - You can specify local, private , central .... single, multiple sources etc..
    - Gradle Cache 
- Gradle tests
    - ```gradle test```
    - You can add filter to tests    
    - **gradle-testsets-plugin** for running integration tests
- Gradle Wrapper
    - provides specific version og gradle to the project
        - helps in consistant builds
        - gradlew.bat for windows 
        - gradlew.sh for linux
    - Wrapper Task     


### Gradle commands
- ``` gradle tasks  ``` - lists the tasks available
- ``` gradle -i taskName ``` - run in info mode
- ``` gradle -q dependencies ``` - lists the dependency libs
- ``` gradle -q dependencies -configuration compile ``` - dependency w.r.t specific configuration

