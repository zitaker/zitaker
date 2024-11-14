### Hi there 👋

<h3 align="center">An example of how I write code.</h3>

```python
"""
This module defines classes related to personal information and attributes.

Classes:
   - AboutMe: Logs general personal hobbies and interests.
   - AttributesInfo: Extends AboutMe with additional personal details, such as
     contact information, spoken languages, age, and programming skills.

Attributes:
   - AttributesInfo.contact: Returns contact information.
   - AttributesInfo.life: Returns a tuple of languages spoken and age.
   - AttributesInfo.coding: Returns programming skills.

Logging:
   - The logging level is set to INFO. When an AboutMe object is instantiated,
     personal hobbies and interests are logged.

Tests:
   - Tests verifying data types:
       - test_attributes_info_contact_type.
       - test_attributes_info_life_type.
       - test_attributes_info_coding_type.

   - Tests verifying correctness of values:
       - test_about_me_logging.
       - test_attributes_info_contact.
       - test_attributes_info_life.
       - test_attributes_info_coding.
"""

import logging

from typing import Tuple

import pytest

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
    def contact(self) -> dict:
        """
        Retrieves personal contact information.

        Returns:
            Contact details.
        """

        return {
            "whatsapp": "https://wa.me/79601589492",
            "telegram": "https://t.me/Georg_Dryndin",
            "gitlab": "https://gitlab.basealt.space/dryndinga",
            "linkedin": "https://www.linkedin.com/in/georg-dryndin-3a098b257",
            "hexlet": "https://ru.hexlet.io/u/user-1bdf7d03342d857f",
            "telephone": "+79601589492",
            "email": "georbearwolf@gmail.com",
        }

    @property
    def life(self) -> Tuple[list[str], int]:
        """Retrieves information about the languages I speak and my age."""

        languages = ["English", "Russian"]
        age = 27

        return languages, age

    @property
    def coding(self) -> dict:
        """Retrieves information about programming skills."""

        return {"junior/middle": "python"}


def test_attributes_info_contact_type() -> None:
    """
    Test that the `contact` property in `AttributesInfo` returns a dictionary.

    Asserts:
        The `contact` property returns a dict.
    """
    attributes_info = AttributesInfo()
    assert isinstance(attributes_info.contact, dict)


def test_attributes_info_life_type() -> None:
    """
    Test that the `life` property in `AttributesInfo` returns a tuple where
    the first element is a list of strings and the second element is an int.

    Asserts:
        - The `life` property returns a tuple.
        - The first element in the tuple is a list of strings.
        - The second element in the tuple is an int.
    """
    attributes_info = AttributesInfo()
    life_data = attributes_info.life
    assert isinstance(life_data, tuple)
    assert isinstance(life_data[0], list)
    assert all(isinstance(lang, str) for lang in life_data[0])
    assert isinstance(life_data[1], int)


def test_attributes_info_coding_type() -> None:
    """
    Test that the `coding` property in `AttributesInfo` returns a dictionary.

    Asserts:
        The `coding` property returns a dict with string values.
    """
    attributes_info = AttributesInfo()
    assert isinstance(attributes_info.coding, dict)
    assert all(
        isinstance(level, str) for level in attributes_info.coding.values()
    )


def test_about_me_logging(caplog: pytest.LogCaptureFixture) -> None:
    """
    Test that the `AboutMe` class logs messages about hobbies and interests
    on initialization.

    Args:
        caplog (pytest.LogCaptureFixture): Fixture for capturing log messages.

    Asserts:
        - Log message about traveling, outdoor activities, and sports.
        - Log message about rowing and martial arts.
    """
    with caplog.at_level(logging.INFO):
        AboutMe()
    assert "I love traveling, outdoor activities and sports." in caplog.text
    assert "I was engaged in rowing, I am fond of martial arts." in caplog.text


def test_attributes_info_contact() -> None:
    """
    Test that the `contact` property in `AttributesInfo` returns expected
    contact information.

    Asserts:
        The `contact` property returns a dictionary with specific key-value
        pairs.
    """
    attributes_info = AttributesInfo()
    expected_contact = {
        "whatsapp": "https://wa.me/79601589492",
        "telegram": "https://t.me/Georg_Dryndin",
        "gitlab": "https://gitlab.basealt.space/dryndinga",
        "linkedin": "https://www.linkedin.com/in/georg-dryndin-3a098b257",
        "hexlet": "https://ru.hexlet.io/u/user-1bdf7d03342d857f",
        "telephone": "+79601589492",
        "email": "georbearwolf@gmail.com",
    }
    assert attributes_info.contact == expected_contact


def test_attributes_info_life() -> None:
    """
    Test that the `life` property in `AttributesInfo` returns expected
    languages and age.

    Asserts:
        - The `life` property returns a list with specific languages.
        - The `life` property returns the expected age.
    """
    attributes_info = AttributesInfo()
    languages, age = attributes_info.life
    assert languages == ["English", "Russian"]
    assert age == 27


def test_attributes_info_coding() -> None:
    """
    Test that the `coding` property in `AttributesInfo` returns expected
    programming skills.

    Asserts:
        The `coding` property returns a dictionary with specific key-value
        pairs.
    """
    attributes_info = AttributesInfo()
    expected_coding = {"junior/middle": "python"}
    assert attributes_info.coding == expected_coding
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
