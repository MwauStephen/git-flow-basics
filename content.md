`Git-flow Basics`

## For you to use git flow on windows installing the Git SCM comes with in built git workflow commands

## Git flow works with two main branches `Main/master` and the `develop` branch.

`Steps to start using git flow`

## 1.Create an empty repository on github.

## 2.Create a new folder on your local computer.

## 3. Add the the repo url from your local machine(basically pushing content to the newly created remote repo)

## 4.Start using gitflow.

`To start using git flow`

## Initialize gitflow using this command.

<!--
git flow init
 -->

## The above command creates two branches `master/main` and `develop` branch.

## The other branch input prompts(`feature,hotfix,release,bugfix and support`) can be left to be added later

## After intializing gitflow,and being switched to develop branch you need to commit and push the changes in develop branch,using the following command.

<!--
 a must step otherwise publish changes on feature branches wont be publish unitl index(develop is commited.

git push -u origin develop

 -->

`Creating branches from develop branch`

## Whenever there is any new feature eg(`login...`) you need to create a feature branch off/from the develop branch.By default after running the first command,gitflow uses the develop branch as default after initializaiton.

## To create your first feature branch use the following command.

<!--

git flow feature start feature_name_branch

git flow feature start login-feature
 -->

## After creating the above feature branch,gitflow will automatcially switch to this branch.

## You can now start woriking on the changes and commiting to this branch.

## After commiting to this branch,all the changes are local so you need to push them to the remote origin.

## To do that you run the following command

<!--
git flow feature publish login-feature
 -->

## Once you are done with developing the feature(`login-feature`),you then need to merge it to the develop branch using gitflow command below.

 <!-- 
 git flow feature finish login-feature
  -->

## Once you run the above command(merging of feature branch to develop branch),you will be automatically switched to `develop branch`.

## Now after merging the feature to develop and being switched to the develop branch ..this changes are still locally in your machine so you need to push them to the remote origin.

## Run the following command to push the develop local changes to the remote origin.

<!--
git push origin --all
 -->

## Now the above merging has some effects on the feature branch that you just merged into develop.The feature branch (`login-feature`) gets deleted both locally and remotely after merging .ie after running this command

 <!-- 
 git flow feature finish login-feature
  -->

`NB:After publishing feature branch to develop,then publishing develop to main..for each you must open a pull request`.

`Pull Request`

## Also known as a `merge request` in some version control systems like GitLab, is a fundamental concept in collaborative software development, particularly when using distributed version control systems like Git.

## It's essentially a request to merge changes made in one branch into another branch, typically from a feature or topic branch into the main branch (e.g., 'develop' or 'main').
