JIRA for Alfred
============

This is an extension for [Alfred App](http://www.alfredapp.com), which let's you send basic commands to an [Atlassian JIRA](http://www.atlassian.com/software/jira) instance. 
The extension contains the [JIRA Command Line Interface](https://studio.plugins.atlassian.com/wiki/display/JCLI/JIRA+Command+Line+Interface) by Bob Swift to communicate with JIRA.
You will need [Alfred](http://www.alfredapp.com/#download-alfred) and the [Powerpack](http://www.alfredapp.com/purchase) to use this.

Now take me to the [download](https://raw.github.com/devault-gmbh/Alfred-Ext/master/JIRA.alfredextension) already!

Installation
----------------

To install JIRAlfred in Alfred double click on the extension file.

You then need to create a bash script containing your JIRA URL and credentials. For this copy the script located at *~/Library/Application Support/Alfred/extensions/applescripts/JIRA/jira-sample.sh*, rename it to *jira.sh* and move it up one level in the folder structure. Then fill it out with your JIRA information as in the example below.

    #!/bin/bash
    # Copy this file to ~/Library/Application Support/Alfred/extensions/applescripts/jira.sh
    # - Customize for your JIRA installation, for instance you might want to add default parameters like the following:
    java -jar `dirname $0`/JIRA/lib/jira-cli-2.5.0.jar --server http://my-server --user myUsername --password myPassword "$@"

Finally you should have a script configured for your JIRA instance located at *~/Library/Application Support/Alfred/extensions/applescripts/jira.sh* CHMODed correctly.

The reason for moving this file out of the extension folder, is that by doing it the [Extension Updater from David Ferguson](http://jdfwarrior.tumblr.com/updater) can be supported for this extension without the need of recreating the *jira.sh* script.

How to use
--------------

Once installed, you can run the following commands, for examples look below.


    # Comments
    jira comment issuekey comment
    jira c issuekey comment

    # Log work
    jira log issuekey comment #timeSpent
    jira l issuekey comment #timeSpent

    # Help
    jira help
    jira ?
        

Examples
----------------
    # Comments
    $ jira comment JIRALFRED-4 We got issues..
    $ jira c DRAGON-1 Thou shall be prepared, i got a two handed sword now.

    # Log work
    $ jira log JIRALFRED-2 Look Alfred, i crafted an extension #3h 15m
    $ jira l DRAGON-1 Eat this! #30m
        
Download
----------------
Here you go: [JIRAlfred](https://raw.github.com/devault-gmbh/Alfred-Ext/master/JIRA.alfredextension)
    

Version History
--------------------
### 1.1 - March 21, 2012
 
- Validation
- Fixed some bugs
- Support for updates

### 1.0 - March 21, 2012
 
- Initial commit
- Added ability to add comments to an issue in JIRA
- Added ability to log work on an issue in JIRA
- Added compatibility for update extension