# Public Package Repository

To use packages from this repository, configure AVIO Github Package Registry as a maven repository.


In your POM, add following plugin repository in `pluginRepositories` tag (add if doesn't exist) -

```
    <pluginRepository>
        <id>github-avio-pkg</id>
        <name>AVIO Github Package Repository</name>
        <url>https://maven.pkg.github.com/avioconsulting/public-packages/</url>
        <layout>default</layout>
    </pluginRepository>
```
To access regular maven dependencies, add following repository in `repositories` tag (add if doesn't exist) -
```
    <repository>
        <id>github-avio-pkg</id>
        <name>AVIO Github Package Repository</name>
        <url>https://maven.pkg.github.com/avioconsulting/public-packages/</url>
        <layout>default</layout>
    </repository>
```
In your ~/.m2/settings.xml, add credentials for server id github-avio-pkg, like below -
```
    <server>
        <id>github-avio-pkg</id>
        <username>YOUR_GIT_USER</username>
        <password>YOUR_GIT_PERSONAL_TOKEN</password>
    </server>
```
See working-with-the-apache-maven-registry#authenticating-with-a-personal-access-token for more details on Github Package Authentication.

**NOTE:** The Github Personal Token must have **read:packages** permission.

