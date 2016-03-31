#Kotlin

## Competition:
- Ceylon: Sponsored by Redhat, not deemed good enough for them to actually use it...
- Clojure: No typesystem, A completely different set of paradigms and systax (which is unfamiliar to most people)
- Groovy: Typesystem is an afterthough, only kept alive by Gradle
- Scala: TBC

- Java (6, 7, 8): The reason the above exist


To be specific it is not intended to be an improvement over any of them. It is an improvement over Java. It actually makes Java coding easier (I know, I know, that sounds odd, but I find it quite true), and a lot more fun. Primarily by cutting away a lot of boilerplate, cruft and then by introducing the most critical type safety feature related to better null handling, even as the syntax is more natural, succinct and allows you to express your logic much better using functional constructs. (Java 8 does that, but somewhere you lose track of what the chain of functions was doing because of its verbosity).

Its strength is really its small learning curve for Java programmers. As in real small learning curve. And what supports that quite well is its retention of familiarity, and outstandingly well done java interoperability. So you don't have to worry much about reusing any of the java frameworks. All this put together makes kotlin one of the most productive languages I have ever used.

## Elephant in the room: Scala
- Type-Constructor Polymorphism (Higher kinded types)
- Implicit conversions, parameters, etc (This is a good thing IMHO)
- Macros
- Custom symbolic operators (GOOD!)
- Existential types
- Structural type definitions
- Path-dependant types
- ...


## Compare with Scala
 - Scala builds are really slow (And it takes a change in code style to make them not slow)
 - Scala has a _lot_ of Features
 - Operator overloading & implicit definitions can (and often do) make code


## Most important things:
- Ecosystem
- Quick builds / tests
- Tooling (IDE, build systems, package managers)
- Language Features

## The good
- Backed by Jetbrains
- Being used to create the best suite of IDES in the world, actually meets a need
- Great attitude towards null safety (Some leaky parts around java interop by design)




Pragmatic:
- Seamless Java interop, in both directions
- Can run on on Java 6




## Samples

### apply, let, run for builders
```
// Java
File makeDir(String path) {
  File result = new File(path);
  result.mkdirs();
  return result;
}

// Kotlin
fun makeDir(path: String): File = File(path).apply { mkdirs() }
```


```
// Java
Customer customer = new Customer()
customer.setName("Dave")
customer.setAge(21)


// Kotlin

```

### use instead of try with resource
```
val properties = Properties().apply {
  FileInputStream("path/to/file").use { load(it) }
}
```


# Learn
https://github.com/Kotlin/kotlin-koans
