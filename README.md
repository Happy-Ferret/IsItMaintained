# Maintained

Monitoring open source projects activity.

![](web/img/dude.png)

## Metrics

- Issue median closing time (collaborators issues excluded)
- Percentage of open issues (collaborators issues excluded)

Ideas:

- Last commit date (from all branches)
- Issue average/median acknowledgement time (i.e. first comment after the issue was open)

Dropped ideas:

- Release frequency: depends a lot on the project, hard to say a frequency is "good" or "bad"

## Run

    $ composer install
    $ bower install
    $ cd web/
    $ php -S 0.0.0.0:8000 index.php

The first time a badge is generated takes a few seconds, then it is cached. Be patient.

GitHub has an API rate limit that is reached very easily. To circumvent that, you can generate an
API token (https://github.com/settings/applications) and set it in `parameters.php`.

## Commands

- `bin/console stats:show user/repository`: shows the statistics for a repository (skips the cache)
- `bin/console cache:clear`: clears all the caches
- `bin/console cache:warmup`: warmup the caches

## Requirements

- PHP 5.6
- GD extension (`php5-gd`)
