# jvm  [![Build Status](https://travis-ci.org/caarlos0/jvm.svg?branch=master)](https://travis-ci.org/caarlos0/jvm)

> The _"Java Version Manager"_

Automatically change `JAVA_HOME` based on current directory `pom.xml`
or `.java-version` files.

For now, only Ubuntu and OSX are supported.

### Usage

```sh
git clone https://github.com/caarlos0/jvm.git ~/.jvm

# for bash
echo "source ~/.jvm/jvm.sh" >> .bashrc

# for zsh
echo "source ~/.jvm/jvm.sh" >> .zshrc
```

Then, just `cd` to a java project folder. If the `pom.xml`  has a
`<java.version>1.7</java.version>`, for example, jvm will try to
set JDK7 to your PATH.

If you don't have and don't want to have this in your project's pom,
you can also do this:

```sh
echo 7 >> .java-version
```


### TODO

- Add support for more platforms (maybe via some config file);
- Better documentation;
- Tests;
- Replace JAVA_HOME in PATH instead of replacing it;
- Set JAVA_HOME only when changed;
