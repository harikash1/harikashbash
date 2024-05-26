Project Documentation

Author: HARIKASH SENTHILKUMAR

Student Code: 1000115710

Last Modified: 26/05/2024

This document provides an overview of two Bash scripts developed for a scripting assignment:

Task 1: User Environment Script

Summary:

This script automates the creation of user accounts and their environment based on data provided in a CSV file. It reads information like email addresses, birth dates, groups, and shared folder details to create users, set passwords, and configure their environment.

Pre-requisites:

    The script requires the following software to be installed:
        cut - for manipulating text data from the CSV file
        useradd - for creating user accounts
        passwd - for setting user passwords (may require sudo privileges)
        groupadd (optional) - for creating groups if specified in the CSV file
        chown - for changing ownership of files and directories
        mkdir - for creating directories
        cp - for copying files (optional) - used for creating links to shared folders

Instructions:

    Prepare the CSV file:
        Ensure your CSV file is formatted correctly with columns for email (username generation), birth date (password generation - YYYYMM format), group memberships (optional), and shared folder paths (optional).
    Review the log file:

    The script creates a log file named user_environment.log in the same directory as the script. This file details user creation and configuration actions, including any errors encountered.

Task 2: Backup Script

Summary:

This script automates the process of backing up a directory to a remote server. It takes a directory path as input, creates a compressed archive (.tar.gz), and uploads it securely to the specified server using scp.

Pre-requisites:

    scp command-line tool for secure file transfer (requires SSH access to the remote server)
    tar command-line tool for archive creation
Provide server details:

The script will prompt you for the following information about the remote server:

    Server IP address or URL
    Port number (default SSH port is 22)
    Username with SSH access on the remote server
    Target directory on the remote server to store the backup archive

Review the log file:

The script creates a log file named backup.log in the same directory as the script. This file details the backup process, including archive creation, connection status, and upload success or failure messages.
