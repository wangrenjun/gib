This shell script run Git in bulk for simplifies fetch a lot of repositories, it support query Github / Gitlab / Bitbucket APIs to get the job done

Currently supported features
------------------------------

* Bulk clone/pull repositories based on configurtion
* Bulk clone/pull all repositories of users / organizations / starred / watched / following peoples using Github API
* Bulk clone/pull all repositories of users / groups using Gitlab API

Usage
------

```c
USAGE: gib [-h|--help] COMMAND [<args>]
List of commands:
    clone            Bulk clone repositories
    pull             Bulk pull
    clone-or-pull    Bulk clone or pull if exists
Running this script require the jq(https://stedolan.github.io/jq/) to be installed in the system.
```

```c
USAGE: gib clone [-c|--conf <configuration file>] [-v|--verbose] [-h|--help]
```

```c
USAGE: gib pull [-c|--conf <configuration file>] [-v|--verbose] [-h|--help]
```

```c
USAGE: gib clone-or-pull [-c|--conf <configuration file>] [-v|--verbose] [-h|--help]
```

Configuration supported variables
---------------------------------

* **base_dir**: Global default working directory
* **default_branch**: Global default repository branch
* **default_access_token**: Global default `Personal Access Token`, use them when executing clone/pull commands
* **repo_url**: Repository git url (http/ssh)
* **github_user**: Username in github, it can be the name of organization if you are not sure
* **github_org**: Organization name in github
* **github_starred**: Username in github, it will clone/pull all his starred repositories
* **github_watched**: Username in github, it will clone/pull all his watched repositories
* **github_all_following**: Username in github, it will clone/pull all the repositories of people he following
* **gitlab_user**: Username in gitlab
* **gitlab_group**: Group name in github
* **dir**: Directory of the repositories in this line
* **branch**: Git branch of the repositories in this line
* **access_token**: `Personal Access Token` in this line

Demo
----

![image](https://github.com/wangrenjun/gib/raw/master/screenshots/demo.png)
