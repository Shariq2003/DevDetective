<div align="center">

# 🕵️ DevDetective

**Investigate any GitHub developer in a second — search a username and get their profile, stats and links on one clean card, in light or dark mode.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-dev--detective--neon.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://dev-detective-neon.vercel.app)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![GitHub API](https://img.shields.io/badge/GitHub_REST_API-181717?style=flat-square&logo=github&logoColor=white)
![GitHub last commit](https://img.shields.io/github/last-commit/Shariq2003/DevDetective?style=flat-square)

[Features](#-features) · [How it works](#-how-it-works) · [How to Use](#-how-to-use) · [Getting Started](#-getting-started) · [Contributing](#-contributing)

</div>

---

## ✨ Features

- 🔍 **Search any GitHub user** by username
- 🪪 **Profile card** with:

  | Section | Fields |
  |---|---|
  | Identity | Avatar · name · `@username` link · join date · bio |
  | Stats | Public repos · followers · following |
  | Links | Location · website · Twitter · company |

- 🌗 **Light / dark mode** toggle, remembered across visits with `localStorage`
- 🚫 **"No results"** feedback for usernames that don't exist
- 📱 **Responsive** design for all screen sizes

## 🔄 How it works

```mermaid
sequenceDiagram
    actor U as You
    participant App as DevDetective
    participant GH as api.github.com
    U->>App: Enter a username + Search / Enter
    App->>GH: GET /users/{username}
    alt user exists
        GH-->>App: profile JSON
        App-->>U: Render profile card
    else not found
        GH-->>App: 404 Not Found
        App-->>U: Show "No results"
    end
```

## 🎮 How to Use

1. Enter a GitHub username in the search bar.
2. Click **Search** or press **Enter**.
3. The profile appears below the search bar.
4. Toggle **LIGHT / DARK** with the mode button in the header.

## 🚀 Getting Started

No dependencies, no build step.

```bash
git clone https://github.com/Shariq2003/DevDetective.git
cd DevDetective
# open index.html in your browser
```

> ℹ️ The unauthenticated GitHub API allows 60 requests per hour per IP.

<details>
<summary><b>📁 Project structure</b></summary>

```text
DevDetective/
├── index.html
├── styles.css
├── script.js       # API call, rendering, theme toggle
└── assets/         # icons & favicon
```

</details>

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a branch: `git checkout -b feature/YourFeature`
3. Commit: `git commit -m "Add some feature"`
4. Push: `git push origin feature/YourFeature`
5. Open a Pull Request

---

<div align="center">

Built by **[Shariq](https://github.com/Shariq2003)** · [LinkedIn](https://www.linkedin.com/in/shariq-sd)

⭐ If you like this project, consider giving it a star!

</div>
