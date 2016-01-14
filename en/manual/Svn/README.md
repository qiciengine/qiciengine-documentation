# Project Directory Structure and Version Control

## Project Directory Structure
A project contains the following directories:  
* Assets - a game resource directory 
* Build - publishing directory
* Editor - script files to extend editor
* Plugins - the plugins used in the project
* ProjectSetting - configuration files
  * editor.setting -  the configuration file used to configure the editor
  * project.setting - the configuration file used to configure the project or the game
  * scene.setting - the configuration file used to configure game scenes
  * script.setting - the configuration file used to configure script loading order
* Scripts - game logic codes
* Temp - temporary directory

## Version Control
QICI Engine's version control choice is SVN or GIT. The following directories or files must be added to version control:
* Assets
* Editor
* Plugins
* ProjectSetting
  * project.setting
  * scene.setting
  * script.setting
* Scripts