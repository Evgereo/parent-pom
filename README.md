# maven parent pom

## Getting started

Before adding parent pom dependency to your project, you need to build all components.

1) Build check-style and spotbugs using the command: mvn clean install (to install the artifact in the local repository).

2) Build parent-pom in the same way.

3) Add parent dependency to your pom.xml file.

```` markdown
<parent>
    <groupId>world.evgereo.maven</groupId>
    <artifactId>parent-pom</artifactId>
    <version>${CURRENT_VERSION}</version>
</parent>
````
