# Development Environment Setup Guide

This guide will help you set up the development environment for block development on macOS, Windows, and Ubuntu.

## Prerequisites
Before starting, ensure you have the following:
- A stable internet connection
- Administrator rights on your device

## 1. macOS Setup

### Install Homebrew
Homebrew is a package manager for macOS.
<code>/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</code>

### Install Node.js and npm
<code>brew install node</code>

### Install Git
<code>brew install git</code>

### Install Visual Studio Code
Download and install [Visual Studio Code](https://code.visualstudio.com/).

### Clone the GitHub Repository
Open Terminal and run:
<code>git clone https://github.com/your-repo/your-project.git</code>
<code>cd your-project</code>

### Install Project Dependencies
<code>npm install</code>

### Start the Development Server
<code>npm start</code>

## 2. Windows Setup

### Install Node.js and npm
Download and install Node.js from the [official website](https://nodejs.org/).

### Install Git
Download and install Git from the [official website](https://git-scm.com/).

### Install Visual Studio Code
Download and install [Visual Studio Code](https://code.visualstudio.com/).

### Clone the GitHub Repository
Open Git Bash and run:
<code>git clone https://github.com/your-repo/your-project.git</code>
<code>cd your-project</code>

### Install Project Dependencies
<code>npm install</code>

### Start the Development Server
<code>npm start</code>

## 3. Ubuntu Setup

### Update Package List
<code>sudo apt update</code>

### Install Node.js and npm
<code>sudo apt install nodejs npm</code>

### Install Git
<code>sudo apt install git</code>

### Install Visual Studio Code
Download and install the .deb package from the [Visual Studio Code website](https://code.visualstudio.com/).
<code>sudo apt install ./<path-to-downloaded-file>.deb</code>

### Clone the GitHub Repository
Open Terminal and run:
<code>git clone https://github.com/your-repo/your-project.git</code>
<code>cd your-project</code>

### Install Project Dependencies
<code>npm install</code>

### Start the Development Server
<code>npm start</code>

## Common Steps for All Operating Systems

### Setting Up GitHub SSH Key (Optional but Recommended)

#### Generate SSH Key
Open Terminal (or Git Bash on Windows) and run:
<code>ssh-keygen -t rsa -b 4096 -C "your_email@example.com"</code>

#### Add SSH Key to GitHub
Copy the SSH key to your clipboard:
<code>pbcopy < ~/.ssh/id_rsa.pub  # macOS</code>
<code>cat ~/.ssh/id_rsa.pub | clip  # Windows</code>
<code>xclip -sel clip < ~/.ssh/id_rsa.pub  # Ubuntu (install xclip if not available)</code>

Go to your GitHub account settings, navigate to SSH and GPG keys, and add the new SSH key.

#### Clone Repository Using SSH
<code>git clone git@github.com:your-repo/your-project.git</code>
<code>cd your-project</code>

### Installing Additional Tools

#### ESLint (for code quality)
<code>npm install eslint --save-dev</code>
<code>npx eslint --init</code>

#### Prettier (for code formatting)
<code>npm install prettier --save-dev</code>
<code>echo {}> .prettierrc</code>

#### Running Lint and Prettier
Add the following scripts to your `package.json`:
<code>
"scripts": {
    "lint": "eslint '**/*.js'",
    "format": "prettier --write '**/*.js'"
}
</code>

Run the linting and formatting scripts:
<code>npm run lint</code>
<code>npm run format</code>

By following these steps, you will have a fully functional development environment for block development on macOS, Windows, and Ubuntu. This setup includes Node.js, npm, Git, and Visual Studio Code, and provides instructions for cloning a repository and starting the development server.
