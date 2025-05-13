# Fitness-Tracker

As someone passionate about fitness and health tracking, this system will empower users to log and analyze their workout routines efficiently, while giving administrators the tools to manage exercises and equipment.

Fitness Tracker CMS is a content management system designed to help users log, organize, and analyze their workouts, featuring a structured database with User, Workout, Exercise, and Equipment entities. Key functionalities include CRUD operations for managing workouts and exercises, progress tracking via charts (e.g., calories burned, workout frequency), and admin tools to curate exercise libraries and equipment links. The system leverages 1-M relationships (User→Workouts) and M-M relationships (Exercise↔Equipment) to enable scalable data interactions, with a user-friendly interface for logging workouts and visualizing fitness trends.

##  Entities & Relationships

###  Entities

1. **User**
2. **Workout**
3. **Exercise**
4. **Equipment**

### Relationships

#### 1. One-to-Many (1:M)
- **User → Workout**  
  One user can log many workouts.

- **Exercise → WorkoutExercise**  
  One exercise can appear in many workout logs.

- **Equipment → ExerciseEquipment**  
  One equipment type can be linked to many exercises.

#### 2. Many-to-Many (M:M)
- **Exercise ↔ Equipment**  
  Achieved via the `ExerciseEquipment` junction table.
