# Command Reader

Command Reader allows you to execute a command and read it into a file.

## Use 

To use it in your maven project add the following to your pom.xml

```
<plugin>
    <groupId>org.command.reader.plugins</groupId>
    <artifactId>command-reader-maven-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
    <configuration>
        <workingDirectory>src/main/frontend</workingDirectory>
        <outputDirectory>src/main/frontend</outputDirectory>
        <command>ls</command>
        <additionalCommands>
            <commandone>ls -a</commandone>
        </additionalCommands>
    </configuration>
    <executions>
        <execution>
            <phase>generate-resources</phase>
            <goals>
                <goal>frontend-resources</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```            