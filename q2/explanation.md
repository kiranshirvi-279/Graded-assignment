q2 Secure Project Workspace Setup

mkdir -p secure_workspace/{docs,src,logs}: Created the secure workspace directory structure.

touch secure_workspace/docs/plan.txt secure_workspace/src/app.txt secure_workspace/logs/activity.log: Created the required project files.

chmod 750 secure_workspace and subdirectories: Set directory permissions so owner can read/write/execute, group can read/execute, and others have no access.

chmod 640 ...: Set file permissions so owner can read/write and group can read, preventing others from reading or modifying sensitive files.

ls -ld and ls -l: Verified the directory structure and permissions after setup.

umask: Confirmed the default permission mask used during file creation.
