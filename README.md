# gitem
## A command for git workflow automation
### Usage
##### Just type the following command in your terminal to automatically push all changes in your git project to the currently checked out branch of your local and remote repositories.

```shell 
gitem '<your commit message>' 
```  

### Installation
##### Add the following code to the end of your ~/.bashrc file

```sh
gitem () {
  git add -A
  git commit -m "$1"
  branch=$(git branch | sed -n -e 's/^\* \(.*\)/\1/p')
  git push origin $branch
}
```

##### Then run the following in your terminal

```shell
source ~/.bashrc
```

### That's it! You're good to go!
