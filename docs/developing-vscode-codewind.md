# Play Rogue Cloud using Codewind for VS Code #


## A) Clone the [Rogue Cloud Client](https://github.com/sujeilyfonseca/rogue-cloud-client-codewind) repository into your codewind-workspace directory ##

Codewind creates a folder called `codewind-workspace` within your home directory to contain your projects. In this step we will locate that folder, and then `git clone` the [rogue-cloud-client-codewind](https://github.com/sujeilyfonseca/rogue-cloud-client-codewind) repository in that folder. You can also download the ZIP file. 

1. Determine the location of the **codewind-workspace** directory:
   * **Mac/Linux**: `docker inspect codewind-pfe | grep "HOST_WORKSPACE_DIRECTORY="`
     * Example: `"HOST_WORKSPACE_DIRECTORY=/home/user/codewind/codewind-workspace"` means your workspace can be found in `/home/user/codewind/codewind-workspace`
   * **Windows (Command Prompt)**: `docker inspect codewind-pfe | find "HOST_WORKSPACE_DIRECTORY="`
     * Example: `"HOST_WORKSPACE_DIRECTORY=C:\\codewind-workspace"` means your workspace can be found in `C:\codewind-workspace`
2. From within the `codewind-workspace` directory, clone the **Rogue Cloud Client** repository:
  ```
  cd <path-to-your-codewind-workspace>
  git clone https://github.com/sujeilyfonseca/rogue-cloud-client-codewind.git
  ```
3. Back in VS Code, under the **Codewind** view, right-click on **Projects (Local)** and select **Add Existing Project** 
4. Specify the path of the `rogue-cloud-client-codewind` folder that you cloned from the previous step, then click **Add to Codewind**
5. You will see a brief `Processing...` status message, followed by a `Please confirm the project type` message
   * The Type field should be: `liberty`
   * The Language field should be: `Java`
   * If one or both of these are inaccurate, jump back to step 3 and ensure the correct path is selected
6. Presuming your project is correctly identified, click **Yes**
7. Before the code starts building, the container needs to initialize and download the Java and Maven dependencies for the underlying build system. This can take between 5 to 10 minutes depending on CPU and network connection (this initialization is only required the first time you use the Codewind tools).


## B) Register your player ##
1. In the code editor, press ``CTRL-P`` (Windows) or  ``Command-P`` (Mac), type ``StartAgentServlet.java``, and select ``StartAgentServlet.java``
   * ``CTRL-P/Command-P`` is a great way to quickly find Java classes in VS Code

2) Edit the following fields in `StartAgentServlet.java` to create a new user and password:
```
public static final String USERNAME = "<specify-a-username-here>";
public static final String PASSWORD = "<specify-a-password-here>";
```
   * These values are to ensure that *only you* can access and control your character.
   * The username and password you specify are automatically registered when your code first begins controlling a character on the game map, and they do not have to correspond to an existing email address or account.

3) Press ``CTRL-S`` (Windows) or ``Command-S`` (Mac) to save your changes


## C) Next steps: Watch your agent ##

To watch your agent as it interacts with the game world, right-click on the `rogue-cloud-client-codewind` project in the **Codewind** view and select **Open App**.

Congratulations, your character is now exploring, interacting with the game world, and earning you points on the leaderboard!


## D) Troubleshooting ##
If you obtain a credential (i.e., username/password) error, verify that you have provided a username and password in the StartAgentServlet class. Correct the problem, and then `Stop` and `Start`the server again.
