# Rigel Automation
This app is designed for automated E2E testing on real MTR devices. 

## Prerequisites
To be able to build & run this app from this repository, you must first prepare and install the following:
1. **Machine Setup**. Follow this [guidance](https://domoreexp.visualstudio.com/Teamspace/_wiki/wikis/Teamspace.wiki/222/Machine-Setup) on basic setup of local development environment, including Git and Package Manager.
2. **IDE**. Any choice of code editor would work, but we recommend [VS Code](https://code.visualstudio.com/) here as it supports extra features via various plugins.
3. **Node.js**. This project relies on version >=18.0.0. We recommend [nvm](https://github.com/coreybutler/nvm-windows) for convenience of switching node version between this repository and your other projects, if necessary.
4. **Yarn**. Install it globally via npm command.
5. **[Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)** + **[DevOps extension](https://docs.microsoft.com/en-us/azure/devops/cli/?view=azure-devops)**. Required for accessing scoped artifactory.
6. **.npmrc**. Follow the instructions [here to set up a 90 day token](https://domoreexp.visualstudio.com/Teamspace/_wiki/wikis/Teamspace.wiki/36827/NPM-and-Yarn-Authentication?anchor=(recommended!)-setting-up-your-.npmrc-manually).
7. **Micrsoft Teams Rooms**. Either standalone device, [UWP package](https://skype.visualstudio.com/SBS/_git/client_sfb_rigel?path=%2FREADME.md&_a=preview) installed locally or [Rigel Self-Service](https://aka.ms/rigel-self-service) would work. **You need to follow this [guidance](https://domoreexp.visualstudio.com/Teamspace/_wiki/wikis/Teamspace.wiki/43663/2-Enable-MTR-Debugging-Port) to enable remote debugging port.**

## Getting Started
The instructions below will get you set up for coding:

To fetch this repository, run the following command within your preferred local directory.
```
git clone https://domoreexp.visualstudio.com/DefaultCollection/Teamspace/_git/teams-client-platform-mtr
```

To install package dependencies, run the following command within this repository.
```
yarn install
```

To launch this app locally, run the following command within this repository.
```
yarn dev
```

Instructions explaining how to use this app can be found [here](https://domoreexp.visualstudio.com/Teamspace/_wiki/wikis/Teamspace.wiki/43666/3-Launch-Automation-App).

## Local Build
To build an executable binary locally with your changes, simply run the following command within this repository, and you'll get a binary file named `automation.exe` under the path `<repository>/dist/bin`  
```
yarn build:ci
```

If you need a prod build, follow this [guidance](https://domoreexp.visualstudio.com/Teamspace/_wiki/wikis/Teamspace.wiki/43664/1-Get-Executable-Build) to download versioned packages from CI pipeline.

## Other Useful Commands
|         Command        |               Usage                 |
| ---------------------- | ----------------------------------- |
| `yarn lint:fix`        | Check and auto-fix linter error     |
| `yarn prettier`        | Format code file                    |

## Contributing
All the documentation explaining the dev design and other details can be found under this [wiki](https://domoreexp.visualstudio.com/Teamspace/_wiki/wikis/Teamspace.wiki/38400/Rigel-Automation).