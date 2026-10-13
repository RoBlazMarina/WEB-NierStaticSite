# 🤖 YORHA System

**Coordination System for the YORHA Project**

A static website inspired by the universe of *NieR: Automata*. It simulates the internal platform YoRHa androids use to coordinate their operations from the Bunker: checking the regulations, reviewing the shift calendar and reporting incidents.

> 🌐 **Language note:** the website's content and interface are written entirely in **Spanish**. This README is in English for documentation purposes only.


---

## 📑 Table of Contents

- [Description](#-description)
- [Site Pages](#-site-pages)
- [Project Structure](#-project-structure)
- [Technologies Used](#-technologies-used)
- [Design and Styling](#-design-and-styling)
- [How to Run](#-how-to-run)
- [Credits and Disclaimer](#-credits-and-disclaimer)

---

## 📖 Description

**YORHA System** is a web layout project built with HTML5 and CSS3, with no frameworks and no JavaScript. Every page shares the same header with a Bunker background image, a fixed navigation bar and a footer with the legal disclaimer, so the whole site looks consistent.

## 🗂️ Site Pages

| Page | File | Content |
|------|------|---------|
| **Home** | `index.html` | Welcome message, YoRHa regulations, an embedded video of the Council of Humanity broadcast, and a side panel with the operational models. |
| **General Calendar** | `Calendario.html` | Table with the Bunker's weekly activity schedule (activation, evaluation, deployment, maintenance, simulations, rest cycles, etc.). |
| **Incident Form** | `Formularios.html` | Form for androids to report incidents: model data, estimated risk, priority and report. |

### Page Details

**🏠 Home**
- Welcome text introducing the platform's functions.
- Regulations as a nested list, with a highlighted reminder about mandatory equipment.
- YouTube video embedded with an `<iframe>`.
- Side panel (`<aside>`) with collapsible sections (`<details>` and `<summary>`) for each operational model, including description and image: **A, B, D, E, G, H, M, O and S**.

**📅 Calendar**
- Table using `colspan` and `rowspan` to represent activity blocks spanning several days or hours.
- Semantic structure with `<thead>`, `<tbody>` and `<tfoot>`.
- The schedule is updated every Sunday at 00:00 (UTC-7).

**📝 Incident Form**
- Fields for email, model (`select`), model number and ID.
- Estimated risk slider (`range`, 0-100).
- Priority radio buttons (low, medium, high, urgent).
- Free-text report and **Submit** / **Reset** buttons.
- Grouped with `<fieldset>` and `<legend>`.

## 📁 Project Structure

```
WEB-NierStaticSite/
│
├── index.html            # Home page
├── Calendario.html       # Weekly calendar
├── Formularios.html      # Incident form
│
├── Css/
│   └── estilos.css       # Single stylesheet for the whole site
│
├── Imágenes/
│   ├── Bunker.png        # Header image
│   ├── ModeloA.jpg
│   ├── ModeloB.png
│   ├── ModeloD.png
│   ├── ModeloG.png
│   ├── Modelo H.jpg
│   ├── ModeloM.png
│   ├── ModeloO.png
│   └── ModeloS.png
│
├── .gitattributes
└── README.md
```

## 🛠️ Technologies Used

- **HTML5**: semantic tags (`header`, `nav`, `main`, `article`, `section`, `aside`, `footer`).
- **CSS3**: tag, class, id and descendant selectors, Flexbox and CSS Grid.
- **Google Fonts**: [Oxanium](https://fonts.google.com/specimen/Oxanium) typeface.
- **Git and GitHub**: version control and repository hosting.

## 🎨 Design and Styling

- **Color palette:** black background and cream tone `rgb(231, 228, 208)`, reminiscent of the NieR: Automata interface.
- **Navigation:** fixed top bar with a *hover* effect (opacity and colors change).
- **Layout:** the home page uses a two-column grid (`3fr 1fr`) for the main content and the side panel.
- **Boxes:** rounded corners and inset shadows (`box-shadow: inset`) on the sections.
- **Table:** double container and alternating row colors for readability.
- **Images:** scaled to the width of their container (`max-width: 100%`) so they don't break the layout.

## 🚀 How to Run

No installation or dependencies required.

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/WEB-NierStaticSite.git
   ```
2. Enter the project folder:
   ```bash
   cd WEB-NierStaticSite
   ```
3. Open `index.html` in your browser, either by double-clicking it or with an extension such as *Live Server* in VS Code.

> ⚠️ An internet connection is required to load the Oxanium font and the YouTube video.

## ✍️ Credits and Disclaimer

- Project developed by **Marina Rodríguez Blázquez** ([@mrb0060](https://github.com/mrb0060)).
- The images and videos used **are not my property**. All rights reserved to **Square Enix** for the official material, and to **SubstantialBreath412** (Reddit) for the *fanmade concept*.
- Non-profit project created for educational purposes.
