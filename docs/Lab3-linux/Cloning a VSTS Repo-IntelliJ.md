## IntelliJ - Working with Git

In this exercise, you are going to open the MyShuttle2 repo from your VSTS account in your VM for editing in IntelliJ.
This exercise assumes you have completed Exercise 1, have created a Team Project that uses Git for version control, and imported the MyShuttle2 GitHub repo into your team project. This exercise uses a team project named **jdev**, though your team project name may differ.

Connect to VSTS from IntelliJ
-----------------------------

1. Click on the IntelliJ icon in the toolbar to open IntellJ IDEA.

    ![Click IntelliJ in the Toolbar](media/intellij-git/click-intellij.png "Click IntelliJ in the Toolbar")

1. The first time you run IntelliJ, it will prompt for IntelliJ settings and theme settings. Click on "Do not import settings," then click on "Skip All and Set Defaults" to use the defaults.

    ![Accept the default IntelliJ theme](media/intellij-git/intellij-defaults.png "Accept the default IntelliJ theme")

1. When the Welcome dialog appears, click Configure and then select Plugins.

    ![Click on Configure to configure Plugins](media/intellij-git/intellij-config-plugins.png "Click on Configure to configure Plugins")

1. In the search box type `visual studio team services` and click the "Search in repositories" link in the main window.

    ![Search for the VSTS plugin](media/intellij-git/intellij-search-vsts.png "Search for the VSTS plugin")

1. Click install to install the extension. The install button will change to a "Restart" button - click it to restart IntelliJ.

    ![Install the plugin and restart IntelliJ](media/intellij-git/intellij-click-install.png "Install the plugin and restart IntelliJ")

1. When IntelliJ restarts, the Welcome dialog will appear again. Click "Check out from Version Control" and select "Team Services Git".

    ![Checkout from Team Services Git](media/intellij-git/intellij-open-from-vsts.png "Checkout from Team Services Git")

1. Click on "Sign in..." to sign in to your VSTS account.

    ![Sign in to VSTS](media/intellij-git/intellij-vsts-signin.png "Sign in to VSTS")

Clone MyShuttle2 from VSTS with IntelliJ
-----------------------------

1. Once you have authenticated, enter "MyShuttle2" into the search bar and select the MyShuttle2 repo from your team project. Click the Clone button to clone the repo to the VM.

    ![Select the VSTS repo](media/intellij-git/intellij-select-repo.png "Select the VSTS repo")

1. IntelliJ detects a Maven project file (pom.xml) and asks if you want to open it. Click "Yes" to open the project. You can dismiss the Tip of the Day dialog that appears.

1. Press "Alt-1" to open the Project View.
1. Expand `src\main\java\com.microsoft.example` and click on "DataAccess" to open the DataAccess class.
1. A yellow warning appears in the main editor window prompting you to "Setup SDK". Click on the link.

    ![Setup the JDK for the project](media/intellij-git/intellij-setup-sdk.png "Setup the JDK for the project")

1. In the Select Project SDK dialog, click "Configure..."

    ![Click on Configure](media/intellij-git/intellij-jdk-configure.png "Click on Configure")

1. In the upper left, click the green "+" icon to add a new SDK.

    ![Add an SDK](media/intellij-git/intellij-add-sdk.png "Add an SDK")

1. Select `java-8-openjdk-amd64` from the folder list and click OK. Click OK back through the rest of the dialogs.

    ![Select the SDK folder](media/intellij-git/intellij-select-sdk.png "Select the SDK folder")

> **Note**: The project will not currently compile, since it has a dependency on a library (MyShuttleCalc) that it cannot resolve. You will fix this in the Package Management lab.

Clone MyShuttleCalc from VSTS with IntelliJ
-----------------------------

1. While the MyShuttle2 project is open in IntelliJ, in the toolbar at the top of IntelliJ, select File -> New -> Project from Version Control -> Team Services Git. 

    ![New Team Services Git project](media/intellij-git/intellij-new-myshuttlecalc-project.png "New Team Services Git project")
    
1. Enter "MyShuttleCalc" into the search bar and select the MyShuttleCalc repo from your team project. Click the Clone button to clone the repo to the VM.
    
    ![Clone the MyShuttleCalc repo](media/intellij-git/intellij-clone-myshuttlecalc.png "Clone the MyShuttleCalc repo")
    
1. IntelliJ will prompt to open the project in the same or a new window. Choose "New Window" to open another instance of IntelliJ with the MyShuttleCalc project. 

    ![New window](media/intellij-git/intellij-new-window.png "New window")

1. IntelliJ should open in a new instance with the project loaded. 

    ![MyShuttleCalc](media/intellij-git/intellij-myshuttlecalc.png "MyShuttleCalc")
