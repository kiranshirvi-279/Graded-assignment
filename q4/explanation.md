q4 File Access and I/O Investigation

echo "sample log line" > app.log: Created a sample log file to inspect file access.

exec 3<app.log: Opened app.log on file descriptor 3 for reading.

lsof -p $$ | grep app.log: Confirmed the shell process has app.log open with descriptor 3.

ls -l /proc/$$/fd | grep app.log: Verified the /proc file descriptor entry points to app.log.

ls -l > stdout.txt: Redirected stdout to stdout.txt and verified file output capture.

ls /not_a_real_path 2> stderr.txt: Redirected stderr to stderr.txt for the missing path error.

(ls -l && ls /not_a_real_path) > combined.txt 2>&1: Combined stdout and stderr into one file.

ulimit -a: Inspected current process resource limits to understand I/O and process constraints.
