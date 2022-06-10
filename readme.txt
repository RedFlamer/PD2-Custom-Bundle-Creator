You must ensure the game's bundle_db.blb is in the same directory as the tool for it to work as well as the bundle files you're appending to.
Make sure the bundle_db and bundles you're modifying are backed up as this tool will not create backups and does not provide a method to revert changes.
This tool was made for PAYDAY 2 update 24.2 and may have issues with other PD2 updates/PD:TH/RAID WW2.

In order to declare a package and it's contents create an info.txt file in the directory of the tool, it should strictly follow this specific format:
PACKAGE "name of package" e.g. PACKAGE packages/my_custom_package
path
extension
path
extension
APPEND "name of package" e.g. APPEND packages/game_base
path
extension
path
extension
APPENDALL "name of all_x bundle" e.g. APPEND all_4
path
extension
path
extension
ENDPACKAGEINFO
Append/Appendall mode will not check to ensure the files you append aren't already present in the bundle, the bundle database will not be modified if the file is found, so appending assets from other bundles is possible
The tool should have created new bundle files in the directory, they can then be placed in the assets folder of the game and loaded through PackageManager:load("package name")