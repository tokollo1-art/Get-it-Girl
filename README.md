🎀 Get It, Girl! 🎀

The Accountability Partner That Doesn't Take 'No' For An Answer
Get It, Girl! is a high-energy productivity application designed to bridge the gap between simple task management and active habit coaching. Built in Java, it leverages strict OOP principles to ensure that your goals are managed with the same rigor you apply to your life.

✨ Features

Nesting & Hierarchy: Utilize recursive logic to break "Big Goals" down into small steps.

Escalating Accountability: A custom notification engine that increases urgency for overdue tasks as well as a check in feature that allows you to reflect on the incomplete/overdue task.

State Persistence: Seamlessly saves your progress to local JSON storage so you never lose your momentum.

Vibrant UX: A terminal or GUI-based interface designed with a modern, high-energy aesthetic.

🛠️ Tech Stack

Core: Java 17+ (utilizing Collections API, Generics, and Streams).

Build Tool: Maven (for dependency management and lifecycle control).

Storage: JSON (via Jackson or Gson) for local data persistence.

Environment: Pop!_OS / Linux.

🏗️ System Architecture (The "Brain")

This project follows a Model-View-Controller (MVC) pattern to keep the accountability logic separate from the user interface.

Key Components:
Goal Class (Model): An object-oriented representation of a task, containing metadata like creationDate, deadline, and accountabilityLevel.

AccountabilityEngine (Controller): The heart of the app. It iterates through the goal collection and calculates "Urgency Scores" based on elapsed time.

JsonStorageManager: Handles the serialization and deserialization of Java Objects into JSON format for persistence.

📂 Project Structure

Plaintext
src/main/java/com/getitgirl/
├── model/
│   ├── Goal.java            # Task structure and priority logic
│   └── UserProfile.java     # User settings and streak data
├── service/
│   ├── AccountabilityEngine.java  # The logic that "nudges" the user
│   └── StorageService.java        # Interface for JSON I/O
├── App.java                 # Entry point
└── ui/
    └── ConsoleStyles.java   # Custom ANSI colors for that "Girly Pop" feel

💅 Technical Highlights
Interface-Driven Design: The StorageService is built as an interface, allowing the app to switch from JSON to a SQL database in the future without breaking core logic.

Custom Exceptions: Created specific exception handling (e.g., TaskOverdueException) to manage the accountability flow gracefully.

Lambda Expressions: Used Java Streams to filter and sort tasks by urgency, ensuring high performance even with large lists.

Your goals are waiting. Get it, girl! 💅✨
