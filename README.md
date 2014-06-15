protoc-jar-maven-plugin
=======================

Protocol Buffers codegen plugin - based on protoc-jar executable JAR

Simple maven plugin to compile .proto files using protoc-jar embedded protoc compiler. See the Protocol Buffers site for details: https://code.google.com/p/protobuf/

Based on
* https://github.com/os72/protoc-jar
* https://github.com/igor-petruk/protobuf-maven-plugin

#### Usage
```xml
<plugin>
	<groupId>com.github.os72</groupId>
	<artifactId>protoc-jar-maven-plugin</artifactId>
	<version>2.5.0.1</version> <!-- protobuf 2.5.0 -->
	<!-- <version>2.4.1.1</version> --> <!-- protobuf 2.4.1 -->
	<executions>
		<execution>
			<phase>generate-sources</phase>
			<goals>
				<goal>run</goal>
			</goals>
			<configuration>
				<addSources>main</addSources>
				<outputDirectory>src/java</outputDirectory>
				<includeDirectories>
					<include>src/java</include>
				</includeDirectories>
				<inputDirectories>
					<include>src/java</include>
				</inputDirectories>
			</configuration>
		</execution>
	</executions>
</plugin>
```
