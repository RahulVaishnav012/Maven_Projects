# Maven_Projects
#We are adding Jacoco plugin to generate the code coverage report
<build>
  <plugins>
     <plugin>
        <groupId>org.jacoco</groupId>
        <artifactId>jacoco-maven-plugin</artifactId>
        <version>0.8.7</version>
        <executions>
          <execution>
            <goals>
              <goal>prepare-agent</goal>
            </goals>
          </execution>
          <!-- attached to Maven test phase -->
          <execution>
            <id>report</id>
            <phase>test</phase>
            <goals>
              <goal>report</goal>
            </goals>
          </execution>
        </executions>
     </plugin>
  </plugins>
</build>

#To make our jar file as executable we need to add the below plugin
<plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-jar-plugin</artifactId>
        <version>3.4.2</version>
        <configuration>
					<archive>
						<manifest>
							<mainClass>com.dummy.App</mainClass>
						</manifest>
					</archive>
				</configuration>
  </plugin>
