# DevcamPortfolio
- rails generate scaffold Blog Title:string body:text

rake routes


### Initiating git inside application
 git init

 add particular file
	git add <file_name>
	
adding everything 
	git add . / git add --all / git add -A
	
to see status
	git status / git log
	

> USING gitignore file
 gitignore is the way by which we can tell git that which file we don't want to checked into version control.

Let suppose we don't out secrets file to not get checked into version control and we mention that in the gitignore file 
/config/secrets.yml  which currently i don't have in my application maybe because of different versions of rails.

Therotically any changes that we make to the file should not be seen in the git status command but it shows 
also to remove any changes from specified file
 git checkout /config/secrests.yml

continued 

git shows the ignored file because of git cached we have to clear out all of the cached
git rm . -r --cached
Now we should make commit of this tasks by mentioning that we have cleared cached and push the commit.
Now we can make changes in the file that we need it to be ignored and it will not be added into the repo.
it's going to remove all the cached now ignored file will not get seen as jordan said so but it didn't work for me i was trying this blogs_controller.rb file.






