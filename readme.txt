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
APPENDALL "name of all_x bundle" e.g. APPENDALL all_4
path
extension
path
extension
ENDPACKAGEINFO

Description of the modes provided by the tool:
PACKAGE: Creates new bundles that can be loaded through PackageManager:load("package name")
APPEND: Appends assets onto a bundle that will get loaded when the bundle loads
APPENDALL: Appends assets onto an all_x bundle that can be streamed in by the game