***Main issue:***
- When having finished with a preemptive version of the web server, we dealt with a crash
- The page notified us of an "Internal Server Error"

1) Upon further experimentation, when booting up the server packages were being deleted:
2) Following the error messages, we began to redownload packages so that the __init__.py within ./docker_run_all.sh would run correctly (see Part 1 - web server.md for images)
  - Tried downloading python-is-python3 after line 25 python command not found
  - Tried downloading flask-marshmallow
  - There was a "no module to install" error message following many of these redownloaded packages
  - Following the CTFd documentation, we started [Flask's built-in debugging server](https://docs.ctfd.io/docs/deployment/installation/)

3) The same error message was displayed after this troubleshooting
5) Within CTFd platform we ran [prepare.sh](https://github.com/CTFd/CTFd/blob/master/prepare.sh) which allowed us to boot up the web server
6) Shortly after, the web server would crash again
7) We realized that this was a reoccuring issue that stemmed from the NVMe's inappropriate memory allocation (ran out)

To address this issue, we have:
- Cached data to be stored on RAID instead of NVMe
- CTFd Platform: Reconfigure CTFd, reuploaded challenges, changed port numbers in docker files
- Use a performance benchmarking tool such as Samsung Magician Software to keep track of drive statistics
