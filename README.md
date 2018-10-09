![Project Status: Active][Project Status Image]

Code Auto Update
===========================

It has been designed for "utilities repositories" aka repo with few/no collaboration and must be kept up-to-date<br>
I use it in https://github.com/usbkey9/uktools

It works like a master-slave replication where git upstream is the master and clones are the slaves

You have to call this script in each of yours directly callable script<br>
Don't worry if your scripts call between them, there is a delay of 1 hour between pulls

# Usage

* Download script, set exec permission
``` 
wget https://raw.githubusercontent.com/usbkey9/autoup/master/autoup && chmod +x autoup
```

* Activate it
``` 
touch autoup.on
```

* Call it from all your callable bash script (preferably in the early) with PID

```
./autoup $$
```
You can replace `$$` with your process id if you call autoup from non-bash

* If you want to disable it

```
./autoup -unin
```

* Debug (will always update repo and enable verbose)

```
touch autoup.debug
```

There is a good example in [https://github.com/usbkey9/uktools/](https://github.com/usbkey9/uktools/blob/master/setup#L23) 

## Disclaimer

* When debug off, if your repo don't need update, nothing will be prompt
* The script doesn't update itself so there is no backdoor possible
* If you use SSH key for git auth in your repo: avoid using non-X-session for running autoup

## TODO (Tests)

* It doesn't support subrepo/submodule for now (external help is welcome)
* Any other contributions is welcome


[Project Status Image]: https://img.shields.io/badge/project-active-green.svg "Project Status: Active"
