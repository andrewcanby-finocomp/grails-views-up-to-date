# grails-views-up-to-date

Example repo to reproduce https://github.com/grails/grails-views/issues/336

# Steps

* `./gradlew clean build`
* 💥


```
❯ ./gradlew clean build

> Task :compileGsonViews FAILED
Execution optimizations have been disabled for task ':compileGsonViews' to ensure correctness due to the following reasons:
  - Gradle detected a problem with the following location: '/projects/uptodateviews/build/gson-classes/main'. Reason: Task ':bootWarMainClassName' uses this output of task ':compileGsonViews' without declaring an explicit or implicit dependency. This can lead to incorrect results being produced, depending on what order the tasks are executed. Please refer to https://docs.gradle.org/7.2/userguide/validation_problems.html#implicit_dependency for more details about this problem.

FAILURE: Build failed with an exception.

* What went wrong:
Some problems were found with the configuration of task ':compileGsonViews' (type 'JsonViewCompilerTask').
  - In plugin 'org.grails.plugins.views-json' type 'grails.views.gradle.json.JsonViewCompilerTask' property 'compileOptions.encoding' is missing an input or output annotation.
    
    Reason: A property without annotation isn't considered during up-to-date checking.
    
    Possible solutions:
      1. Add an input or output annotation.
      2. Mark it as @Internal.
    
    Please refer to https://docs.gradle.org/7.2/userguide/validation_problems.html#missing_annotation for more details about this problem.
  - In plugin 'org.grails.plugins.views-json' type 'grails.views.gradle.json.JsonViewCompilerTask' property 'compileOptions.forkOptions' is missing an input or output annotation.
    
    Reason: A property without annotation isn't considered during up-to-date checking.
    
    Possible solutions:
      1. Add an input or output annotation.
      2. Mark it as @Internal.
    
    Please refer to https://docs.gradle.org/7.2/userguide/validation_problems.html#missing_annotation for more details about this problem.
  - In plugin 'org.grails.plugins.views-json' type 'grails.views.gradle.json.JsonViewCompilerTask' property 'compilerName' is missing an input or output annotation.
    
    Reason: A property without annotation isn't considered during up-to-date checking.
    
    Possible solutions:
      1. Add an input or output annotation.
      2. Mark it as @Internal.
    
    Please refer to https://docs.gradle.org/7.2/userguide/validation_problems.html#missing_annotation for more details about this problem.
  - In plugin 'org.grails.plugins.views-json' type 'grails.views.gradle.json.JsonViewCompilerTask' property 'fileExtension' is missing an input or output annotation.
    
    Reason: A property without annotation isn't considered during up-to-date checking.
    
    Possible solutions:
      1. Add an input or output annotation.
      2. Mark it as @Internal.
    
    Please refer to https://docs.gradle.org/7.2/userguide/validation_problems.html#missing_annotation for more details about this problem.
  - In plugin 'org.grails.plugins.views-json' type 'grails.views.gradle.json.JsonViewCompilerTask' property 'scriptBaseName' is missing an input or output annotation.
    
    Reason: A property without annotation isn't considered during up-to-date checking.
    
    Possible solutions:
      1. Add an input or output annotation.
      2. Mark it as @Internal.
    
    Please refer to https://docs.gradle.org/7.2/userguide/validation_problems.html#missing_annotation for more details about this problem.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

Deprecated Gradle features were used in this build, making it incompatible with Gradle 8.0.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

See https://docs.gradle.org/7.2/userguide/command_line_interface.html#sec:command_line_warnings

Execution optimizations have been disabled for 1 invalid unit(s) of work during this build to ensure correctness.
Please consult deprecation warnings for more details.

BUILD FAILED in 18s
6 actionable tasks: 6 executed

```
