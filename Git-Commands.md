# adds all the file for to the tracked files list

        git add -A

# commit the tracked files to git local

        git commit -m "my_message_for_the_commit"

# attach local repo to a remote git repo

	git remote add origin https://github.com/prp311/test.git
	git remote add origin /repos/project1.git/

# push the changes to remote repository

        git push -u origin master

# add credentials locally, to avoid entering repeatedly

	git config credential.helper store

# help
	https://stackoverflow.com/questions/7632454/how-do-you-use-git-bare-init-repository
