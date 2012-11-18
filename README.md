Landing Page Templates
====================
The Jekyll templates used by Aplethora for landing page creation.

Setup
-----

1. Obviously you will need [Jekyll](https://github.com/mojombo/jekyll), then you are good to go.
2. The structure in code kit uses a _less directory and a css directory in the assets directory. Your Codkit setup needs to reflect that so it compiles the css into the correct place. There is a codekit-config.json that you can import the settings from if you need. [More Info](#codekit-settings)

Usage
-----
The landing page templates are setup to use a one, two or three column style fluid/responsive layout. Proper steeps in setting up a new site:	
	
1. Create a new directory at the root and name it after the domain	
2. Inside of the directory create two files, "index.html" and "privacy.html"
3. Inside of index.html add the following code:

		---
		layout: default
		title: Site Title
		structure: one_col|two_col|three_col
		css: customCssFileName
		---
		<header></header>
		<!-- three column layout has two asides -->
		<aside></aside>
		<section></section>
		<aside></aside>
		<footer></footer>

4. Inside of privacy.html add the following code:

		---
		layout: privacy
		title: Privacy - Site Title
		domain: SiteDomain.com
		css: customCssFilename
		---
		<!-- Duplicate the header code from index.html -->
		<header></header>
		
5. You will need to create a new css file for each project. The template.css file can be copied to your new file in order to help speed up the process. The custom.css file needs to at least have the following code:

		@import: 'global.less';
		
Codekit Settings
----------------
In order to make sure Codekit processes your code correctly please follow the steps below:

1. Right click on the project folder in codekit and select Project Settings > Enable project-level settings
2. In the project settings under the General tab click the "Choose..." button under "Apply Project Defaults From File"
3. Select the codekit-config.json file from this repo
4. Use Codekit to process all of your less, js and images.
5. Love life!

Semantic.gs
-----------
The layout css files are written using [Semantic.gs](http://semantic.gs) to help control the columns and allow the site to be responsive. Documentation can be found on their site.