# Creating App Shortcuts in Ubuntu: Example of Paraview

1. Move paraview to /opt and set the rights

        sudo mv /path/to/paraview /opt/paraview
        sudo chmod -R 755 /opt/paraview/

2. Create desktop shortcut in /usr/share/applications (and rename it paraview.desktop).

    If the file already exists:
    
        cp /opt/paraview/share/aplications/path/to/desktop.desktop /usr/share/applications/paraview.desktop
        
    otherwise create the file : 
    
        vim /usr/share/applications/paraview.desktop

   Note that there are other methods like putting the desktop shortcut in ~/.local/share/applications and then symlink, see for instance the installation of zotero : https://www.zotero.org/support/installation 

4. Modify the desktop file accordingly (or complete with the following if it did not exist):

        [Desktop Entry]
        Version=1.0
        Type=Application
        Name=ParaView
        Comment=Parallel visualization application
        Exec=/opt/paraview/bin/paraview %f
        TryExec=/opt/paraview/bin/paraview
        Icon=/opt/paraview/share/icons/hicolor/96x96/apps/paraview.png
        StartupWMClass=paraview
        Categories=Qt;Science;DataVisualization;
