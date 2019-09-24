# Play Rogue Cloud using Codewind for Eclipse #


## A) Clone the [Rogue Cloud Client](https://github.com/sujeilyfonseca/rogue-cloud-client-codewind) repository into your codewind-workspace directory ##

Codewind creates a folder called `codewind-workspace` within your home directory to contain your projects. In this step we will locate that folder, and then `git clone` the [rogue-cloud-client-codewind](https://github.com/sujeilyfonseca/rogue-cloud-client-codewind) repository in that folder. You can also download the ZIP file. 

1. Determine the location of the **codewind-workspace** directory:
   * **Mac/Linux**: `docker inspect codewind-pfe | grep "HOST_WORKSPACE_DIRECTORY="`
     * Example: `"HOST_WORKSPACE_DIRECTORY=/home/user/codewind/codewind-workspace"` means your workspace can be found in `/home/user/codewind/codewind-workspace`
   * **Windows**: `docker inspect codewind-pfe | find "HOST_WORKSPACE_DIRECTORY="`
     * Example: `"HOST_WORKSPACE_DIRECTORY=C:\codewind-workspace"` means your workspace can be found in `C:\codewind-workspace`
2. From within the `codewind-workspace` directory, clone the **Rogue Cloud Client** repository:
  ```
  cd <path-to-your-codewind-workspace>
  git clone https://github.com/sujeilyfonseca/rogue-cloud-client-codewind.git
  ```
3. Import the project into Eclipse: 
   * Select **File** (menubar item) > **Import...** 
   * In the dialog, select **Maven** (tree item) > **Existing Maven Projects**, and click **Next >**
   * Search for your `<path-to-your-codewind-workspace>/rogue-cloud-client-codewind` using **Browse...**
   * Click on **Open** > **Finish**
4. Right-click on **Codewind** > **Projects (Local)** and select **Add Existing Project...**
5. `gameclient` or `rogue-cloud-client-codewind` should appear in the checkbox list, select it (if not already selected) and click **Next >**
6. Select `MicroProfile / Java EE` (if not already selected) and click **Finish**
7. Before the code starts building, the container needs to initialize and download the Java and Maven dependencies for the underlying build system. This can take between 5 to 10 minutes depending on CPU and network connection (this initialization is only required the first time you use MicroProfile with the Codewind tools). 

## B) Register your player ##
1. In the code editor, press ``CTRL-SHIFT-R`` (Windows) or ``Command-Shift-R`` (Mac), type ``StartAgentServlet.java``, and select ``StartAgentServlet.java``
   * ``CTRL-SHIFT-R/Command-Shift-R`` is a great way to quickly find Java classes in Eclipse

2. Edit the following fields in `StartAgentServlet.java` to create a new user and password:
```
public static final String USERNAME = "<specify-a-username-here>";
public static final String PASSWORD = "<specify-a-password-here>";
```
   * These values are to ensure that *only you* can access and control your character.
   * The username and password you specify are automatically registered when your code first begins controlling a character on the game map, and they do not have to correspond to an existing email address or account.
   
3. Press ``CTRL-S`` (Windows) or ``Command-S`` (Mac) to save your changes


## C) Next steps: Watch your agent ##
 
To watch your agent as it interacts with the game world, right-click on the `gameclient` project in the **Codewind Explorer** view and select **Open Application**.

**Note**: If you are on Windows, you will need to copy-paste the URL into an external browser (Chrome, Firefox, Edge) because Eclipse's internal browser uses IE11 (an unsupported browser).

Congratulations, your character is now exploring, interacting with the game world, and earning you points on the leaderboard!


## D) Troubleshooting ##
If you obtain a credential (i.e., username/password) error, verify that you have provided a username and password in the StartAgentServlet class. Correct the problem, and then `Stop` and `Start`the server again.
