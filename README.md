# metric-maven-tile
Maven tile for performing metrics enhancement


## Example usage: In pom.xml add

In `properties` specify the packages to search for classes to enhance and the debug level showing classes being enhanced.

```xml
<properties>
	<metric.enhance.packages>org.example.myapp.**</metric.enhance.packages>
	<metric.enhance.args>debug=1</metric.enhance.args>
</properties>		
```


In `build plugins` add the tile:

```xml

<plugin>
	<groupId>io.repaint.maven</groupId>
	<artifactId>tiles-maven-plugin</artifactId>
	<version>2.8</version>
	<extensions>true</extensions>
	<configuration>
		<filtering>false</filtering>
		<tiles>
			<tile>org.avaje.metric:tile-enhance:1.1</tile>
		</tiles>
	</configuration>
</plugin>
```
