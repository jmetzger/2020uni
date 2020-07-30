# Eclipse GIT / Gitlab - Training (Remote Training GIT 07.2020)

## Bitbucket - Server ##

### Install Trial ###

https://confluence.atlassian.com/bitbucketserver/install-a-bitbucket-server-trial-867192384.html



## Gitlab - Requirements ## 

https://docs.gitlab.com/ee/install/requirements.html

## Schnittstellen (Ansatzpunkte für Entwicklung Plugin)

### Programmierung über JGit (Java-Bibliothek unterhalb von eGIT) ###

```
EGit verwendet die JGit - Bibliothek:
```

https://www.vogella.com/tutorials/JGit/article.html

### API von gitlab ###

https://docs.gitlab.com/ee/api/

```
# Auch Erstellen von Commits s durchführen
https://docs.gitlab.com/ee/api/commits.html
```

## Hooks ##

### Client Side hooks ###

https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks

### Server Side hooks (vanilla git-Server only - no gitlab) ###

https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks
https://git-scm.com/book/en/v2/Customizing-Git-An-Example-Git-Enforced-Policy#_an_example_git_enforced_policy


### File_Hooks in gitlab ###

```
# Important. The data it retrieves (json) is completely
# different than in server - hooks (git) 
https://gitlab.t3isp.de/help/administration/file_hooks
```

### Server Hooks in GIT (you cannot use those in gitlab) ###

```
#gitlab is tied together differently.. so not useable here
