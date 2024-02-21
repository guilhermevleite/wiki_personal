# To use key instead of password on Ubunti:

Copy the key into the ~/.ssh/authorized_keys file
Permission must be: rw--------
# To use SSH key instead of password on Git services:

Copy the following in ~/.ssh/config
Make sure ~/.ssh/config has the following permission:
> chmod 0700
OR
> chmod u+rwx,go-rwx ~/.ssh/config

> # Gitlab
> Host gitlab.com  
>   Hostname altssh.gitlab.com  
>   User git  
>   Port 443  
>   IdentityFile ~/Dropbox/remote/ssh/git

> # Github
> Host github.com  
>   Hostname ssh.github.com  
>   User git  
>   Port 443  
>   IdentityFile ~/Dropbox/remote/ssh/git
