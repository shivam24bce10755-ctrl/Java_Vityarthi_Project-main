# Student Management System (Vityarthi Project)

[Repository](https://github.com/shivam24bce10755-ctrl/Java_Vityarthi_Project-main)

![Java](https://img.shields.io/badge/Java-11%2B-blue) ![Build Status](https://github.com/shivam24bce10755-ctrl/Java_Vityarthi_Project-main/actions/workflows/java-ci.yml/badge.svg) ![License: MIT](https://img.shields.io/badge/License-MIT-yellow)

---

## Project Summary

**Student Management System (Vityarthi Project)** is a console-based Java SE application for managing student records, courses, enrollments, and grades. The project demonstrates modern Java features and good coding practices: OOP, design patterns, exception handling, file I/O (NIO.2), Streams & lambdas, Date/Time API, generics and a modular package layout.

---

## Key Features

* Student CRUD (create, update, list, deactivate)
* Course creation and search (by instructor, department, semester)
* Enrollment with business-rule validation (credit limits, duplicate checks)
* Grade recording, GPA calculation and transcript generation
* CSV import/export and timestamped backups using NIO.2
* Reports: GPA distribution, top students, enrollment statistics
* Clean separation of concerns (cli, domain, service, io, util, config, exception)

---

## Tech Stack

* Language: Java (11+ recommended)
* Build / Run: javac / java (command-line) or any Java IDE (Eclipse, IntelliJ)
* Storage: CSV files for sample data (in `data/`)
* Patterns: Singleton, Builder (where applicable)
* APIs used: Streams API, java.time, NIO.2

---

## Project Structure

Below is the repository layout (formatted from your screenshot):

```
Java_Vityarthi_Project-main/
├── screenshots/
│   ├── file_struct.png
│   ├── java_check.png
│   ├── menu_testing.png
│   └── menu.png
├── Student Management System/
│   ├── data/
│   │   ├── courses.csv
│   │   └── students.csv
│   └── edu/
│       └── ccrm/
│           ├── cli/           # Command-line interface classes
│           ├── config/        # Configuration management
│           ├── domain/        # Domain models (Person, Student, Course, etc.)
│           ├── exception/     # Custom business exceptions
│           ├── io/            # Import/export & backup utilities (NIO.2)
│           ├── service/       # Business logic / services
│           └── util/          # Utility classes (reports, helpers)
├── Main.java                   # Application entry point
└── README.md
```

> Note: When committing, ensure folder names with spaces are handled properly. If you prefer, you can rename `Student Management System` to `student-management-system` for easier cross-platform use.

---

## Installation & Setup

### Prerequisites

* Java 11 or newer installed
* Command-line (Command Prompt / PowerShell on Windows, Terminal on macOS/Linux) or an IDE (Eclipse / IntelliJ)

### Quick steps (command-line)

1. Open a terminal and navigate to the project root (where `Main.java` is).
2. Compile:

```bash
# Example: compile all java files and place classes into out/
find . -name "*.java" > sources.txt
javac -d out @sources.txt
```

3. Run:

```bash
java -cp out Main
```

> If `find` is not available (Windows), compile within your IDE or use explicit `javac` commands per package.

### Running in an IDE (Eclipse / IntelliJ)

1. Create a new Java project and import the repository folder (or create a project and copy sources).
2. Ensure the Java SDK is set to 11+.
3. Mark source folders (e.g., the `edu` package root) as source roots if necessary.
4. Run `Main.java` as a Java application.

---

## How to Use (CLI flow)

Typical user flow after starting the application:

1. Application loads configuration and reads CSV sample data (if present).
2. Use the menu to:

   * Add / Edit / Deactivate students
   * Add / Search / Update courses
   * Enroll / Unenroll students (with validations)
   * Record grades and generate transcripts
   * Export data to CSV and create timestamped backups
   * Generate reports (GPA distribution, top students, enrollment stats)

---

## Data Files

* `Student Management System/data/students.csv` — sample student data
* `Student Management System/data/courses.csv` — sample course data

You may import/export CSV files using the application's import/export facility.

---

## Screenshots

Screenshots are included in the repository under `screenshots/`. Relative paths are used here so they render correctly on GitHub.

Project file structure screenshot:

![Project structure](screenshots/file_struct.png)

Java version check / environment verification:

![Java verification](screenshots/java_check.png)

Application menu:

![Main menu](screenshots/menu.png)

Menu testing / runtime example:

![Menu testing](screenshots/menu_testing.png)

---

## Mapping to Course / Syllabus Topics

* **OOP Principles**: Encapsulation, Inheritance, Abstraction, Polymorphism — implemented across domain classes.
* **Design Patterns**: Singleton (e.g., `AppConfig`), Builder (e.g., `Course.Builder`).
* **Exception Handling**: Custom exceptions for business rules (duplicate enrollments, credit limits).
* **Collections & Streams**: Stream API and lambda expressions for filtering, grouping and statistical reports.
* **File I/O**: NIO.2 (`Path`, `Files`) for CSV I/O and backups.
* **Date/Time API**: `java.time.LocalDate` and related classes for dates.
* **Generics & Type Safety**: Generic interfaces for reusable components.
* **Enums**: Grade / Semester definitions.

---
