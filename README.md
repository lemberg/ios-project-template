# ios-project-template
####Steps to setup iOS(objective-c) new project

1. Clone XCode Project structure
`git clone git@github.com:lemberg/ios-project-template.git
cd ios-project-template/ProjectTemplate 
git pull origin master`

2. Create empty "Single View Project" with custom name `YourProjectName` and `Bundle Id`
Inside project remove all files from subgroup `YourProjectName`(move all files to the Trash)
3. Go to `ios-project-template/ProjectTemplate` directory 
Drag and drop files `.gitignore, Podfile, Classes/, Resources/, Vendors/` to your  project 
inside directory `YourProjectName/` and select checkbox `Copy Items if Needed`  and `Create groups`
4. For universal project (iPhone and iPad) create additional directories:
`Classes/Shared/` and move there all folders from directory `Classes/` except `Application/,  Support/`
`Classes/iPhone/`
`Classes/iPad/`
5. In `YourProjectName` XCode project remove reference to  `.gitignore, Podfile` files
6. Connect `info.plist, Prefix.pch, Image.xcassets` to your project

#### Folder descriptions

```
/<Project Name>
	/Resources				# Images, storyboards,videos, .string files 
		/Storyboards
	/Classes
 		/Application 			# App delegate and related files
		/ViewControllers		# View controllers
		/Common					# Base common protocols, headers, ategories for the hole 
								projects.
			/Protocols
			/Categories
		/Models			# Models, Core Data schema
		/Views
		/Services	# Services bring together the functions of multiple managers to
					accomplish 	a full task such as authentication a user or uploading a 
					parcel
			/Protocols
			/Managers 		# Managers are directly related to their respective models, 
							and do all of the business logic surrounding those models. They 
							do not bring that logic together, though. (Create, delete,date, 
							fetch entities from the Core Data)
	/Support			# Helpers, protocols, mocks, .plists
	/Vendors			# 3rd party dependencies not managed by CocoaPods
```
