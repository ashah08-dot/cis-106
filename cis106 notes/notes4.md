 	Managing files and directories:
The commands are often followed by options and then arguments which are the items upon which the command acts on.
Example: Command -option argument
	   ls                   -l          ~/Downloads    : it will long list all the files in Downloads directory.

* Commands:
Mkdir: to create directories.
Mkdir -p: to create a parent directory with other directories.
Touch: to create files.
rm: to remove the files.
rm -r: to remove the directory.
Mv: to move and rename the directories using relative path.
Sudo mv: to move and rename directories using absolute path.
Cp: to copy the files, to copy the files -r option must be used.
To display inode data: stat + file
To create hard link: ln file ~/Downloads/fileHL
Soft link: ln -s files fileSL
For getting help: man ls, to exit man page ‘q’.

 	Wildcards:
Star (*) wildcard: it matches anything and nothing and matches any number of characters.
Example: ls *.txt – it will list all the files who has .txt as an extension, regardless the name and size of the file.


When to use * wildcard:
To list all the files with a particular file extension
When you do not know the complete name of file, but you remember the portion of the name.
When you want to copy, move or remove all files that match with a particular name convention.

Example: ls *.txt *.pdf – to list all files with the extension .txt and .pdf
	  ls file.* - to match the name of the file regardless the extension
	 ls *file.* - to list the file that has string ‘file’ in its name.

Question mark (?) wildcard: it matches precisely one character.
It is very helpful when you want to list the hidden files. 
Example: ls .??* - it will match all the files that start with a or ..and have any character after it.

Bracket [] wildcard: it matches a single character in range.
It uses ! mark to reverse the match or say to make an exception. 
Example: match everything except vowels [!aeiou] or except numbers [!0-9].

For example:
Ls f[aeiou]* : to match all files that have a vowel after letter f.
Ls f[a-z]* : to match all the files that has range of letter after f

To list the files who has 1990-2000 in its name
Ls 1990..2000 

 	Brace {} Expansion: its not a wildcard but another feature of bash that allows you to generate arbitrary strings to use with commands.
To create a whole directory structure In a single command:
	Mkdir -p music/{jazz,rock}/{mp3files,video,oggfiles}/new{1..3}

Parent directory: music
Sub directory: jazz – contains: mp3files: new, old, video: new, old, oggfiles: new, old.
	           Rock - contains: mp3files: new, old, video: new, old, oggfiles: new, old.
To remove multiple files in single directory:
Rm -r {all the files you want to remove}.
