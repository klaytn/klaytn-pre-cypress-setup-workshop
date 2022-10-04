# Klaytn Workshop - Pre Cypress Setup

![Klaytn Docs](https://raw.githubusercontent.com/trakim/pre/main/static/images/klaytn.png)

## Index
  - [Overview](#overview) 
  - [Getting Started](#getting-started)
  - [Contributing](#contributing)
<!--  Other options to write Readme
  - [Deployment](#deployment)
  - [Used or Referenced Projects](Used-or-Referenced-Projects)
-->

## Overview
<!-- Write Overview about this project -->
**If you want to join Klaytn Baobab network, this workshop will be the best guidance. Below are included in this workshop.**
- Prerequisites (Firewall & Package Installation)
- Chaindata Fast sync with Baobab
- Baobab Network Configuration
- Service Status Management

## How this repository works
**Hugo and GitHub are utilized for generating this workshop.**
### [Hugo](https://gohugo.io/about/) - Static Site Generator
**Hugo** is used for scaffolding and generating this workshop.
### GitHub
1. **GitHub Repository**: stores the source code of Hugo.
2. **GitHub Action**: automatically build and deploy your contents to the branch **gh-pages**.
3. **GItHub Pages**: hosts the output to public.

## Contributing
<!-- Write the way to contribute -->
Thank you for your interest in contributing to Klaytn Workshop. Klaytn Workshop is always open to anyone and we welcome your contribution. 
### How to contribute on Klaytn Workshop
1. Site scaffolding
```
.
├── README.md
├── archetypes
├── config
├── content    ====> Where contents can be updated.(Markdown)
├── data
├── layouts
├── resources
├── static
└── themes
```
2. Labaeling - [issue|typo|update|new]
3. Branch Naming when PR - hubo/update-3-b, hugo/new-3-c 
