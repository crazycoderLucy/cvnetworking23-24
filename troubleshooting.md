One day the NVMe ran out of memory (due to inappropriate memory allocation) - server crashed, notfied "Internal Server Error"

Packages were being deleted:
- Tried downloading python-is-python3 after line 25 python command not found
- Tried downloading flask-marshmallow
- Telling us no module to install
- start Flask's built-in debugging server, did not work - same error message as running before

Ran prepare.sh - started working

NOW:
- Make flags and cache data stored on RAID instead of NVMe
- Must reconfigure CTFd - redownloaded
- Reuploading challenges
- Changed all port numbers in docker files
