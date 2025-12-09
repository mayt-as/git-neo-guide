# Git Neo-Guide 🚀

A modern, interactive Git Cheat Sheet designed with the **NeoPop** aesthetic (inspired by CRED's design system). This single-page application provides a clean, visual guide to essential Git commands, parameters, and workflows.

## ✨ Features

* **Neo-Brutalist Design**: High contrast, hard shadows, and vibrant accent colors based on the NeoPop design language.
* **Modern Git Commands**: Focuses on modern best practices, including `git switch`, `git restore`, and cleaner workflow tips (like `--rebase`).
* **Visual Workflow Diagram**: A built-in visualization of how data moves between your working directory and the remote repository.
* **Responsive Layout**: Fully responsive masonry grid layout that works perfectly on mobile, tablet, and desktop.
* **Single-File Architecture**: The entire website (HTML, CSS, SVG) is contained in a single `index.html` file for easy deployment.

## 📊 Git Workflow

The guide is built around this core data flow:

```mermaid
graph LR
    %% Define Nodes
    WD[Working Dir]
    SA[Staging Area]
    LR[Local Repo]
    RR[Remote Repo]

    %% Forward Actions
    WD -- git add --> SA
    SA -- git commit --> LR
    LR -- git push --> RR

    %% Backward/Sync Actions
    RR -- git pull --> LR
    LR -- git reset --> SA
    SA -. git restore / checkout .-> WD

    %% Styling
    style WD fill:#1a1a1a,stroke:#333,color:#fff
    style SA fill:#1a1a1a,stroke:#333,color:#fff
    style LR fill:#1a1a1a,stroke:#333,color:#fff
    style RR fill:#1a1a1a,stroke:#333,color:#fff
```

## 🚀 How to Use

Since this is a static website contained in a single file, you don't need to install any dependencies.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/git-neo-guide.git](https://github.com/yourusername/git-neo-guide.git)
    ```
2.  **Open the file:**
    Simply double-click `index.html` to open it in your web browser.

## 🛠️ Tech Stack

* **HTML5**: Semantic structure.
* **CSS3**: Custom properties (Variables), Flexbox, CSS Grid (Masonry), and embedded SVGs.
* **No JavaScript**: Pure CSS interactions for hover states and layout logic.

## 🎨 Design System

This project implements a simplified version of the **NeoPop** design system:

* **Background**: `#0d0d0d` (Dark Mode)
* **Typography**: `Inter` for UI, `Fira Code` for commands.
* **Accents**:
    * **Green**: Syntax
    * **Cyan**: Parameters
    * **Rose**: Danger/Undo Actions
    * **Amber**: Branching

## 🤝 Contributing

Contributions are welcome! If you want to add more commands or improve the diagram:

1.  Fork the Project.
2.  Create your Feature Branch (`git switch -c feature/AmazingFeature`).
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the Branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.