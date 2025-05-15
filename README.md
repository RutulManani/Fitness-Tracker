# 🏋️‍♂️ Fitness Tracker CMS

## 💡 Overview

As someone passionate about fitness and health tracking, this system will empower users to log and analyze their workout routines efficiently, while giving administrators the tools to manage exercises and equipment.

Fitness Tracker CMS is a content management system designed to help users log, organize, and analyze their workouts, featuring a structured database with User, Workout, Exercise, and Equipment entities. Key functionalities include CRUD operations for managing workouts and exercises, progress tracking via charts (e.g., calories burned, workout frequency), and admin tools to curate exercise libraries and equipment links. The system leverages 1-M relationships (User→Workouts) and M-M relationships (Exercise↔Equipment) to enable scalable data interactions, with a user-friendly interface for logging workouts and visualizing fitness trends.

---

## 🎯 Key Features

- ✅ User registration and login
- ✅ Log workouts with date, time, and details
- ✅ Track exercises and calories burned
- ✅ Admin panel for managing workouts, exercises and equipment
- ✅ Progress visualization (e.g., workout frequency, calories burned)
- ✅ Scalable data model with relationships for Users, Workouts, Exercises, and Equipment

---

## 🗂️ Entities & Relationships

### 📦 Entities

- **User**  
  Stores user profile and login information.

- **Workout**  
  Records of individual workout sessions linked to users.

- **Exercise**  
  Library of exercises with details and categories.

- **Equipment**  
  Catalog of fitness equipment linked to exercises.

---

### 🔗 Relationships

1️⃣ **One-to-Many (1:M)**

- **User → Workout**  
  - A user can log multiple workouts.

- **Exercise → WorkoutExercise**  
  - An exercise can appear in many workout logs.

- **Equipment → ExerciseEquipment**  
  - A piece of equipment can be linked to multiple exercises.

2️⃣ **Many-to-Many (M:M)**

- **Exercise ↔ Equipment**  
  - Managed via an `ExerciseEquipment` junction table.
  - Allows exercises to be associated with multiple equipment types and vice versa.

---

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, JavaScript  
- **Backend**: Node.js / Express.js (or chosen framework)  
- **Database**: SQL / NoSQL (depending on implementation)  
- **Authentication**: JWT or session-based authentication  

---

## 📊 Example Data Flow

1. User logs in and records a workout session.
2. User selects exercises and optionally assigns equipment used.
3. The workout is stored in the database linked to the user.
4. Progress data is aggregated and visualized in charts.

