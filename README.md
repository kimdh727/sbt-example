# SBT Example

For sbt example project

[scala-sbt.org](https://www.scala-sbt.org/index.html)

## Create sbt build

```sh
touch build.sbt
```

## Start sbt shell

```sh
sbt
```

## Exit sbt shell

```sbt
sbt:sbt-example> exit
```

## Compile a project

```sbt
sbt:sbt-example> compile
```

## Recompile on code change

Automatically re-executed whenever one of the source files within the project is modified.

Press `Enter` to exit `~compile`

```sbt
sbt:sbt-example> ~compile
```

## Getting help

```sbt
sbt:sbt-example> help
```

```sbt
sbt:sbt-example> inspect
```

```sbt
sbt:sbt-example> inspect tree
```

## Run your app

```sbt
sbt:sbt-example> run
```

## Save the session to build.sbt

```sbt
sbt:sbt-example> session save
```

## Reload the build

```sbt
sbt:Hello> reload
```

## Run tests

```sbt
sbt:Hello> test
```

## Run incremental tests continuously

```sbt
sbt:Hello> ~testQuick
```

## List all subprojects

```sbt
sbt:Hello> projects
```

## Broadcast commands

Set `aggregate` so that the command `hello` is broadcast to `helloCore` too

## Make dependncy

Use `dependsOn(...)` to add a dependency on other subprojects.

## Add sbt-native-packager plugin

Create `project/plugins.sbt`:

```scala
addSbtPlugin("com.typesafe.sbt" % "sbt-native-packager" % "1.3.4")
```

Change `build.sbt` as follows to add `JavaAppPackaging`:

```scala
...
.enablePlugins(JavaAppPackaging)
...
```

## Create a .zip dustribution

```sbt
sbt:Hello> dist
```

## Dockerize your app

```sbt
sbt:Hello> Docker/publishLocal
```

## Set the version

```scala
ThisBuild / version := <version>
```

## Switch saclaVersion temporarily

```sbt
sbt:Hello> ++2.12.14!
```

This setting will go away after `reload`.

## Batch mode

```sh
sbt clean "testOnly HelloSpec"
```

## sbt new command

```sh
sbt new scala/scala-seed.g8
```

```sh
...
A minimal Scala project.

name [Scala Seed Project]: hello

Template applied in ./hello
```
