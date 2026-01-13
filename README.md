# NoteIt App (Java Text Editor) 📝

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Swing](https://img.shields.io/badge/GUI-Swing_Framework-blue?style=for-the-badge)
![Event Driven](https://img.shields.io/badge/Pattern-Event_Driven-success?style=for-the-badge)

## 📖 Overview

**NoteIt** is a functional desktop text editor built with **Java Swing**. It showcases the implementation of a graphical user interface (GUI) with file I/O operations and native system integration.

## 🏗️ Software Architecture

### Component Hierarchy (`extends JFrame`)
The main class `editor` extends `JFrame`, serving as the primary window container.
-   **`JTextArea`**: One central component for text input, filling the center of the LayoutManager.
-   **`JMenuBar`**: Hosts the File and Edit menus.
-   **`JMenuItem`**: Triggers specific actions (Cut, Copy, Paste, Save).

### Listeners & Event Handling
The class implements the `ActionListener` interface to handle user interactions via `actionPerformed(ActionEvent e)`.
-   **Command Pattern**: The method switches on `e.getActionCommand()` to route logic (e.g., if "cut" -> call `t.cut()`).
-   **Clipboard Operations**: Leveraging built-in `JTextComponent` methods (`cut()`, `copy()`, `paste()`) to interact with the system clipboard.

### File I/O Implementation
-   **Opening Files**:
    -   `JFileChooser`: Provides a native file selection dialog.
    -   `FileReader` & `BufferedReader`: Reads character streams line-by-line and appends them to the text area.
-   **Saving Files**:
    -   `FileWriter` & `BufferedWriter`: Writes the content of the `JTextArea` back to the disk.

## 🎨 Theming

The application explicitly sets the **Metal Look and Feel** with the **OceanTheme** via `UIManager.setLookAndFeel()`, ensuring a consistent cross-platform appearance.

## 🚀 Execution

1.  Compile:
    ```bash
    javac code.java
    ```
2.  Run:
    ```bash
    java editor
    ```

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 👤 Author

**Simran Agarwal**
-   [Profile](https://github.com/officialsimranagarwal)
-   [LinkedIn](https://linkedin.com/in/simran-agarwal-54751b191)

---
*Generated with ❤️ by Simran Agarwal*
