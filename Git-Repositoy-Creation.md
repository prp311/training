	#create repo
        sudo mkdir /repos/
	chown --reference=$HOME /repos/
	chmod --reference=$HOME /repos/

	# initialise repo
        git init --bare /repos/project1.git

	# Create working directory. Skip if already exists
	mkdir ~/project1
	cd ~/project1

	# initialize working directory
	git init

	# add file and commit to local repo
	echo fist version > README
	git add -A
	git commit -m "First commit"

	# push the changes to remote repo (/repos/project1.git)
	git remote add origin /repos/project1.git/
	git push -u origin master
