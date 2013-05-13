named-regex
==================

* Author: Tony Trinh (not affiliated with Berico Technologies)
* Url: http://tony19.github.com

> Fork of Tony's library for Named Capture Groups in Java 5/6.  It is included here for maintenance purposes (we did change the project `groupId` to our own).

This library is a thin wrapper for `java.util.regex`, implementing named capture groups for Java 5/6 (and it works on Android).

This is a fork of the [named-regexp][1] project from Google Code (currently inactive).

Usage
-----
You can use the same constructs for named capture groups from Java 7 (i.e., `(?<name>patt)`, etc.), as in the following example:

```java
import com.google.code.regexp.Pattern;
import com.google.code.regexp.Matcher;

public class NamedRegexpTest {
	public static void main(String[] args) {
		// pattern contains capture group, named "foo"
		Matcher m = Pattern.compile("(?<foo>\\w+) world").matcher("hello world!");
		m.find();
		System.out.println(m.group("foo")); // prints "hello"
	}
}
```
See more [examples][3]

Download
--------
Grab the latest release ([`named-regexp-0.1.9.jar`][4]) and include it in your classpath...

*OR* Maven users can simply add this dependency:

```xml
<repositories>
  <repository>
   <id>nexus.bericotechnologies.com</id>
   <name>Berico Technologies Nexus</name>
   <url>http://nexus.bericotechnologies.com/content/groups/public</url>
   <releases><enabled>true</enabled></releases>
   <snapshots><enabled>true</enabled></snapshots>
  </repository>
</repositories>

<dependency>
  <groupId>com.berico.utils</groupId>
  <artifactId>named-regexp</artifactId>
  <version>0.1.10</version>
</dependency>
```

Support
-------
Feel free to ask any questions at named-regexp@googlegroups.com.
Please report any issues in [JIRA][2].


License
-------
[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)

[1]: http://code.google.com/p/named-regexp
[2]: https://tony19.atlassian.net/issues/?jql=project%20%3D%20REGEX
[3]: http://tony19.github.com/named-regexp/index.html
[4]: https://oss.sonatype.org/content/repositories/releases/com/github/tony19/named-regexp/0.1.9/named-regexp-0.1.9.jar
[5]: https://oss.sonatype.org/content/repositories/snapshots/
[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/6153b1e63711b00863135b84138816f9 "githalytics.com")](http://githalytics.com/tony19/named-regexp)
