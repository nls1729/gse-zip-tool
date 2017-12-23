# gse-zip-tool - Gnome Shell Extension Zip Tool

See https://bugzilla.gnome.org/show_bug.cgi?id=778677. The ability install
or uninstall Gnome Shell extensions was removed from the gnome-tweak-tool
Gnome Shell version 3.26.

Gnome Shell Extension Zip Tool is based on the code removed from the tweak
tool. The application is provided for use by extension writers who need to
install extensions from zip files and uninstall extensions.  A user who
reports a problem with an extension may be asked to perform tests in order
to find the source of the problem.  The user may be asked to install a test
version of the extension by the extension writer.  In this case the user
needs a simple means to install the extension zip file.

The application provides four toolbuttons:

1. About - Displays an about dialog with the usual about information.

2. Open - file chooser for selection of the zip file to install or the
   local gnome shell extension's directory to uninstall.

3. Install - toggle button when selected places application in install mode.
   Only a zip file can be selected.  The zip file is examied to insure the
   file contains a Gnome Shell extension.

4. Uninstall - toggle button when selected places application in uninstall
   mode.  When the file chooser is opened the local extension directory
   is displayed. Only a directory with an ampersand in its name can be
   selected for removal.

5. When the user opens the selected zip file or local extension directory
   the install or uninstall is performed and the user is directed to restart
   the Gnome Shell session (logout/login) to complete the operation.
  
A Makefile is provided to install the application.

1. $ make version - for maintainer's use only
   This option sets the version number based upon a file named VERSION.
   The VERSION file is not available on the remote Github repository.

2. $ make install - installs the application and support files.
   The Python executable is installed in $HOME/.local/bin.  The ui file
   is installed in $(HOME)/.local/share/gse-zip-tool.  The application
   icon is installed in $(HOME)/.local/share/gse-zip-tool.  The
   desktop file org.nls1729.gse-zip-tool.desktop is generated and
   installed in $(HOME)/.local/share/applications.

3. $ make uninstall - uninstalls the application and support files.

This application has been tested on Fedora and Ubuntu with Gnome Shell
version 3.26. 
