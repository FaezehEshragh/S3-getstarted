# App

This project contains a maven application with [AWS Java SDK 2.x](https://github.com/aws/aws-sdk-java-v2) dependencies.

## Prerequisites
- Java 1.8+
- Apache Maven
- GraalVM Native Image (optional)

## Development

Below is the structure of the generated project.

```
├── src
│   ├── main
│   │   ├── java
│   │   │   └── package
│   │   │       ├── App.java
│   │   │       ├── DependencyFactory.java
│   │   │       └── Handler.java
│   │   └── resources
│   │       └── simplelogger.properties
│   └── test
│       └── java
│           └── package
│               └── HandlerTest.java
```

- `App.java`: main entry of the application
- `DependencyFactory.java`: creates the SDK client
- `Handler.java`: you can invoke the api calls using the SDK client here.

#### Building the project
```
mvn clean package
```
#### Running the project
```
mvn exec:java -Dexec.mainClass="org.example.App"
```
#### AWS Config
Got access key and secret from aws IAM. 
You need to create a user (other than root) and for that user, you can create and access key.
To configure aws Access key, secret and region on your local use this command: 

```
aws configure
```
#### AWS Active Session Test
To make sure your config is correct and you have an active session, use this:

```
aws sts get-caller-identity

```


