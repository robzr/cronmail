# cronmail
Bash wrapper script for consistent HTML formatting of cron job output

```Usage: cronmail [-b ..] [-e ..] [-h] [-l #] [-m ..] [-n] [-p ..] [-r ..] [-s ..] command [args...]"
  -b    Override basename (default is based on command)
  -e    Subject for error (defaults to: [$basename] Error!)
  -f    Specify from header
  -h    Print this help
  -l    Limit output lines (default: 1500)
  -m    Specify mail-to (defaults to $MAILTO)
  -n    Suppress email on success
  -p    Prefix command output (defaults is no prefix)
  -r    Specify reply-to
  -s    Subject for successful run (defaults to: [$basename] Successful Run)```

Example usage:
```$ crontab -l
*/15 * * * * cronmail -m errors@example.com -n rsync -av server:mirror_files /opt/mirror/
```
