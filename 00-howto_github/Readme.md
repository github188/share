
# HOW-TO github

Record some skills for github usage.

##Global setup:
  
    git config --global user.name "Your Name"
    git config --global user.email lovelacelee@gmail.com
      
##Next steps(Create a new repo):

    mkdir myrepo
    cd myrepo
    git init
    touch README
    git add README
    git commit -m 'first commit'
    git remote add origin git@github.com:lovelacelee/myrepo.git
    git push -u origin master
      
##Existing Git Repo?(Add a existing repo)

    cd existing_git_repo
    git remote add origin git@github.com:lovelacelee/existing_git_repo.git
    git push -u origin master