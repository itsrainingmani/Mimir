tags: #python #gdrive #api #linux

Building a simple CLI with python to automate uploading epubs to Google Drive
The CLI looks for a config folder that is located in the root of the current user and also checks for a `client_secrets.json`. Using the GDrive's Python client packages gives inbuilt functions for common activities and also authentication and token refresh

Token Refresh - Store the token as a `.pickle` file in linux's `/tmp` folder.  Actually, it makes more sense to store the token pickle file within the config folder since `/tmp` does not guarantee that the file will persist between invocations of the application.

Using Python's `setup.py` with an entry point in it is the easiest way of defining an executable script that can then be installed locally with pip (`pip install -e /path/to/script`). The `-e` flag designates this package as "editable" which means we can modify the script without needing to reinstall it.

This seems like a better method than using shebangs to denote that the script is executable since we can maintain our existing folder structure and location and leverage Python to perform the building and setup process for us.