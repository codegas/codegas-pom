# codegas-pom

Modules to be used as CodeGas Parent and Import POMs

### GPG signing

The release process requires signing applications with GPG. This is to prevent man-in-the-middle attacks when deploying artifacts.

Follow these instructions for generating a GPG key pair and distributing the public key:
 
http://central.sonatype.org/pages/working-with-pgp-signatures.html

### Releasing

Releasing artifacts to Maven Central is done through Sonatype.

http://central.sonatype.org/pages/apache-maven.html

##### For SNAPSHOTs

Run the following to deploy a clean SNAPSHOT to the Sonatype SNAPSHOT repository

`mvn clean deploy`

##### For non-SNAPSHOTs

Run the following to run a clean-slate release prepartion which will walk through setting the release version and next SNAPSHOT version.

`mvn release:clean release:prepare`

Run the following to deploy prepared release to Sonatype staging repostiory

`mvn release:perform`