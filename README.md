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

* 

## Import RSSOwl Sources


## Run from Eclipse

## Export from Eclipse



The target platform to use to build RSSOwl 2.x. Instructions:

* download Eclipse (http://archive.eclipse.org/eclipse/downloads/drops/R-3.7-201106131736/index.php)
* get rssowl projects from https://github.com/rssowl
* import into eclipse
* download target.zip from https://github.com/bpasero/rssowl-target
* start eclipse and configure the contents of either rssowl_win (for windows) or rssowl_nix (for mac and linux) as the target platform in preferences
