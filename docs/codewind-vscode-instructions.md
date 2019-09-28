[![Marketplace](https://img.shields.io/vscode-marketplace/v/IBM.codewind.svg?label=marketplace&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=IBM.codewind)
[![License](https://img.shields.io/badge/License-EPL%202.0-red.svg?label=license&logo=eclipse)](https://www.eclipse.org/legal/epl-2.0/)
[![Build Status](https://ci.eclipse.org/codewind/buildStatus/icon?job=Codewind%2Fcodewind-vscode%2Fmaster)](https://ci.eclipse.org/codewind/job/Codewind/job/codewind-vscode/job/master/)
[![Chat](https://img.shields.io/static/v1.svg?label=chat&message=mattermost&color=145dbf)](https://mattermost.eclipse.org/eclipse/channels/eclipse-codewind)

# Codewind for VS Code
Create and develop cloud-native, containerized web applications using VS Code.

## Installing Codewind
Prerequisites:
- Install [VS Code](https://code.visualstudio.com/download)
- Install Docker
- If you use Linux, you also need to install Docker Compose.

Complete the installation:
1. Find Codewind for VS Code in the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=IBM.codewind) or by searching for `Codewind` in the [Extensions View](https://code.visualstudio.com/docs/editor/extension-gallery#_browse-for-extensions).
2. Open the **Codewind** view in the **Explorer** view group or enter `Focus on Codewind View` into the [Command Palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette). If you do not see the Codewind view in either the **Explorer View** or the **Command Palette**, the extension did not install correctly.
3. Please verify that Docker is running on your computer before continuing with the following step. To start Docker, open the application and enter your account.
4. Codewind requires the installation of additional Docker images to run. Choose **Install** when prompted to complete the installation. The installation may take a few minutes to complete. Codewind creates a folder called `codewind-workspace` within your home directory to contain your projects. On Windows, this is the `C:\codewind-workspace` directory. When the installation is complete, you can open the `codewind-workspace` folder or a project within the workspace as your VS Code workspace. The tools offer to open the workspace for you if it’s not open already.

## Using Codewind for VS Code
To see the actions available, open the [Command Palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette) and type `Codewind`.</br>

Features:
1. Create new projects from application templates or import existing container-ready projects.
2. View Codewind projects, including application and build statuses.
3. Debug **Microprofile/Java EE**, **Spring**, and **Node.js** projects in their containers.
4. View application and build logs in the **Output** view.
5. View and edit project deployment information.
6. Open a shell session into a Codewind application container.
7. Toggle project auto build and manually initiate project builds.
8. Disable, enable, and delete projects.
