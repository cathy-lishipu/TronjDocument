# Quickstart

## Installation

### Gradle Setting

Add repo setting:

```groovy
repositories {
    maven {
        url  "https://dl.bintray.com/starsakary/tronj"
    }
}
```

Then add `abi` as dependency.

```groovy
dependencies {
    ....

    implementation 'org.tron.tronj:abi:0.1.0'
    implementation 'org.tron.tronj:client:0.1.0'

    ....
}
```

###Maven Settings

Use maven repo setting from Bintray.

```xml
<dependency>
  <groupId>org.tron.tronj</groupId>
  <artifactId>abi</artifactId>
  <version>0.1.0</version>
  <type>pom</type>
</dependency>
```

## Using Tronj

### Choose net from **main net**, **shasta** or **nile**

```java
TronClient client = ofMainnet("your private key");
// TronClient client = ofShasta("your private key");
// TronClient client = ofNile("your private key");
```

### With private net

If using a private net, you may use another constructor: `TronClient(String grpcEndpoint, String grpcEndpointSolidity, String hexPrivateKey)`

```java
TronClient client = new TronClient("127.0.0.1:50051", "127.0.0.1:50052", "your private key");
```

Aftre binding your private key with the `TronClient` object, your are ready to build, sign and broadcast your transactions.



## Refer to Javadocs

Tronj has javadocs for essential classes and functions, you may use `gradle javadoc` to generate Javadocs for a specific package to read more details.