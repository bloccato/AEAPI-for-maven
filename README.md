# Installing AdvancedEnchantments API in Local Maven Repository
This is a guide on how to make API for AdvancedEnchantments coded by GC from AdvancedPlugins working in Maven

# I'M NOT AN OFFICIAL DEVELOPER FOR ADVANCEDENCHANTMENTS

## Steps

- Download AdvancedEnchantments API jar file from [SpigotMC](https://www.spigotmc.org/resources/advancedenchantments-api.76819/)
- Move the jar you have downloaded to your local Maven repository (usually based in C:/Users/<profilename>/.m2)
- Open a terminal and write the following command
`mvn install:install-file -Dfile=<path> -DgroupId=<groupId> -DartifactId=<artifactId> -Dversion=<version> -Dpackaging=jar`
where:
**<path>** is your absolute path to jar file (i.e. C:/Users/<profilename>/.m2/jars/AdvancedEnchantments-8.7.4.jar),
**<groupId>** is the group id for the jar file you're importing (i.e. **ae**),
**<artifactId>** is the artifact id (i.e. **advancedenchantments**) and
**<version>** is the project version (i.e. **8.7.4**)
- Now open your pom.xml file on your project and go under *<dependencies>* tag and write the follow, replacing *groupId*, *artifactId* and *version* with the variables you provided before in the command.
    ```
    <dependency>
      <groupId>groupId</groupId>
      <artifactId>artifactId</artifactId>
      <version>version</version>
      <scope>compile</scope>
    </dependency>
    ```
