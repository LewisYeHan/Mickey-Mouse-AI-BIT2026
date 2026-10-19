# 1.3 Application Software & Execution Lifecycle

**Development Status:** `drafted` (Substantive V1.0 Draft)  
**Author:** Cao Minh Tuan (`@mnhtnc`)  

---

## 1. Concept Explanations & Terminology

If System Software and the Operating System are the foundation, plumbing, and electricity of a building, **Application Software (Apps)** are the rooms and tools where humans actually get work done—such as writing essays, editing photos, browsing the web, or playing games.

### Key Terminology
* **Application Software:** End-user programs designed to perform specific, user-focused tasks (e.g., Microsoft Word, Spotify, Google Chrome, SOLIDWORKS), running on top of the Operating System.
* **User Space vs. Kernel Space:** To keep the computer safe, the OS divides memory into two zones: **User Space** (a restricted sandbox where applications run) and **Kernel Space** (a protected zone where the OS Kernel and drivers run with full hardware access).
* **System Call (Syscall) & API:** A controlled doorway through which an application in User Space politely asks the OS Kernel to perform a hardware action on its behalf (such as saving a file to the SSD or sending data over Wi-Fi).

---

## 2. Visual Sequence: How an Application Runs

```text
+---------------------------------------------------------------+
|               [ 1. Executable File Stored on SSD ]            |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|          [ 2. OS Loader Creates a Process in RAM ]            |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|           [ 3. CPU Executes App Instructions (Threads) ]      |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|       [ 4. App Requests Hardware via System Call (Syscall) ]  |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|      [ 5. OS Kernel Safely Performs Hardware Action ]         |
+---------------------------------------------------------------+
