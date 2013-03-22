Build RSSOwl 2.x using Eclipse
==============================

This page will guide you through the process of setting up Eclipse to run and export RSSOwl 2.x.

## Install Eclipse

You should be able to use any Eclipse version to run and export RSSOwl. If you have never installed Eclipse before, simply download
and extract Eclipse from here: http://www.eclipse.org/downloads/packages/eclipse-classic-422/junosr2

We recommend to use a fresh workspace with RSSOwl to ensure that your configuration is not messing up with the RSSOwl cofiguration.
As such, your package explorer should be empty and not have any other projects in there.

## Setup Target Platform

RSSOwl requires a specific version of Eclipse RCP to run. You can not build RSSOwl with any newer RCP version than 3.4.2. For your convinience,
the target platform in this repository will just work and matches with the target platform that is used to build RSSOwl for official releases.

* download rssowl-target (https://github.com/bpasero/rssowl-target/archive/master.zip)
* unzip rssowl-target and the included target.zip
* in Eclipse open Window > Preferences > Plug-in Development > Target Platform
* Click "Add..."
* Click "Next"
* Click "Add..."
* Choose "Directory" and "Next"
* Click "Browse"
* Choose "target_win" if you plan to run/export for Windows and "target_nix" for Mac/Linux
* Click "Ok" and "Finish" and "Finish" again
* The target platform should show up in the list named "New Target"
* Check the "New Target" so that it becomes active and close the preferences dialog with "Ok"

Remember to change the target platform between Windows and Mac/Linux if you plan to export RSSOwl for multiple platforms!

## Import RSSOwl Sources

RSSOwl is a set of Eclipse Java plug-ins. Use your favorite source control provider in Eclipse to either get the sources through
SVN or GIT:
* SVN: https://sourceforge.net/p/rssowl/code/8614/tree/
* GIT: https://github.com/rssowl/RSSOwl/

Make sure to check out the specific RSSOwl version you want to build. The current stable version is RSSOwl 2.1.6. 

You should see the following list of plugins and features in your package explorer after import
* org.rssowl.core
* org.rssowl.core.tests
* org.rssowl.feature
* org.rssowl.feature.dependencies
* org.rssowl.feature.eclipse
* org.rssowl.feature.tests
* org.rssowl.lib.db4o
* org.rssowl.lib.httpclient
* org.rssowl.lib.jdom
* org.rssowl.lib.lucene
* org.rssowl.ui

You should not see any compile errors when you do a full build (Project > Clean).

RSSOwl works best with Java 1.5 or 1.6.

## Run from Eclipse

* click on Run > Run Configurations from the menu
* click on "Launch RSSOwl 2.0" from "Eclipse Application"
* click the "Plug-ins" tab
* uncheck all plugins from the "Target Platform"
* click on "Add required plug-ins"
* click "Run"

RSSOwl should start just fine.

## Run Tests from Eclipse

* click on Run > Run Configurations from the menu
* click on "Launch RSSOwl 2.0 Tests" from JUnit Plug-in Tests

## Export from Eclipse

* click on rssowl.product in org.rssowl.ui
* click on "Eclipse Product export wizard" from the "Exporting" area
* change the root directory to be "rssowl"
* uncheck "Synchronize before exporting"
* uncheck "Generate metadata repository"
* click "Finish"
* if you want to export for multiple platforms, check the "Export for multiple platforms" option

Keep in mind that for Mac/Linux you need the rssowl_nix target platform set and for Windows the other one.
