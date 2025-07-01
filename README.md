# 🕒 Spring Boot Scheduling Tasks Example

This is a simple Spring Boot project that demonstrates how to use `@Scheduled` tasks to run background jobs on a fixed schedule.  
It also supports containerization using **Cloud Native Buildpacks**, enabling easy Docker image generation without writing a `Dockerfile`.

---

## 🚀 Features

- ✅ Scheduled background task that runs every 5 seconds
- 🛠️ Built with Spring Boot and Gradle
- 🐳 Docker image built via **Buildpacks**
- 📦 No need for Dockerfile
- ☁️ Ready for container deployment

---

## 📁 Project Structure

```
.
├── src/
│   └── main/
│       ├── java/com/example/demo/
│       │   └── ScheduledTasks.java
│       └── resources/
│           └── application.properties
├── build.gradle
├── .gitignore
└── README.md
```

---

## 🧪 How to Run

### 🔹 Run locally (without Docker)

```bash
./gradlew bootRun
```

Or build and run the `.jar`:

```bash
./gradlew build
java -jar build/libs/scheduling-tasks-0.0.1-SNAPSHOT.jar
```

---

### 🐳 Build Docker image using Buildpacks

Make sure Docker is installed and running.

```bash
./gradlew bootBuildImage
```

This creates a Docker image named:

```
scheduling-tasks:0.0.1-SNAPSHOT
```

---

### ▶️ Run the Docker container

```bash
docker run -p 8080:8080 scheduling-tasks:0.0.1-SNAPSHOT
```

---

## 📓 Notes

- The scheduled task will print a message every 5 seconds in the console.
- Buildpacks use the [Paketo](https://paketo.io/) buildpack under the hood.
- Docker is not required if you only run the `.jar` locally.

---

## 🧑‍💻 Author

Created by [Your Name].  
Feel free to fork, contribute, or use this as a reference for scheduling and containerization.
