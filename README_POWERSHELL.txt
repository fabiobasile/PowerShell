Step 1: Use the following Power Shell script to rename all sub-directories according to the root folder name

Get-ChildItem -Recurse -Filter *PROJECTNAME* | Rename-Item -NewName { $_.name -replace 'PROJECTNAME', '[replace with actual project name]'} -verbose

Step 2: Use the following Power Shell script to rename all sub-directories according to the project date in this format: "010123" (e.g. "Jan 1st, 2023")

Get-ChildItem -Recurse -Filter *PROJECTNAME* | Rename-Item -NewName { $_.name -replace '000000', '[replace with actual project date]'} -verbose

Step 3: All new files created in these folders must be appended with the root prefix.