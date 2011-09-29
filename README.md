
PreRequisite
===============

* Firefox
* Python
* Git
* make

Getting setup
=====================

To pull and run openwebapps addon:
  
    git clone https://github.com/mozilla/openwebapps
    cd openwebapps
    make pull
    make run
  
You can build an xpi:

    make xpi
  
You can run the tests:

    make test
  

If you want to run (using make run) in a specific profile:

    OWA_PROFILE=/path/to/firefox/profile make run
  
Tests cannot be run in a specific profile.


Prepare your firefox profile
-----------------------------

You probably want a test firefox profile so open up the [Profile Manager](http://kb.mozillazine.org/Profile_manager).

In the Mac:

    /Applications/Firefox.app/Contents/MacOS/firefox -ProfileManager

On Windows:

    firefox.exe -P

In the profile manager, create a profile with the name `fxsharetest`, then exit the profile manager.

Repository Layout
===================

This is an experiment around installable web applications.  What
you'll find here:

<dl>
<dt>addons/</dt>
<dd>Addons for different browsers that provide better support
    for web applications: including new features (like search and
    notification support) and better integration into browser UI.</dd>

<dl>
<dt>docs/</dt>
<dd>Documentation, including an in-depth discussion of the design
  and goals of the project.</dd>

<dt>example/</dt>
<dd>An example that shows how to integrate myapps javascript libraries
    to allow a site author to trigger an installation of their application.</dd>

<dt>harness/</dt>
<dd>Files related to setting up a local develoment environment.  Currently
    a nodejs script that will allow you to run a webserver that serves
    up the various sites contained here.</dd>

<dt>site/</dt>
<dd>The "myapps" website.  To the end user this site is a location
    where they can launch their application dashboard.  To the developer
    this is the domain under which several javascript libraries are
    hosted that allow interaction with the user's applications.
    Site nightlies are hosted at https://myapps.mozillalabs.com</dd>
</dl>

<dt>store/</dt>
<dd>The "appstore" website, implemented as a Python webserver.
  Implements a demonstration application store that performs 
  authentication of users and provides "proof-of-purchase" assertions
  to applications.  No real payment processing is performed.
  Hosted at https://appstore.mozillalabs.com.
  </dd>
</dl>

## LICENSE

All files that are a part of this project, except where explicitly noted, are covered
by The following license:

    Version: MPL 1.1/GPL 2.0/LGPL 2.1
    
    The contents of this file are subject to the Mozilla Public License Version 
    1.1 (the "License"); you may not use this file except in compliance with 
    the License. You may obtain a copy of the License at 
    http://www.mozilla.org/MPL/
    
    Software distributed under the License is distributed on an "AS IS" basis,
    WITHOUT WARRANTY OF ANY KIND, either express or implied. See the License
    for the specific language governing rights and limitations under the
    License.
    
    The Original Code is openwebapps.
    
    The Initial Developer of the Original Code is Mozilla Foundation.

    Portions created by the Initial Developer are Copyright (C) 2010
    the Initial Developer. All Rights Reserved.
    
    Contributor(s):
    
    Alternatively, the contents of this file may be used under the terms of
    either the GNU General Public License Version 2 or later (the "GPL"), or
    the GNU Lesser General Public License Version 2.1 or later (the "LGPL"),
    in which case the provisions of the GPL or the LGPL are applicable instead
    of those above. If you wish to allow use of your version of this file only
    under the terms of either the GPL or the LGPL, and not to allow others to
    use your version of this file under the terms of the MPL, indicate your
    decision by deleting the provisions above and replace them with the notice
    and other provisions required by the GPL or the LGPL. If you do not delete
    the provisions above, a recipient may use your version of this file under
    the terms of any one of the MPL, the GPL or the LGPL.
