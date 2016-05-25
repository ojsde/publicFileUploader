Key data
============

- name of the plugin: Public file uploader plugin
- author: Felix Gründer
- current version: 1.0.0.0
- tested on OJS version: 2.4.6
- github link: https://github.com/ojsde/publicFileUploader.git
- community plugin: no
- date: 25.5.2016

Description
============

In addition to the Files Browser where the journal manager can store files, this plugin provides the possibility to upload and manage files being publicly accessible (in contrast to the Files Browser, where the user has to be logged in to access the files).
This feature has been implemented as a plugin for the TinyMCE editor, which comprises a corresponding icon (provided that the current user has at least the role proof reader)

Installation
============

- Download and unzip the archive https://github.com/ojsde/publicFileUploader/archive/ojs_stable_2_4_6.zip
- copy the directory lib/pkp/lib/tinyMCE/jscripts/tiny_mce/plugins/publicfileuploader into the directory lib/pkp/lib/tinyMCE/jscripts/tiny_mce/plugins of your OJS installation
- copy the directory pages/publicfiles into the directory pages
- replace the following 3 files in the directory plugins/generic:
	a)  customBlockManager/CustomBlockEditForm.inc.php
	b)	staticPages/StaticPagesEditForm.inc.php
	c)	tinyMCE/TinyMCEPlugin.inc.php
	by the corresponding files in the directory plugins/generic of the zip folder

 
Implementation
================

Database access, server access
-----------------------------
- reading access to OJS tables: 0

- writing access to OJS tables: 0

- new tables: 0
- recurring server access: yes

		writing/reading files to/from [files_dir]/publicuploads/[journalID]
 
Classes, plugins, external software
-----------------------
- OJS classes used (php): 3
	
		classes.handler.Handler
		plugins.generic.tinymce.TinyMCEPlugin
		lib.pkp.classes.file.FileManager

- necessary plugins: 1

		TinyMCE Plugin
		
- optional plugins: 2
		
		Custom Block Manager
		Static Pages Plugin
		
- use of external software: no
	
- file upload: yes

	directory: [files_dir]/publicuploads/[journalID]
 
Metrics
--------
- number of files: 18

Settings
--------
- public_files_max_size (default: 20MB) in config.inc.php, section [files]

Plugin category
----------
- plugin category: generic

Other
=============
- does using the plugin require special (background)-knowledge?: no
- access restrictions: yes

	in order to upload files, the user has to be logged in and has to be (at least) the role proof reader


