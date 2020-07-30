# Eclipse GIT / Gitlab - Training (Remote Training GIT 07.2020)

## Bitbucket - Server ##

### Install Trial ###

https://confluence.atlassian.com/bitbucketserver/install-a-bitbucket-server-trial-867192384.html

```
# Download Installer 
# Use default options
https://www.atlassian.com/software/bitbucket/download
# You directly download it ... you need to know the version to construct the link
wget https://www.atlassian.com/software/stash/downloads/binary/atlassian-bitbucket-7.4.0-x64.bin
```

### Home Directories ###

  * This is where the data and the repos live
  * Just called home here, but not really /home 
  
```
Installation Summary
Installation Directory: /opt/atlassian/bitbucket/7.4.0 
Home Directory: /var/atlassian/application-data/bitbucket 
HTTP Port: 7990 
Install as a service: Yes
```

## Bitbucket - Cluster ## 

### Aufbau ###
https://confluence.atlassian.com/bitbucketserver/clustering-with-bitbucket-data-center-776640164.html


### Backup - Strategy ### 

  * Backup Home- directory (/var/atlassian/application_data/bitbucket/) and db-server
  
  ```
  # /etc/passwd 
  atlbitbucket:x:1000:1000:Atlassian Bitbucket:/var/atlassian/application-data/bitbucket:/bin/sh

  ```
  * Scripte als Vorlage: 
  * https://bitbucket.org/atlassianlabs/atlassian-bitbucket-diy-backup/src/master/
  * Filesystem muss Snapshots unterstützen (Ausser ZFS und AWS liegen hier keine Scripte vor) 
  * Sicherung von 


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
