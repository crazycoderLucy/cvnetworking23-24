***Main issue:***
- When having finished with a preemptive version of the web server, we dealt with a crash
- The page notified us of an "Internal Server Error"

Upon further experimentation, when booting up the server packages were being deleted:
- Following the error messages, we began to redownload packages so that the __init__.py within ./docker_run_all.sh would run correctly
- Tried downloading python-is-python3 after line 25 python command not found
- Tried downloading flask-marshmallow
- Telling us no module to install
- start [Flask's built-in debugging server]([url](https://docs.ctfd.io/docs/deployment/installation/
)), did not work - same error message as running before

Ran prepare.sh - started working
https://github.com/CTFd/CTFd/blob/master/prepare.sh

We realized that this was a reoccuring issue that stemmed from the NVMe's inappropriate memory allocation (ran out)

NOW:
- Make flags and cache data stored on RAID instead of NVMe
- Must reconfigure CTFd - redownloaded
- Reuploading challenges
- Changed all port numbers in docker files
- Use a performance benchmarking tool such as Samsung Magician Software
