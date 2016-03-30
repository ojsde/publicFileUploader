# Managing public files

The aim of this plugin is to provide a possibility to upload files in OJS which are publicly downloadable (also for not logged in users).
It is implemented as a plugin for the TinyMCE editor: if the current user has at least the role "proof reader", the tinyMCE editor contains an additional button.

By clicking this button a file management dialog with the following features appears:
- uploading new files
- displaying a list of already existing files (where the files can also be deleted)

A maximum overall size for these files (default: 20 MB) can be set in the config file of OJS. 
