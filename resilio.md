# Resilio Sync

* Start resilio sync
> sudo systemctl start resilio-sync
* Enable autostart (doesn't really works)
> sudo systemctl enable resilio-sync
* Change user permission
> sudo usermod -aG user_group rslsync  
> sudo chmod g+rw synced_folder

## Permissions

> sudo usermod -aG user_group rslsync  
> sudo usermod -aG rslsync user_name  
> sudo chmod g+rw synced_folder
