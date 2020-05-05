# epub2text
epub2text

Simple bash script which uses the program 'epub2txt' from https://github.com/kevinboone/epub2txt2
to create separate '.txt' files from a folder of epubs, and put them into a sub-directory called 'txt'.
All the original epubs remain intact.
This processes epubs up to 350X faster than the 'ebook-convert' tool from calibre.

I don't know how to make an install yet so it has to be done manually


To install as a terminal function copy the 'epubtotext' file so you can type in terminal:

epub2text path/to/epub/folder

to convert epubs into txt


Otherwise it's easier to simply install as a bash script using the 'epub2text' file.

once installed type epub2text and press enter
it asks you to enter full pathname to folder, so do that and press enter

1.
put the bash script 'epubtotext' into your #!/bin/bash folder or somewhere else into your $PATH.
to view folders that are in your PATH type in terminal:

echo $PATH

2.
set permission for program to run using:

chmod 755 /full/path/to/epubtotext

or use:

chmod -R 755 full/path/to/folder

which will change permissions for all files in folder to 755 
ie. gives you permission to: read, write, & execute all files in folder

Now all you need to do is open epubtotext and edit the first line path_books="path/to/your/books"
save the file and type in terminal to run:

epubtotext

If you are using the epubtotext_function file: continue on

3.
to use the epub2text function you have to add the file location to '.bashrc' file in your home folder
.bashrc is hidden by default as all files with '.' at the start of their name are.
to open .bashrc in terminal editor:

cd ~
nano .bashrc

add this somewhere in .bashrc and save it:

source full/path/to/epubtotext

where full/path/to/epubtotext_function is the path on your computer to epubtotext_function

4.
you now need to get the terminal to update its values from '.bashrc' by running:

source ~/.bashrc

5. Now all you need to do is type in terminal:

epub2text path/to/folder/with/epubs

and it will make a new folder inside specified folder with all the converted '.txt files



