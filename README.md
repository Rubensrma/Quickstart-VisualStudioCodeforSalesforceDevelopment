  
  <p align="center">
    <img windth="470" src="https://www.qtrainers.com/upload/topic/700/2019/06/topic-700-37375d0ca3bfed76a.jpg">
</p>
  
  @salesforce
  
  
  
  
  
  
  
  
  
  
  # Use Visual Studio Code for Salesforce development

  **Project👨‍💻**

  # Quickstart: Visual Studio Code for Salesforce development

  Configure and integrate the recommended IDE for Salesforce development.

  **🔗TRAILHEAD👨‍💻:https://trailhead.salesforce.com/pt-BR/content/learn/projects/quickstart-vscode-salesforce**

  **🔗My Trailhead Salesforce profile:https://trailblazer.me/id?lang=pt_BR**

  ### ---------------------------------------------------------------------------------------------------

  In this step, we will explore some of the more advanced features of Visual Studio Code, for example, how to use the integrated terminal and our newly installed Salesforce Extension Pack.

  ## Terminal vs. command palette

  As with any good development tool, there is more than one way to do things with Visual Studio Code. The two main ways to interact with the Salesforce CLI are through the integrated terminal or the quick opening window.

  To display the quick opening window, press **Command + P** on the Mac or **Ctrl + P** on Windows. If you type `?`, you can see the help menu. In this module, we will use the quick opening window in the command palette mode, which allows us to show and execute commands.

  ![The display of global commands in the quick opening window with?  in the field.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/699cad2f3bdb50d80abd33b2e4594e42_cjptzm-66-v-00090-s-89-fljgg-9-bg.png)

  ## Create a project

  1. Press **Command + Shift + P** on Mac or **Ctrl + Shift + P** on Windows to open the command palette.
  2. Make sure the new prompt starts with `>`
  3. Type **SFDX: Create Project** and press **Enter** to select the default model.
  4. Type the name of the project `VSCodeQuickstart`and press **Enter** .
  5. Select your workspace as the place to create the project to make it easier to find later.
  6. Wait for the new Visual Studio Code window to open. You should see an indication that the extension is preparing your project before filling out the file explorer.

  ![Extension notice: Running SFDX: Create Project.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/6ae0230ffbeb9667708db7dd98306ccf_cjptzm-66-x-000-a-0-s-89-cl-09-gz-42.png)

  ## Search your files

  1. Press ** Command + P ** on Mac or **Ctrl + P** on Windows to make the search palette appear. This shifts the focus to searching for files.
  2. Type `project-scratch-def.json`in the field.
  3. Click on the result to open the file.
  4. On the left side of Visual Studio Code, click the Find and Replace menu. ![forget](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/6e008a51c38cc23568fafa4df52c07d6_cjptzm-671000-d-0-s-89-a-9-sh-5-nyf.png)
  5. Search `orgName`.
  6. In the first result found in project-scratch-def.json.
  7. Change the value of orgName (after: and enter “”) to `Learning VS Code`.
  8. Save the file by pressing **Command + S** on the Mac, **Ctrl + S** on Windows.

  ![The project-scratch-def.json file with the new name of the organization.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/f5742acbb1d3d8d4595d56c3aadb4333_cjptzm-673000-e-0-s-89-m-93-o-5-yb-1.png)

  ## Authenticate to your Playground

  1. Press **Command + Shift + P** on Mac or **Ctrl + Shift + P** on Windows to open the command palette.
  2. Type `SFDX: Authorize an Org`.
  3. To accept the default login URL, press **Enter.**
  4. Enter the alias `VSCodePlayground`.
  5. Note that your default browser opens a new Salesforce login window. Log in to your Playground using the Playground username and password retrieved in the last step.
  6. When access to the connected application is requested, click to allow.   ![The Allow access to a global connected application page](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/35b7e9cde25290c50977ea8932aa92c3_cjptzm-674000-f-0-s-89846-lck-3-l.png)
  7. Close the browser window.

  The command line terminal window returns a success message when the transaction is complete.

  ![USER successfully authorized with organization ID / Now you can close the browser.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/e79231bf40a1e2a893b8b22f1c72774b_cjptzm-677000-g-0-s-89-iyreg-3-fa.png)

  ## Create an Apex class

  1. Click the Explorer icon ![explorer icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/a939fa52445b29275826f819a9e29226_cjptzm-679000-h-0-s-89-jq-2-k-3-f-5-r.png)in Visual Studio Code to expand the force-app folder.

  2. In the VSCODEQUICKSTART directory, click **force-app** to show the folder tree. In the force-app / main / default directory, you can find metadata included in the project, such as applications, aura, classes and more.  ![The expanded folder tree so that you can see the class folder.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/5d4d124608fcaeb84ef64b5010208a42_folder-structure-may-2019.png)

  3. Press **Command + Shift + P** on Mac or **Ctrl + Shift + ****P** on Windows to open the command palette.

  4. Type `SFDX: Create Apex Class`.

  5. Enter the name `AccountController`.

  6. If VS Code asks, select **force-app / main / default / classes** as the directory to which you want to add `AccountController.cls`.

  7. In the newly opened AccountController.cls file, replace the standard code with the following:

  8. ```
     public with sharing class AccountController {
       public static List<Account> getAllActiveAccounts() {
         return [SELECT Id,Name,Active__c FROM Account WHERE Active__c = 'Yes'];
       }
     }
     ```

     Copy

  9. Save the file.

  ## Query

  Our new Apex class has a SOQL query in it, but we want to make sure that it works as intended before deploying it to our organization. We use the command palette to run the query against our organization.

  1. In line 3 of the code, highlight the query `SELECT Id,Name,Active__c FROM Account WHERE Active__c = 'Yes’`
  2. Press **Command + Shift + P** on Mac or **Ctrl + Shift + P** on Windows to open the command palette.
  3. Search `SFDX:Execute SOQL Query with Currently Selected Text`.
  4. Press **Enter** .
  5. Select **REST API** and press **Enter** .
  6. On the Output tab of the integrated terminal window, view the results of your query. The window should contain a summary that says: SFDX: Run SOQL Query ... ended with exit code 0. This means that it was executed successfully.

  ![The Output tab showing the 10 records received from your Trailhead Playground.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/4bac25f56b8e74ebf1ee37e96ef4d99e_cjptzm-67-e-000-k-0-s-891-w-0-bp-99-x.png)

  ## Deploy

  The last step is to deploy your code to your Playground using Visual Studio Code.

  1. Right-click the **classes** folder .
     ![With the classes folder right-clicked, SFDX: Deploy Source to Org is selected in the list of options.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/f268c57e0e2c85243117680600e3b641_deploy-00000.png)
  2. Click **SFDX: Deploy Source to Org** .
  3. On the Output tab of the integrated terminal, view the results of your deployment. You should also have received a warning that says: SFDX: Deploy Source to Org ... ended with exit code 0. This means that it ran successfully.

  ![The Output tab showing results with exit code 0 as successful.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/quickstart-vscode-salesforce/use-vscode-for-salesforce/images/pt-BR/3025e4bef52d29ac9439afb6360f6516_cjptzm-67-i-000-m-0-s-896-w-8-q-2-ecx.png)


   # Salesforce Developer#
   
<p align="center">
    <img windth="470" src="https://github.com/Rubensrma/Quickstart-VisualStudioCodeforSalesforceDevelopment/blob/master/img-process/Visual%20Studio%20Code%20for%20Salesforce%20development11.jpeg">
</p>
