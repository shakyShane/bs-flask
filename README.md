A sample project to help illustrate an issue with the Flask + BrowserSync.

#Step 1 - Install

First, ensure you are using the latest BrowserSync version

```bash
sudo npm install -g browser-sync
```

#Step 2 - start Flask

* FORK this repo (so that you can send a PR showing the bug)
* run `python run.py` to start the development server

#Step 3 - Proxy with BrowserSync

Take the URL that Flask gives you, usually something like `http://127.0.0.1:5000/` and 
run BrowserSync in proxy mode using the following command

```bash

browser-sync start --proxy http://127.0.0.1:5000/ --files="app/templates/**, app/static/**"

```

You should now see that css changes are auto-injected & html files reloaded on file change.

#Step 4 - reproduce your bug.
Go ahead and do anything to this sample that will clearly demonstrate the bug and push it
back up to github. Then BrowserSync authors can simply clone your fork and work to resolve the bug.

