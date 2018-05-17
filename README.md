# cronmail
Bash wrapper script for consistent HTML formatting of cron job output

```
Usage: cronmail [-b ..] [-e ..] [-h] [-l #] [-m ..] [-n] [-p ..] [-r ..] [-s ..] [-t ..] command [args...]
  -b    Override basename (default is based on command)
  -e    Subject for error (defaults to: [$basename] Error!)
  -f    Specify from header
  -h    Print this help
  -l    Limit output lines (default: 1500)
  -m    Specify mail-to (defaults to $MAILTO)
  -M    Optionally override mail-to for success only
  -n    Suppress email on success
  -p    Prefix command output (defaults is no prefix)
  -r    Specify reply-to
  -s    Subject for successful run (defaults to: [$basename] Successful Run)
  -t    Override email tagline
```
Example usage:
```
$ crontab -l
*/15 * * * * cronmail -n -m errors@example.com rsync -av server:mirror_files /opt/mirror/
```
