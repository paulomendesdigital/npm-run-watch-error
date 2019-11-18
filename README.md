# npm run watch Error

For error `throw er; // Unhandled 'error' event` verify if the file `/etc/sysctl.d/99-sysctl.conf` exist
  - If not exist, create with the code below
```
sudo touch /etc/sysctl.d/99-sysctl.conf
```

Then run the code below to fix the error
```
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.d/99-sysctl.conf && sudo sysctl --system
```
