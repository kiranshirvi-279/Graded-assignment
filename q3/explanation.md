q3 File System and Link Analysis

rm -f original.txt hardlink.txt symlink.txt: Removed previous files to begin the experiment cleanly.

echo "Linux link test file" > original.txt: Created the original file with test content.

ln original.txt hardlink.txt: Created a hard link that shares the same inode as original.txt.

ln -s original.txt symlink.txt: Created a symbolic link pointing to original.txt.

ls -li: Checked inode numbers and identified which files are hard links or symbolic links.

stat original.txt hardlink.txt symlink.txt: Collected metadata for the original file, hard link, and symlink.

cat original.txt, cat hardlink.txt, cat symlink.txt: Verified that all three paths returned the same file content.

rm original.txt: Deleted the original file name to test link behavior.

ls -li: Verified that hardlink.txt still exists with the same inode and symlink.txt remains but now points to a missing target.

cat hardlink.txt: Confirmed hard link still provides the file content.

cat symlink.txt: Demonstrated the symbolic link is broken after deleting the original file.
