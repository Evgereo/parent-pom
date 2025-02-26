# maven parent pom

## Uses:
- **Java 17**
- **Maven 3.6.3**
- **Spring Boot 3.2.2**

## Getting started

Before adding parent pom dependency to your project, you need to build all components.

1) Build check-style and spotbugs using the command: `mvn clean install` (to install the artifact in the local repository).

2) Build parent-pom in the same way.

3) Add parent dependency to your pom.xml file.

``` markdown
<parent>
    <groupId>world.evgereo.maven</groupId>
    <artifactId>parent-pom</artifactId>
    <version>${CURRENT_VERSION}</version>
</parent>
```

## Management code quality plugins

### Checkstyle plugin

Checkstyle is a static code analyzer for Java that checks whether the code conforms to specified standards of layout and style.
All settings are described in the file: `checkstyle.xml.vm`

By default, the checkstyle plugin is enabled by a maven profile named: `check-style`.

To disable the checkstyle plugin, run maven lifecycle commands with the flag: `-P!check-style`.

Checkstyle doc: https://checkstyle.sourceforge.io

### SpotBugs plugin

SpotBugs is a static code analyzer for Java that looks for potential bugs, vulnerabilities and problems in code. 
It analyzes bytecode and identifies patterns that can lead to bugs, memory leaks or other problems.

By default, the spotbugs plugin is enabled by a maven profile named: `spotbugs`.

To disable the check style plugin, run maven lifecycle commands with the flag: `-P!spotbugs`.

Spotbugs doc: https://spotbugs.readthedocs.io
