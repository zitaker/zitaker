### Hi there 👋

<h3 align="center">An example of how I write code.</h3>

```python
"""
This module defines classes related to personal information and attributes.

It contains the following classes:
1. AboutMe:
   A class representing general personal hobbies and interests, including
   a love for traveling, sports, and martial arts. It logs this information
   when an object is instantiated.

2. AttributesInfo:
   A subclass of AboutMe that extends the functionality by providing
   additional personal attributes, including contact information, knowledge
   of languages and programming skills.

Classes:
- AboutMe: Logs personal information and hobbies.
- AttributesInfo: Contains information about me and adds personal contact
  information, the languages I speak, age, and programming skills.

Methods:
- AttributesInfo.contact: Returns personal contact information.
- AttributesInfo.life: Returns the languages I speak and my age.
- AttributesInfo.coding: Returns programming skills.

The logging level is set to INFO, so personal hobbies and interests are
logged when an object is created.
"""

import logging

from typing import Tuple, List, Dict

logging.basicConfig(level=logging.INFO)


class AboutMe:
    """Class representing personal information and hobbies."""

    def __init__(self):
        """Registers personal hobbies and interests."""

        logging.info("I love traveling, outdoor activities and sports.")
        logging.info("I was engaged in rowing, I am fond of martial arts.")


class AttributesInfo(AboutMe):
    """
    Class that inherits from AboutMe and adds additional personal attributes.
    """

    @property
    def contact(self) -> Tuple[str, str, str, str, str, str, str]:
        """
        Retrieves personal contact information.

        Returns:
            Contact details.
        """

        whatsapp = "https://wa.me/79601589492"
        telegram = "https://t.me/Georg_Dryndin"
        linkedin = "https://www.linkedin.com/in/georg-dryndin-3a098b257"
        hexlet = "https://ru.hexlet.io/u/user-1bdf7d03342d857f"
        email = "georbearwolf@gmail.com"
        telephone = "+79601589492"
        gitlab = "https://gitlab.basealt.space/dryndinga"

        return whatsapp, telegram, linkedin, hexlet, email, telephone, gitlab

    @property
    def life(self) -> Tuple[List[str], int]:
        """Retrieves information about the languages I speak and my age."""

        languages = ["English", "Russian"]
        age = 27

        return languages, age

    @property
    def coding(self) -> Dict[str, str]:
        """Retrieves information about programming skills."""

        return {"junior/middle": "python"}
```

<!--
сайт для поиска виджетов https://simpleicons.org/?q=Actions
как реализовать виджет https://the-unl.com/kak-oformit-profil-na-github-s-pomoshchyu-github-profile-readme-21
https://img.shields.io/badge/<LABEL>-<MESSAGE>-<COLOR>

**zitaker/zitaker** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
## And here's what I already know
![Python](https://img.shields.io/badge/Python-333333?style=for-the-bardge&logo=Python)
![Docker](https://img.shields.io/badge/Docker-333333?style=for-the-bardge&logo=docker)
![Django](https://img.shields.io/badge/Django-333333?style=for-the-bardge&logo=django)
![Flask](https://img.shields.io/badge/Flask-333333?style=for-the-bardge&logo=flask)
![FastAPI](https://img.shields.io/badge/FastAPI-333333?style=for-the-bardge&logo=FastAPI)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-333333?style=for-the-bardge&logo=postgresql)
![Redis](https://img.shields.io/badge/Redis-333333?style=for-the-bardge&logo=Redis)
![Git](https://img.shields.io/badge/Git-333333?style=for-the-bardge&logo=git)
![GithubActions](https://img.shields.io/badge/GithubActions(CI/CD)-333333?style=for-the-bardge&logo=githubactions)
![Bash](https://img.shields.io/badge/Bash-333333?style=for-the-bardge&logo=gnubash)
![Poetry](https://img.shields.io/badge/Poetry-333333?style=for-the-bardge&logo=Poetry)
![PyTest](https://img.shields.io/badge/PyTest-333333?style=for-the-bardge&logo=pytest)
![Flake8](https://img.shields.io/badge/Flake8-333333?style=for-the-bardge&logo=Python)
![CodeClimate](https://img.shields.io/badge/CodeClimate-333333?style=for-the-bardge&logo=codeclimate)
![HTML](https://img.shields.io/badge/HTML-333333?style=for-the-bardge&logo=html5)
![CSS](https://img.shields.io/badge/CSS-333333?style=for-the-bardge&logo=css3)
![Bootstrap](https://img.shields.io/badge/Bootstrap-333333?style=for-the-bardge&logo=bootstrap)
![uml](https://img.shields.io/badge/UML-333333?style=for-the-bardge&logo=uml)
