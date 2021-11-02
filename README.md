"# dummy" 

<plugin>
    <groupId>org.codehaus.mojo</groupId>
    <artifactId>jaxb2-maven-plugin</artifactId>
    <version>2.3</version>
    <executions>
        <execution>
            <id>xjc</id>
            <goals>
                <goal>xjc</goal>
            </goals>
        </execution>
    </executions>
    <configuration>
        <xjbSources>
            <xjbSource>src/main/resources/global.xjb</xjbSource>
        </xjbSources>
        <sources>
            <source>src/main/resources/user.xsd</source>
        </sources>
        <outputDirectory>${basedir}/src/main/java</outputDirectory>
        <clearOutputDir>false</clearOutputDir>
    </configuration>
</plugin>
