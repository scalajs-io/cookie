Cookie API for Scala.js
================================
[cookie](https://www.npmjs.com/package/cookie) - HTTP server cookie parsing and serialization.

### Description

Basic HTTP cookie parser and serializer for HTTP servers.

<a name="build_requirements"></a>
### Build Requirements

* [SBT v0.13.13](http://www.scala-sbt.org/download.html)

<a name="building_sdk"></a>
### Build/publish the SDK locally

```bash
 $ sbt clean publish-local
```

### Running the tests

Before running the tests the first time, you must ensure the npm packages are installed:

```bash
$ npm install
```

Then you can run the tests:

```bash
$ sbt test
```

### Examples

```scala
import io.scalajs.JSON
import io.scalajs.npm.cookie._

val cookies = Cookie.parse("foo=bar; equation=E%3Dmc%5E2")
println(s"cookies => ${JSON.stringify(cookies)}") //=> { "foo" : "bar", "equation" : "E=mc^2" }
```

### Artifacts and Resolvers

To add the `Cookie` binding to your project, add the following to your build.sbt:  

```sbt
libraryDependencies += "io.scalajs.npm" %%% "cookie" % "0.4.0-pre1"
```

Optionally, you may add the Sonatype Repository resolver:

```sbt   
resolvers += Resolver.sonatypeRepo("releases") 
```
