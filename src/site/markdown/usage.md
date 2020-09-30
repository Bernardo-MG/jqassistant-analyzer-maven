# Usage

The project is based on the the [JQAssistant plugin][jqassistant-plugin]. Their documentation contains detailed information.

By default the project can scan a single project, defined through the scan.path property. This has to be the root of a Java project, for example a Maven project.

To scan just run this project like this:

```
mvn clean verify -Dscan.path=[path to project]
```

### Cleaning Up the Graph

On complex or multimodule projects some classes may appear duplicated. The merge profile will fix this:

```
mvn clean verify -Pmerge -Dscan.path=[path to project]
```

## Additional Projects

To scan more than one project edit the JQAssitant Plugin configuration in the POM. Add a scanInclude node for each project:

```
<scanIncludes>
   <scanInclude>
      <path>c:\project1</path>
   </scanInclude>
   <scanInclude>
      <path>c:\project2</path>
   </scanInclude>
</scanIncludes>
```

## Adding Rules

As indicated in [JQAssistant's docs][jqassistant-rules], new rules can be added to the /jqassistant folder.

Remember to register them into the JQAssistant plugin execution:

```
<execution>
   <id>jqassistant-analyze</id>
   <goals>
      <goal>analyze</goal>
   </goals>
   <configuration>
      <groups>
         <group>custom:Default</group>
      </groups>
      <concepts>
         <concept>custom:*</concept>
      </concepts>
   </configuration>
</execution>
```

[jqassistant-plugin]: https://github.com/kontext-e/jqassistant-plugins
[jqassistant-rules]: http://jqassistant.github.io/jqassistant/doc/1.8.0/#_add_a_rule