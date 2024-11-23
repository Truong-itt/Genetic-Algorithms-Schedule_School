# Genetic Algorithm (GA) for Timetable Scheduling

This project applies **Genetic Algorithm (GA)** to solve the complex problem of timetable scheduling by representing the problem in a 3D space and optimizing the allocation of subjects, teachers, and classrooms under defined constraints.

---

## 1. Problem Overview

### **Timetable Representation**
- The timetable is represented as a **3D model**:
  - **X-axis (Days)**: Days of the week (Monday → Saturday).
  - **Y-axis (Periods)**: Class periods (Period 1 → Period 8).
  - **Z-axis (Rooms)**: Available classrooms (e.g., A101, A102, A103).

### **Constraints**
1. **Hard Constraints** (must be satisfied):
   - Teachers cannot teach multiple classes at the same time.
   - Classrooms cannot be assigned to multiple classes at the same time.
   - Subjects must be assigned to qualified teachers.
   - Each class can only study one subject per period.
   - Number of lessons per day must not exceed the limit.

2. **Soft Constraints** (preferred but not required):
   - Classes are scheduled during the free time of lecturers.
   - Subjects are distributed to avoid gaps in the lecturer's schedule.
   - Important subjects (e.g., Math, Literature) are prioritized in the morning.

---

## 2. Solution Workflow

### **Input Data**
- List of subjects, teachers, classes, and classrooms.
- Lecturer's free time.
- Hard and soft constraints.

### **Workflow Steps**
1. **Modeling the Problem Space**:
   - Represent the timetable as a 3D structure (Day, Period, Room).

2. **Generate Initial Population**:
   - Randomly assign subjects, teachers, and classes into the 3D timetable while adhering to hard constraints.

3. **Optimization**:
   - Use Genetic Algorithm (GA) to reduce violations of hard constraints and optimize for soft constraints.

4. **Output**:
   - Generate the final timetable represented in 3D, with each cell containing the allocated subject, teacher, and class.

---

## 3. Genetic Algorithm (GA) Summary

### Key Steps:
1. **Population Initialization**:
   - Randomly generate initial feasible timetables.
2. **Fitness Evaluation**:
   - Evaluate the quality of timetables based on the number of constraint violations.
3. **Selection**:
   - Select the best timetables based on fitness scores.
4. **Crossover**:
   - Combine two parent timetables to produce new offspring.
5. **Mutation**:
   - Introduce random changes to timetables to increase diversity.
6. **Iteration**:
   - Repeat the process until reaching the stopping condition (e.g., max generations or desired fitness).

---

## 4. Result

### **Timetable Representation**
- The final timetable is visualized as a 3D model:
  - **X-axis**: Days of the week.
  - **Y-axis**: Periods in a day.
  - **Z-axis**: Classrooms.

- Each cell contains:
  - Subject name.
  - Assigned teacher.
  - Class information.

### Example:
- A cell `(Saturday, Period 4, Room A101)` contains the following data:
  - Subject: Math.
  - Teacher: Mr. John.
  - Class: Class 10A.

---

## 5. Requirements and Usage

### **Requirements**:
- Python 3.x.
- Required libraries:
  - `numpy`
  - `matplotlib` (if visualizing the timetable)

### **Usage**:
1. Clone the repository:
   ```bash
   git clone <repository-link>
   cd <repository-folder>
   ```
