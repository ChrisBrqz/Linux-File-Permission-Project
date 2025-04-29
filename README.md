# Linux-File-Permission-Project
File permission auditing and modification in a Linux environment

Project Summary

In the `/home/researcher2/projects` directory, I analyzed permission structures for files and subdirectories, including:
- Regular project files
- A hidden file: `.project_x.txt`
- A sensitive subdirectory: `drafts`

After reviewing the current access control, I applied permission changes to align with organizational security policies.

Key Commands Used
- `ls -la`: Display full permission details of files and directories
- `chmod`: Change file permissions using symbolic notation
- `pwd`: Print working directory


Tasks Performed
- Interpreted 10-character permission strings (`rwxr-xr--`)
- Adjusted file access so that “others” cannot write to any files
- Restricted `.project_x.txt` to user and group read-only
- Limited `drafts` directory access exclusively to the `researcher2` user


Example Changes Made
```bash
chmod o-w project_k.txt               # Remove 'write' from others
chmod u-w,g-w,g+r .project_x.txt      # Hidden file read-only to group
chmod g-x drafts                      # Group can't execute into drafts


Concepts Demonstrated
Linux file permission structures (user, group, other)
Use of hidden files and restricted subdirectories
Command-line permission modification
Least privilege access principle
