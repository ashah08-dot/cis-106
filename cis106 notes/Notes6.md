     Managing data: 
* Archiving utilities: 
Tar:  creates archive by combining files and directories into a single file.
CPIO: creates an archive, restores files from an archive, or copies directory.
Ar: creates, modifies, and extract from archive.

* The tar program:
To create an archive: tar + option (-cf) + archive name + files to add to archive.
To extract an archive: tar + option (-xf) + file to extract.
To extract archive in different directory: tar -xf example.tar –directory ~/Downloads.
Extract specific file: tar -xf example.tar file3.
List the contents of an archive: tar -tf example.tar
Add file to archive: tar -rf example.tar file4.
Update file inside an archive: tar -uf example.tar file4.
To add members of an archive to another archive: tar -Af example.tar example2.tar.
To delete specific member of an archive: tar –delete -f example.tar file3.
To compare files with members of an archive: tar -df example.tar file2.

    The cpio program:
Cpio requires a list of file to archive and option to create an archive is -o. [ls | cpio -ov > archive.cpio].
To extract an archive: cpio -iv < archive.cpio.
Archive specific files: find . -iname *.sh | cpio -ov > scriptsarchive.cpio.
Create tar archive with cpio: ls | cpio -ov -H tar -F sample.tar.
Extract tar archive with cpio: cpio -idv -F smple.tar.
View the content of *.tar Archive file: cpio -it -F sample.tar.

* The ar utility:
Archive files with ar: ar r test.a *.txt.
List content: ar t test.a.
Add new member to an archive: ar r test.a test3.txt.
Delete a member: ar d test.a test3.txt.
 
* File Compression: 
The gzip, bzip2, and xz commands are used for compression.
When you compress file using this command, the result is a file with similar name but with the correspondent file extension.

* Gzip: 
Compress a single file: gzip file.txt.
Multiple files: gzip + file names
To compress and keep original file: gzip -k file.txt
Decompress: gzip -d file.txt
Force compression: gzip -f file.txt
See details of compressed file: gzip -l file.txt.
Compress files recursively: gzip -r schoolfiles
Test the validity of compress file: gzip -t files.txt.gz.
Compress a file to its max: gzip -9 files.txt.gz.
Compress to its min: gzip -1 file.txt.gz

* Bzip2:
Compress a file: bzip2 file.txt
Compress multiple files: bzip2 + files to compress.
Decompress file: bzip2 -d file to decompress.
Compress and keep the file: bzip2 -k + file to decompress.
Compress file and show detail: bzip2 -v + files.
Check integrity of a file: bzip2 -t file.txt.bz2.

* Xz:
Compress a file: xz file.txt
Compress multiple files: xz + files to compress.
Decompress file: xz -d file to decompress.
Compress and keep the file: xz -k + file to decompress.
List compression information: xz -l -v + files.
Compress to its max: xz -9 files.txt.
Compress to its min: xz -0 files.txt
Check integrity of a file: xz -t file.txt.xz.

* 7zip:
Create and archive: 7z a files.tz files.iso.
Extract an archive: 7z e file.7z.
Create and archive with different archive format: 7z a -tzip file.zip fileExample.iso.
See files in an archive: 7z l file.7z.
Test integrity: 7z t file.7z.
To archive with password protection: 7za a -p {password_here} files.7z.

rar:
Create and archive: rar a archive.rar file1 file2 file3.
Extract an archive: unrar archive.rar.



    File Permission: (File Ownership)
A file can be owned by one user and one group.
Ls -l show s you file user, owner, and group owner.
/etc/passwd file contains list of all the users in Linux.
/etc/group file contains a list of all the groups in Linux.
The Chown command is used for changing group owner.

# Symbolic Notation:

category	Operator	Permissions
U (user)	+ (add to existing permissions) 	R (read)
G (group)	-(remove from existing permissions) 	W (write)
O (other)	= (assign absolute permissions)	 X (execute)
A (all)	One of the preceding operators	 One or more of the preceding permissions


Examples: 
Chmod u+x script.sh
Chmod o-x script.sh
Chmod u=rex, g=rw, o=r script.sh

# Numeric Notation:

Permission	Value
Read	4
Write	2
Execute	1

Example:
Chmod 777 script.sh – it will give a file all the permission that is read write and execute.
Chmod 700 script.sh – it will give user all the permissions, and no permission for owner or group.
Chmod 555 script.sh – it gives read and execute permission to all 3: user, owner, and group.

