# jc

Lightweight & fast Java compile script for Maven projects.


## Why

`mvn compile` is slow, or `javac -cp` manually is labor, or IDE (such as Eclipse) is heavy.

Don't you want to compile a unit Java file simply?


## Usage

```
$ jc <Java source file>
```

Above command will be interpreted `javac -cp ${BUILD_CLASSPATH} <Java source file> -d ${PROJECT_HOME}/target/classes`.

Value of `${BUILD_CLASSPATH}` will be retrieved automatically by `mvn dependency:build-path` and cached to `${PROJECT_HOME}/.jc_cache`. If `.jc_cache` has been outdated (compared with pom.xml), re-run Maven and update itself.


## Installation

```
$ git clone https://github.com/keik/jc.git ~/.jc
```

And add these lines to your `~/.bashrc`, `~/.profile`, or `~/.zshrc` file

```
export PATH="$HOME/.jc/bin:$PATH"
```


# License

MIT (c) keik
