# DevOps Java Web

A small Java 21 web application built with Spring Boot. It serves a landing page
at `http://localhost:8080/` and reports application status at
`http://localhost:8080/api/health`.

## Run locally

Build and test with Maven:

```bash
mvn verify
```

Start the application:

```bash
mvn spring-boot:run
```

## Run with Docker

Build the image (the Dockerfile compiles the app and includes a Java runtime in
the final image):

```bash
docker build -t devops-java-web .
```

Run it:

```bash
docker run --rm -p 8080:8080 devops-java-web
```

## GitHub maintenance

GitHub Actions runs the Maven verification and builds the Docker image for
pushes and pull requests targeting `main`. Dependabot checks Maven dependencies
and GitHub Actions weekly.