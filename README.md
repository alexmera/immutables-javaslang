immutables-vavr
===

[![Build Status](https://travis-ci.org/alexmera/immutables-vavr.svg)](https://travis-ci.org/alexmera/immutables-vavr)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.immutables.javaslang/javaslang/badge.png)](https://maven-badges.herokuapp.com/maven-central/org.immutables.javaslang/javaslang)

A set of [Immutables](http://immutables.org) encodings for [Vavr](http://www.vavr.io).

#### Ten Second Tutorial

Include the encodings in your project:

```
<dependency>
  <groupId>org.immutables.javaslang</groupId>
  <artifactId>javaslang-encodings</artifactId>
  <version><!-- Insert latest version here --></version>
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

