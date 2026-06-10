# 📱 Kotlin To-Do Mobile Application

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)
![API](https://img.shields.io/badge/API-21+-blue)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

## 📋 Overview

A feature-rich Android to-do application built with Kotlin, demonstrating modern Android development practices including MVVM architecture, local database persistence, and responsive UI design.

### 🎯 Key Features

✅ **Task Management**
- Create, read, update, and delete tasks
- Mark tasks as complete/incomplete
- Priority levels (High, Medium, Low)
- Due date assignment and reminders
- Category organization

✅ **Data Persistence**
- SQLite local database storage
- Room database library implementation
- Automatic data synchronization
- Offline-first functionality

✅ **User Interface**
- Modern Material Design
- Responsive layout for all screen sizes
- Smooth animations and transitions
- Dark mode support
- Intuitive navigation

✅ **Architecture**
- MVVM (Model-View-ViewModel) pattern
- LiveData for reactive updates
- Repository pattern for data access
- Dependency injection with Hilt

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| **Language** | Kotlin |
| **Platform** | Android 5.0+ (API 21) |
| **Architecture** | MVVM |
| **Database** | SQLite + Room |
| **UI Framework** | Android Jetpack |
| **Async** | Coroutines |
| **Dependency Injection** | Hilt |

---

## 🚀 Installation & Setup

### Prerequisites
- Android Studio 4.0+
- Kotlin 1.4+
- SDK 21+
- Gradle 7.0+

### Build & Run

```bash
# Clone repository
git clone https://github.com/Ramana116/To-Do-App.git
cd To-Do-App

# Build the project
./gradlew build

# Run on emulator
./gradlew installDebug

# Or install APK
adb install app/build/outputs/apk/debug/app-debug.apk
```

---

## 📁 Project Structure

```
To-Do-App/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/ramana/todoapp/
│   │   │   │   ├── ui/
│   │   │   │   │   ├── MainActivity.kt
│   │   │   │   │   ├── TaskListFragment.kt
│   │   │   │   │   ├── TaskDetailFragment.kt
│   │   │   │   │   └── adapters/
│   │   │   │   │       └── TaskAdapter.kt
│   │   │   │   │
│   │   │   │   ├── viewmodel/
│   │   │   │   │   ├── TaskViewModel.kt
│   │   │   │   │   └── TaskListViewModel.kt
│   │   │   │   │
│   │   │   │   ├── repository/
│   │   │   │   │   └── TaskRepository.kt
│   │   │   │   │
│   │   │   │   ├── database/
│   │   │   │   │   ├── TaskDatabase.kt
│   │   │   │   │   ├── TaskDao.kt
│   │   │   │   │   └── Task.kt
│   │   │   │   │
│   │   │   │   ├── utils/
│   │   │   │   │   ├── Constants.kt
│   │   │   │   │   └── Extensions.kt
│   │   │   │   │
│   │   │   │   └── di/
│   │   │   │       └── AppModule.kt
│   │   │   │
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   ├── activity_main.xml
│   │   │   │   │   ├── fragment_task_list.xml
│   │   │   │   │   ├── fragment_task_detail.xml
│   │   │   │   │   └── item_task.xml
│   │   │   │   │
│   │   │   │   ├── values/
│   │   │   │   │   ├── colors.xml
│   │   │   │   │   ├── strings.xml
│   │   │   │   │   └── styles.xml
│   │   │   │   │
│   │   │   │   └── drawable/
│   │   │   │       ├── ic_add.xml
│   │   │   │       ├── ic_delete.xml
│   │   │   │       └── ic_edit.xml
│   │   │   │
│   │   │   └── AndroidManifest.xml
│   │   │
│   │   └── test/
│   │       ├── java/com/ramana/todoapp/
│   │       │   ├── TaskViewModelTest.kt
│   │       │   ├── TaskRepositoryTest.kt
│   │       │   └── TaskDaoTest.kt
│   │       │
│   │       └── androidTest/
│   │           └── java/com/ramana/todoapp/
│   │               └── TaskListFragmentTest.kt
│   │
│   ├── build.gradle
│   └── proguard-rules.pro
│
├── gradle/
│   └── wrapper/
│
├── build.gradle
├── settings.gradle
└── README.md
```

---

## 💻 Core Features

### 1. Task CRUD Operations
```kotlin
// Create task
fun createTask(task: Task) {
    viewModelScope.launch {
        taskRepository.insertTask(task)
    }
}

// Read tasks
fun getTasks(): LiveData<List<Task>> {
    return taskRepository.getAllTasks()
}

// Update task
fun updateTask(task: Task) {
    viewModelScope.launch {
        taskRepository.updateTask(task)
    }
}

// Delete task
fun deleteTask(task: Task) {
    viewModelScope.launch {
        taskRepository.deleteTask(task)
    }
}
```

### 2. MVVM Architecture
- Clean separation of concerns
- ViewModel manages UI state
- LiveData for reactive updates
- Repository pattern for data access

### 3. Room Database
- Type-safe database access
- Compile-time SQL verification
- Automatic schema migration
- Query optimization

### 4. Kotlin Features
- Coroutines for async operations
- Extension functions for cleaner code
- Data classes for model objects
- Null safety with optional types

---

## 🧪 Testing

```bash
# Run unit tests
./gradlew test

# Run instrumented tests
./gradlew connectedAndroidTest

# Run tests with coverage
./gradlew testDebugUnitTestCoverage
```

---

## 📱 Screenshots

[Add app screenshots showing:]
- Task list view
- Task creation dialog
- Task detail view
- Dark mode interface

---

## 🚀 Build & Release

```bash
# Debug build
./gradlew assembleDebug

# Release build
./gradlew assembleRelease

# Generate signed APK
./gradlew bundleRelease
```

---

## 📝 License

MIT License - see [LICENSE](LICENSE) for details.

---

## 👤 Author

**Ramana** - Mobile Developer
- GitHub: [@Ramana116](https://github.com/Ramana116)

---

## 🎓 Learning Outcomes

This project demonstrates:
- ✅ Kotlin programming best practices
- ✅ Android Jetpack libraries
- ✅ MVVM architectural pattern
- ✅ Local database persistence
- ✅ Responsive UI design
- ✅ Unit and instrumented testing

---

**Last Updated:** June 2026
**Status:** Production Ready ✅
