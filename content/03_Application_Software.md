# 1.3 Application Software & Execution Lifecycle

**Status:** Completed  
**Team Member:** Lu My Ky (`@jojolu11`)  

---

## 1. What is Application Software?
* End-user programs designed to help people perform specific tasks (e.g., Word, Excel, Chrome, Figma).
* Runs **on top of the Operating System**.

### 8 Categories of Apps
1. **Word processing:** Create and edit text documents (Microsoft Word, Google Docs).
2. **Spreadsheet:** Organize numbers, formulas, and charts (Excel, Google Sheets).
3. **Presentation:** Build slide decks for talks (PowerPoint, Canva).
4. **Multimedia:** Edit audio, video, and graphics (Premiere Pro, Audacity).
5. **Web browsers:** Access and browse websites (Chrome, Safari, Edge).
6. **Educational:** Help people learn through quizzes and lessons (Duolingo, Moodle).
7. **Graphics:** Professional design and photo editing (Photoshop, Blender, Figma).
8. **Simulation:** Model real-world scenarios for training (MATLAB, Flight Simulator).

---

## 2. The Execution Lifecycle
```text
[ 1. Executable file stored on SSD ]
                 |
                 v
[ 2. OS loader creates a process in RAM ]
                 |
                 v
[ 3. CPU executes instructions via threads ] <---+ (result back)
                 |                              |
                 v                              |
[ 4. App requests hardware via system call ] ---+
                 |
                 v
[ 5. Kernel performs action safely and returns ]
