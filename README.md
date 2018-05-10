![Project Status: Active][Project Status Image]

Code Auto Update
===========================

This script was designed to be call by bash script, and recall it after pulling repo with same arguments<br>
Typically, if you have scripts that must be up-to-date on run, implement autoup in each of them<br>
Don't worry if your scripts call between them, there is a delay of 1 hour between possible pull (disable in debug)

# Usage

* Download script, set exec permission
``` 
wget https://raw.githubusercontent.com/usbkey9/autoup/master/autoup && chmod +x autoup
```

* Activate it
``` 
touch autoup.on
```

* Call it from all your callable bash script (preferably in the early)

```
./autoup $0 $@
```

* If you want to disable it

```
rm autoup.on
```

* Debug (will desactivate 1 hour delay)

```
touch autoup.debug
```

There is a good example in [https://github.com/usbkey9/uktools/](https://github.com/usbkey9/uktools/blob/master/setup#L23) 

## Disclaimer
The script doesn't update itself so there is no backdoor possible

## TODO (Tests)

* It doesn't support subrepo/submodule for now (external help is welcome)
* Any other contributions is welcome


[Project Status Image]: https://img.shields.io/badge/project-active-green.svg "Project Status: Active"
