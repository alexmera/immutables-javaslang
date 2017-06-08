immutables-vavr
===

[![Build Status](https://travis-ci.org/alexmera/immutables-vavr.svg)](https://travis-ci.org/alexmera/immutables-vavr)
[![Download](https://api.bintray.com/packages/alexmera/mvn/immutables-vavr/images/download.svg) ](https://bintray.com/alexmera/mvn/immutables-vavr/_latestVersion)

A set of [Immutables](http://immutables.org) encodings for [Vavr](http://www.vavr.io).

**NOTE: This project is forked from [immutables/immutables-javaslang](https://github.com/immutables/immutables-javaslang)
and migrate from the (old) Javaslang distribution to the new Vavr brand.** 

#### Ten Second Tutorial

Include the encodings in your project:

```
<dependency>
  <groupId>org.immutables.vavr</groupId>
  <artifactId>vavr-encodings</artifactId>
  <version>0.1.1</version>
  <scope>provided</scope>
</dependency>
```

Annotate your types with `@VavrEncodingEnabled`. Alternatively,
you can annotate a `@Style` annotation with `@VavrEncodingEnabled`
and have it apply to any types that are using that style. See
[Styles](http://immutables.github.io/style.html).

Now, any use of [Vavr](http://www.vavr.io) collections in your
abstract value types will magically result in the generated `Builder`
types being augmented with methods to build immutable collections
element-by-element. Use of Vavr's `Option` type will receive
the same special treatment as the standard Java `Optional` type.

