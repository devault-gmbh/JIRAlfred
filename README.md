JIRA for Alfred
============

This is an extension for [Alfred App](http://www.alfredapp.com), which let's you send basic commands to an [Atlassian JIRA](http://www.atlassian.com/software/jira) instance. 
The extension contains the [JIRA Command Line Interface](https://studio.plugins.atlassian.com/wiki/display/JCLI/JIRA+Command+Line+Interface) by Bob Swift to communicate with JIRA.
You will need Alfred and the Powerpack to use this.

Installation
----------------

To install JIRAlfred in Alfred double click on the extension file.

You then need to set your server URL and credentials in the *jira.sh* script which is located in */Users/YOURNAME/Library/Application Support/Alfred/extensions/applescripts/JIRA/jira.sh*

    #!/bin/bash
    # Comments
    # - Customize for your installation, for instance you might want to add default parameters like the following:
    java -jar `dirname $0`/lib/jira-cli-2.5.0.jar --server http://my-server --user myUserName --password myPassword "$@"

True that, it's a bit dodgy and will fuck up your extension when you update the extension, but i'll work on that!

How to use
----------------

Once installed, you can run the following commands, for examples look below.


    jira comment issuekey comment
    jira log issuekey comment #timeSpent
    jira help
        

Examples
----------------
    $ jira comment JIRALFRED-4 That's an amazing issue! 
    $ jira log JIRALFRED-2 Look boss, i crafted an extension #3h 15m
    $ jira log JIRALFRED-3 #30m
        
Download
----------------
[JIRAlfred](https://github.com/devault-gmbh/Alfred-Ext/JIRA.alfredextension)
    

## Version History ##
### 1.0 - March 21, 2012###
 
- Initial commit
- Added ability to add comments to an issue in JIRA
- Added ability to log work on an issue in JIRA
- Added compatibility for update extension