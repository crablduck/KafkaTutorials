# Flink


 To make the applications run within IntelliJ IDEA, the Flink dependencies need to be declared in scope compile rather than provided. Otherwise IntelliJ will not add them to the classpath and the in-IDE execution will fail with a NoClassDefFountError. To avoid having to declare the dependency scope as compile (which is not recommended, see above), the above linked Java- and Scala project templates use a trick: They add a profile that selectively activates when the application is run in IntelliJ and only then promotes the dependencies to scope compile, without affecting the packaging of the JAR files.