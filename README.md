*under development status*


# jc

Java compile script for Maven projects.


## Why needs

`mvn compile` is slow, or `javac -cp` manually is labor, or IDE (such as Eclipse) is heavy.

Don't you want to compile a unit Java file simply?


## Usage

```
$ jc <Java source file>
```

This command will be interpreted `javac -cp ${BUILD_CLASSPATH} <Java source file> -d ${PROJECT_HOME}/target/classes`.

`${BUILD_CLASSPATH}` will be detected automatically with `mvn dependency:build-path`, and will be cached `${PROJECT_HOME}/.jcrc`. If `.jcrc` has been outdated (compared with pom.xml), re-run Maven and update itself.


## Installation

```
$ git clone https://github.com/keik/jc.git ~/.jc
```

And add `$PATH`
```
$ echo 'export PATH="$HOME/.jc/bin:$PATH"' >> ~/.bash_profile
```
