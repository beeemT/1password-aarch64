<a name="readme-top"></a>


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]


<!-- ABOUT THE PROJECT -->
## About The Project

1Password (btw awesome password manager) currently only supplies a download + script install version for linux on arm64. So here is a slightly adjusted PKGBUILD which allows installing with the usual makepkg commands. As soon as 1Password integrates this into their official package this repository will be archived.

All credits go to 1Password, after all it is their product and I just slightly adjusted their package to easily be installed on Apple Silicon linux laptops.

[Here](https://support.1password.com/install-linux/) is a link to the official 'manual' install guide.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

* GPG needs to trust their code signing keys
  ```sh
  curl -sS https://downloads.1password.com/linux/keys/1password.asc | gpg --import
  ```

### Installation

1. Clone this repository
   ```sh
   git clone https://github.com/beeemT/1password-aarch64.git
   ```
3. Install with makepkg
   ```sh
   cd 1Password-aarch64 && makepkg -sic
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Just start 1Password as you would normally.

_For more examples, please refer to the [Documentation](https://support.1password.com/)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [1Password](https://1password.com)
* [othneildrew's Readme template](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge