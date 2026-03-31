# AI School: Conductor — Repository Structure

The project is architected with a strict separation between public student materials and private mentor resources.

## 📁 Repository Overview

| Repository | Access | Purpose |
| :--- | :--- | :--- |
| **[AI-School](https://github.com/Distributed-Validators-Synctems/AI-School)** | **Public** | Curriculum landing page, registration links, and student guides. |
| **for_mentors** | **Private** | Detailed session instructions, "mentor secret sauce," and internal resources. |

## 🛠 Local Setup for Mentors

For security and privacy, the mentor guides are maintained in a separate private repository. Locally, the structure should look like this:

```text
AI-School/             (Public Repo Root)
├── README.md          (Public Curriculum)
├── .gitignore         (Excludes mentor_guides/)
└── mentor_guides/     (Cloned from 'for_mentors' private repo)
```

> [!IMPORTANT]
> The `mentor_guides/` folder must never be pushed to the public `AI-School` repository. This is enforced by the root `.gitignore`.

---
*Built for the Distributed Validators Synctems.*
