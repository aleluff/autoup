![Project Status: Active][Project Status Image]

Code Auto Update
===========================

The script doesn't update itself so there is no backdoor possible

#Usage

* Download script and activate it
``` 
wget https://raw.githubusercontent.com/usbkey9/autoup/master/autoup && touch autoup.on
```

* Call it from all your callable bash script

```
./autoup $0 $@
```

## TODO (Tests)

* It doesn't support subrepo/submodule for now (external help is welcome)
* Any other contributions is welcome


[Project Status Image]: https://img.shields.io/badge/project-active-green.svg "Project Status: Active"
