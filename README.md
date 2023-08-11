https://youtrack.jetbrains.com/issue/KT-61147
===========================================

Steps to reproduce:

1. `$ git clone https://github.com/nsk-mironov/KT-61147`
2. `$ cd KT-61147`
3. `$ ./gradlew :run`
4. The project compiles, but fails in a runtime with the following error:

```
> Task :run FAILED
Exception in thread "main" java.lang.NoSuchFieldError: DEFAULT_DATE_PATTERN
        at com.google.gson.GsonBuilder.<init>(GsonBuilder.java:95)
        at crashme.CrashMeKt.main(CrashMe.kt:6)
        at crashme.CrashMeKt.main(CrashMe.kt)

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':run'.
> Process 'command '/opt/homebrew/Cellar/openjdk@11/11.0.19/libexec/openjdk.jdk/Contents/Home/bin/java'' finished with non-zero exit value 1

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org
```
