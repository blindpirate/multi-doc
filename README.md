# Run without afterEvaluate

```
$ gradle aggregateJavadocs -PsetPathNow=true

BUILD SUCCESSFUL in 1s
5 actionable tasks: 1 executed, 4 up-to-date
```

build/tmp/aggregateJavadocs/javadoc.options:
```
-classpath '/Users/zhb/Projects/tmp/multidoc/a/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/a/build/resources/main:/Users/zhb/Projects/tmp/multidoc/b/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/b/build/resources/main'
-d '/Users/zhb/Projects/tmp/multidoc/build/docs/javadoc'
-doctitle 'multidoc API'
-quiet
-taglet 'foo.ToDoTaglet'
-tagletpath '/Users/zhb/Projects/tmp/multidoc/taglet.jar'
-windowtitle 'multidoc API'
'/Users/zhb/Projects/tmp/multidoc/a/src/main/java/a/A.java'
'/Users/zhb/Projects/tmp/multidoc/b/src/main/java/b/B.java'
```

# Run with afterEvaluate

```
$ gradle aggregateJavadocs

> Task :aggregateJavadocs
javadoc: error - Error - Exception java.lang.ClassNotFoundException thrown while trying to register Taglet foo.ToDoTaglet...
/Users/zhb/Projects/tmp/multidoc/a/src/main/java/a/A.java:4: error: unknown tag: todo
 * @todo Fix this!
   ^
/Users/zhb/Projects/tmp/multidoc/b/src/main/java/b/B.java:4: error: unknown tag: todo
 * @todo Fix this!
   ^
3 errors


FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':aggregateJavadocs'.
> Javadoc generation failed. Generated Javadoc options file (useful for troubleshooting): '/Users/zhb/Projects/tmp/multidoc/build/tmp/aggregateJavadocs/javadoc.options'

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

* Get more help at https://help.gradle.org

BUILD FAILED in 1s
5 actionable tasks: 1 executed, 4 up-to-date
```

build/tmp/aggregateJavadocs/javadoc.options:

```
-classpath '/Users/zhb/Projects/tmp/multidoc/a/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/a/build/resources/main:/Users/zhb/Projects/tmp/multidoc/b/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/b/build/resources/main'
-d '/Users/zhb/Projects/tmp/multidoc/build/docs/javadoc'
-doctitle 'multidoc API'
-quiet
-taglet 'foo.ToDoTaglet'
-windowtitle 'multidoc API'
'/Users/zhb/Projects/tmp/multidoc/a/src/main/java/a/A.java'
'/Users/zhb/Projects/tmp/multidoc/b/src/main/java/b/B.java'
```

