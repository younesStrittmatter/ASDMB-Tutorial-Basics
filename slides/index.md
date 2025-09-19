---
marp: true
header: SETUP
paginate: true
---
<style> 
    header {
            right: 20px;
            text-align: right;
            font-size: 24pt;
        }

    img {
        display: block;
        margin: 0 auto;
    }
    
    .stroop-overview {
        width: 50%;
    }

    .autora-overview {
        width: 85%;
    }

    .colored {
        background: #222;
        padding: 4pt 12pt;
        font-weight: bold;
        border-radius: 2pt;
    }

    .colored.blue {
        color: blue
    }

    .colored.red {
        color: red
    }

</style>

# ASDMB Tutorial: Basics
> Today: Setting Up The Loop

---

# Content

> [Logistics](#logistics)
> [Overview](#overview-what-are-we-building)
> [Tutorial](#tutorial-setup)

---

## Logistics

- *Earlier* (before 7:00 pm) Tutorials on *Tools*
- *Late* (after 20:00 pm) Tutorials on *AutoRA Integration*
- *Office Hours*: I'm here in front of A32 or in my office, second floor 23.
- *What to do if you get stuck*: [troubleshooting.md](troubleshooting.md) is a guide on how to continue at the start of each tutorial

---


# Overview: What are we building?
> [Study](#study)
> [AutoRA System](#autora-system)

---

## Study

In this example study, we are interested in **cognitive control**. To examine this, we will use a **Stroop Task**, in which participants see color words displayed in different ink colors and must respond to the color rather than the word’s meaning. Performance is compared between *congruent* trials (e.g., the word <span class="colored red">RED</span> shown in red) and *incongruent* trials (e.g., the word <span class="colored blue">RED</span> shown in blue), allowing us to measure accuracy differences that reflect congruency effects.

--- 

<style scoped>
    {
        background-color: black;
    }
</style>

<img src="assets/stroop-overview.gif" alt="stroop-overview" class="stroop-overview"/>

---

<style scoped>
    h2 {
        display: None;
    }
    </style>

## AutoRA System

<img src="assets/system-overview.png" alt="autora-overview" 
class="autora-overview"/>

---

## Tutorial: Setup
> [Prerequisits](#prerequisits)
> [Virtual Environment](#virtual-environment)

---

### Prerequisits

- Google Account (personal with org access)
- GitHub Account

---

<style> 
.github-button {
    padding: 8px 12px;
    border-radius: 4px;
    background: #248536;
    color: white;
}
</style>

### Creating the Repository

1. Go to [https://github.com/younesStrittmatter/ASDMB-Tutorial-Basics](https://github.com/younesStrittmatter/ASDMB-Tutorial-Basics) and use as template. Top-right-corner: <span class="github-button">Use this template ▼</span> → Create a new repository
2. Open the repository in Codespaces: <span class="github-button"><> Code ▼</span> → Codespaces 


---
### Virtual Environment

Create a virtual environment (in the terminal):

```shell
python -m venv .venv
```

Activate the environment:

```shell
source .venv/bin/activate
```

Add .gitignore to root folder with entry .venv:
```file
.venv
```

---
### Cookiecutter: Set Up

Install cookiecutter
```shell
pip install cookiecutter
```

Use cookiecutter to set up the project
```shell
cookiecutter https://github.com/AutoResearch/autora-user-cookiecutter
```

alternative:
```shell
python -m cookiecutter https://github.com/AutoResearch/autora-user-cookiecutter
```

---

Cookiecutter: Configuration

- Give your project a name (short, no special characters)
- [?] Do you want to use advanced features?: > yes
- [?] Do you want to install theorists: no theorist (continue)
- [?] Do you want to install experimentalists: no experimentalist (continue)
- [?] Do you want to install experiment-runners: select `[X] autora[experiment-runner-firebase-prolific]` with the spacebar
- [?] Do you want to set up a firebase experiment? (ATTENTION: Node is required for this feature): > yes
- If asked, install the packages (write `y` and continue)

---

- [?] What type of project do you want to create?: > Double Sweet
- Enter your Firebase project ID: Can be same as project name
- ? Enable Gemini in Firebase features? (Y/n) -> `n`
- ? Allow Firebase to collect CLI and Emulator Suite usage and error reporting information? `n` (or Y if you like to)
- Copy the url, login and get the authorization code






