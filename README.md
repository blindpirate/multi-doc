```
$ gradle aggregateJavadocs 

BUILD SUCCESSFUL in 1s
5 actionable tasks: 1 executed, 4 up-to-date
```

build/tmp/aggregateJavadocs/javadoc.options:
```
-classpath '/Users/zhb/Projects/tmp/multidoc/a/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/a/build/resources/main:/Users/zhb/Projects/tmp/multidoc/b/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/b/build/resources/main'
-d '/Users/zhb/Projects/tmp/multidoc/build/docs/javadoc'
-quiet
-taglet 'foo.ToDoTaglet'
-tagletpath '/Users/zhb/Projects/tmp/multidoc/taglet.jar:/Users/zhb/Projects/tmp/multidoc/a/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/a/build/resources/main:/Users/zhb/Projects/tmp/multidoc/b/build/classes/java/main:/Users/zhb/Projects/tmp/multidoc/b/build/resources/main'
'/Users/zhb/Projects/tmp/multidoc/a/src/main/java/a/A.java'
'/Users/zhb/Projects/tmp/multidoc/b/src/main/java/b/B.java'
```
