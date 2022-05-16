# TestComplete - Library Setup

> The purpose of this package is standing only for documentation.

When the library is available on **npmjs**,
you can easily get it with the following command
if **nodejs** is installed on your computer.

I advise to install **nodejs**, because it will greatly help
for getting the dependencies. Without **nodejs**, you will have to 
pull sources from the repository by yourself.

You have to open a command line interface to type the following command.
If you have **Bash** (**Git BASH**) installed on your system, prefers it. Else
use the Windows Command Line **cmd.exe** :

* Windows : [10 Ways to Open the Command Prompt in Windows 10 ](https://www.howtogeek.com/235101/10-ways-to-open-the-command-prompt-in-windows-10/)
* Git BASH : [Git BASH](https://gitforwindows.org/)
* Cygwin : [Cygwin](https://www.cygwin.com/)
* MinGW : [MinGW](https://www.mingw-w64.org/)

Depending of the architecture of your whole NRT project,
I advise you to create in your **TestComplete** project,
a separate & dedicated folder which will receive libraries scripts.

I you envisage to create many **TestComplete** projects (standalone),
maybe you have to consider to create a shared network folder
where path will be absolute.

Once the folder is created, open the command line and browse into it.
Then type the following command.

````bash
npm install @testcomplete/<packageName>
````

Where ``<packageName>`` is the package of scope ``@testcomplete``.
If the package has not a scope, remove ``@testcomplete/`` (or replace
for another scope).

**npm** installs the package with it dependencies locally in the folder
where you type the command.

![NPM Install Library](docs/img/npm_install.png)

In **TestComplete**, you will have to add all files (Library & Dependencies)
to your project to be able **require** them in your scripts.

For package of scope `@testcomplete`,
file are specified in the library documentation.

Example for **ExcelHandler** :

* [Dependency] : ``./node_modules/@neooblaster/tablejs/Bin/Table.js``
* [Package] : ``./node_modules/@testcomplete/excelhandler/ExcelHandler.js``

![Add existing script in TestComplete](docs/img/tc_add_script.png)

![Add existing script in TestComplete](docs/img/tc_add_script_select_script.png)

![Add existing script in TestComplete](docs/img/tc_add_script_added.png)

Once files (Library and its dependencies) are added in **TestComplete**,
now you are able to required the library in any scripts.

**Note** : You can see a little black arrow on each script indicating the script is
in reference of and so not owned by the project.

**Important** : In date of 10/05/2022 (TC 14 & 15), 
adding scripts in your script folder **WILL NOT BE** appended
to your **TestComplete** project.
So you will have to manually add scripts (for each project).

![Requiring ExcelHandler](docs/img/tc_required_excelhandler.png)

You do have to require dependencies, because
the library does itself.
This rule is true for all libraries and their dependencies.
