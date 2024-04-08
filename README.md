# note-it-app
noteIt App
To create a simple text editor in Java Swing we will use a JTextArea, a JMenuBar and add JMenu to it and we will add JMenuItems. All the menu items will have actionListener to detect any action.
There will be a menu bar and it will contain two menus and a button:
 

File menu
open: this menuitem is used to open a file
save: this menuitem is used to save a file
print : this menuitem is used to print the components of the text area
new : this menuitem is used to create a new blank file
Edit menu
cut: this menuitem is to cut the selected area and copy it to clipboard
copy: this menuitem is to copy the selected area to the clipboard
paste : this menuitem is to paste the text from the clipboard to the text area
Close : this button closes the frame

Program to create a simple text editor:
To create a simple text editor: 
 

First, we will create a frame f titled “editor” and apply a metal look and feel and set an ocean theme in it.
We will add a text area and a menubar with three menu File, Edit, and Close.
The “File” option has 4 menu items new, open, save and print.
“Edit” has 3 menu items cut, copy and paste. We will add an action listener to all the menu items(using addActionListener() function) to detect any action.
We will add the menu items to the menu and menu to the menubar using add() function and we would add the menubar to the frame using addJMenuBar() function.
We will add the text area to the frame using add function set the size of the frame to 500,500 using setSize(500,500) function and then display the frame using show function.
Here is how the functions of the menu will be invoked:
 

On selecting the cut, copy, paste and print menu item the inbuilt functions of text area cut(), copy(), paste() and print() will be invoked.
On selecting “save” menu item, a file chooser will get opened which will show the save dialog after selecting a file the filewriter(buffered writer) would write the contents of the text area to the file and close the file writer and buffered writer.
On selecting “open” menu item, a file chooser will get opened which will show the open dialog after selecting a file a file reader and a buffered reader would read the file and set the text of the text area to the contents of the file.
If the “new” menu item is selected the text of the text area will be set to blank. If “close” menu item is selected the frame is closed by using the function isVisible(false).
