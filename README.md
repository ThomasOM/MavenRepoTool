# MavenRepoTool
A simple shell script that creates a maven repository on your project's github repository.
Note that this is now obsolete since Github has public packages that do not require authentication.

# How to use
Please read this before you use the script to prevent messing up your project's github repository.

Before we start, make sure your project creates your jar file in the target folder when installing.
The script finds your jar file by your `group_id`, `artifact_id` and `version` in your `pom.xml`

- Put the script in your project folder. (You can add it to your .gitignore file)
- Run the script in git bash using ``` ./deployscript.sh <group_id> <artifact_id> <version> ``` where `group_id`, `artifact_id` and `version` are equal to the values you have entered in your project's `pom.xml` 
- A new folder will be created in the parent folder of your project, called `<your_project_folder>-repository`
- The script automatically deploys your project to this folder and pushes it to the branch `repository` of your current project
- You can now share your maven dependency using the following repository url: `https://raw.github.com/<your_project_organization>/<your_project_name>/repository/`

Every time you update your project, you can run the script as explained in the second step to update your maven repository

Feel free to use this anywhere you want.
