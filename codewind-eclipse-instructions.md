# Codewind for Eclipse

[![License](https://img.shields.io/badge/License-EPL%202.0-red.svg?label=license&logo=eclipse)](https://www.eclipse.org/legal/epl-2.0/)
[![Build Status](https://ci.eclipse.org/codewind/buildStatus/icon?job=Codewind%2Fcodewind-eclipse%2Fmaster)](https://ci.eclipse.org/codewind/job/Codewind/job/codewind-eclipse/job/master/)
[![Chat](https://img.shields.io/static/v1.svg?label=chat&message=mattermost&color=145dbf)](https://mattermost.eclipse.org/eclipse/channels/eclipse-codewind)

## Installing Codewind for Eclipse
Prerequisites
- Download and install the latest [Eclipse IDE for Java EE Developers](https://www.eclipse.org/downloads/packages/release/) or use an existing installation. The earliest supported version of the Eclipse IDE for Codewind for Eclipse is 4.11.0 (2019-03).
- Install Docker.
- If you use Linux, you also need to install Docker Compose.

Complete the installation:
1. Install [Codewind from the Eclipse Marketplace](https://marketplace.eclipse.org/content/codewind).
2. Open the **Codewind Explorer** view.
3. Double-click the **Codewind** entry in the view to finish installing Codewind. The download is approximately 1 GB. For more information, see [Installing Codewind for Eclipse](https://www.eclipse.org/codewind/mdteclipseinstallinfo.html).

## Using Codewind for Eclipse
Right-click the **Local Projects** entry in the view to create new projects or add existing projects to Codewind. After a project is created or added, it displays in the **Codewind Explorer** view. Right-click the project to see the available actions.

Features:</br>
- Create new projects from application templates or add existing container-ready projects to Codewind.
- View Codewind projects, including application and build statuses.
- Debug **Microprofile/Java EE** and **Spring** projects in their containers.
- Set up a Chrome debug session for **Node.js** projects.
- View application and build logs in the **Console** view.
- View and edit project deployment information.
- Open a shell session into a Codewind application container.
- Toggle project auto build and manually initiate project builds.
- Integrate Codewind validation errors into the **Markers** view.
- Disable, enable, and remove projects.

## Enabling debug logs
1. Create an `.options` file in your Eclipse install directory, the same directory with the `eclipse` executable. Include the following content in the new file:
```
org.eclipse.codewind.core/debug/info=true
```
2. Launch Eclipse with the `-debug` flag.
3. The logs are written to the Eclipse workspace directory to `.metadata/.log`.
