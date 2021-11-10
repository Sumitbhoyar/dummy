"# dummy" 

```
	<build>
		<plugins>
			<plugin>
				<groupId>org.jvnet.jaxb2.maven2</groupId>
				<artifactId>maven-jaxb2-plugin</artifactId>
				<version>0.12.3</version>
				<executions>
					<execution>
						<id>add-source-for-demoapp</id>
						<goals>
							<goal>generate</goal>
						</goals>
						<configuration>
							<schemaDirectory>src/main/resources/workflow</schemaDirectory>
							<schemaIncludes>
								<include>edu.xsd</include>
							</schemaIncludes>
							<bindingDirectory>src/main/resources/workflow</bindingDirectory>
							<bindingIncludes>
								<include>edu.xjb</include>
							</bindingIncludes>
							<generateDirectory>target/generated-sources/xjc/workflow</generateDirectory>
							<generatePackage>com.websystique.xml.workflow</generatePackage>
							<!--  Other configuration options-->
						</configuration>
					</execution>
				</executions>
			</plugin>
		</plugins>

	</build>
```

```

String sourceFile = "test1.txt";
        FileOutputStream fos = new FileOutputStream("compressed.zip");
        ZipOutputStream zipOut = new ZipOutputStream(fos);
        File fileToZip = new File(sourceFile);
        FileInputStream fis = new FileInputStream(fileToZip);
        ZipEntry zipEntry = new ZipEntry(fileToZip.getName());
        zipOut.putNextEntry(zipEntry);
        byte[] bytes = new byte[1024];
        int length;
        while((length = fis.read(bytes)) >= 0) {
            zipOut.write(bytes, 0, length);
        }
        zipOut.close();
        fis.close();
        fos.close();
        
```
