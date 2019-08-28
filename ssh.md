* To use SSH key instead of password:

Copy the following in ~/.ssh/config

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
