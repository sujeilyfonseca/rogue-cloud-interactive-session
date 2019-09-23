[![License](https://img.shields.io/badge/License-EPL%202.0-red.svg?label=license&logo=eclipse)](https://www.eclipse.org/legal/epl-2.0/)
[![Build Status](https://ci.eclipse.org/codewind/buildStatus/icon?job=Codewind%2Fcodewind-eclipse%2Fmaster)](https://ci.eclipse.org/codewind/job/Codewind/job/codewind-eclipse/job/master/)
[![Chat](https://img.shields.io/static/v1.svg?label=chat&message=mattermost&color=145dbf)](https://mattermost.eclipse.org/eclipse/channels/eclipse-codewind)

# Codewind for Eclipse #
Create and develop cloud-native, containerized web applications using Eclipse.

## Installing Codewind for Eclipse ##
Prerequisites:
1. Download and install the latest [Eclipse IDE for Java EE Developers](https://www.eclipse.org/downloads/packages/release/) or use an existing installation. The earliest supported version of the Eclipse IDE for Codewind for Eclipse is 4.11.0 (2019-03).
2. Install Docker
3. If you use Linux, you also need to install Docker Compose

Complete the installation:
1. Install [Codewind from the Eclipse Marketplace](https://marketplace.eclipse.org/content/codewind)
   * Click on **Help** > **Eclipse Marketplace...**
   * Search for **Codewind**
   * Click on **Install**
   * Reload the Eclipse IDE
2. Open the **Codewind Explorer** view
   * Click on **Window** > **Show View** > **Other...**
   * Select **Codewind** > **Codewind Explorer**
   * Click on **Open**
3. Double-click the **Codewind** entry in the view to finish installing Codewind (download is approximately 1 GB)

## Using Codewind for Eclipse ##
Right-click the **Local Projects** entry in the view to create new projects or add existing projects to Codewind. After a project is created or added, it displays in the **Codewind Explorer** view. Right-click the project to see the available actions.

Features:
1. Create new projects from application templates or add existing container-ready projects to Codewind.
2. View Codewind projects, including application and build statuses.
3. Debug **Microprofile/Java EE** and **Spring** projects in their containers.
4. Set up a Chrome debug session for **Node.js** projects.
5. View application and build logs in the **Console** view.
6. View and edit project deployment information.
7. Open a shell session into a Codewind application container.
8. Toggle project auto build and manually initiate project builds.
9. Integrate Codewind validation errors into the **Markers** view.
10. Disable, enable, and delete projects.

## Enabling Debug Logs ##
1. Create an `.options` file in your Eclipse install directory, the same directory with the `eclipse` executable. Include the following content in the new file:
```
org.eclipse.codewind.core/debug/info=true
```
2. Launch Eclipse with the `-debug` flag.
3. The logs are written to the Eclipse workspace directory to `.metadata/.log`.
