# ExtJs-Resharper-Conflict
Issues with Resharper JavaScript Code Completion and Sencha Ext JS Plugin

Requirements Sencha Cmd 6+ installed and a local copy of ExtJS 6.2 which can be obtained from: https://www.sencha.com/legal/gpl/ . Sencha Cmd can be downloaded from here: https://www.sencha.com/products/extjs/cmd-download/ . Sencha Cmd also requires Ruby to be installed for Sass generation.

This application was generated in Visual Studio 2015 Enterprise with Update 2 installed (Update 3 kept hosing my Virtual Machine). Resharper 2016.2 was installed along with the Sencha ExtJs VS Extension. The Extension can be installed for a 30 day trial.

During testing, I noticed that Auto-Complete (a.k.a. Intellisense or Code Completion) was not including any of the Sencha/ExtJs options in the dropdown. I was able to confirm this conflict/bug  by setting the Resharper > Manage Options (Select current solution) > Intellisense > General to use Visual Studio for all intellisense commands. I attempted to use Custom Settings and setting just JavaScript to use Visual Studio and the rest to Resharper, however this did not work.

To reproduce, with Resharpers default setting to control all intellisense open the \Sencha\app\view\main\MainModel.js and press ctrl+space between the extend/alias object, nothing will return in the code completion dropdown. Now follow the steps mentioned previously to make Visual Studio the default intellisense controller. Pressing ctrl+space this time between the extend/alias object and Sencha auto-complete will show all available options. Sencha auto-complete now also shows results within magic string objects.

Ideally it would be best if Resharper & ExtJS got along.

The code provided is Sencha's default application and is licensed under GPL. For more information on the code provided please read Sencha's Legal GPL Page: https://www.sencha.com/legal/gpl/