# sona-flutter

### Download `sona-flutter plugin`

https://github.com/insideapp-oss/sonar-flutter/releases

### Download and install `sonar-scanner-cli`

https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/

### Run

```shell
docker compose up -d
```

### Create `sonar-project.properties` file to root project

```
sonar.projectKey=com.myapp:my-app
sonar.projectName=my-app
sonar.projectVersion=1.0.0
sonar.host.url=http://localhost:9000
sonar.login=admin
sonar.password=P@ssw0rd
sonar.sources=lib
sonar.tests=test
sonar.sourceEncoding=UTF-8
```

### Run test

```shell
flutter pub get 
flutter test --machine > tests.output
flutter test --coverage
```

### Run the analysis and publish to the SonarQube server

```shell
sonar-scanner
```