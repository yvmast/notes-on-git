# Install git and clone a github repository

Resource: [docs.github.com/en/get-started/quickstart/set-up-git](https://docs.github.com/en/get-started/quickstart/set-up-git)

Steps:
* install git from [git-scm.com/downloads](https://git-scm.com/downloads)
* configure username and email. Note that these settings will be stored in your user's home directory in a file called '.gitconfig'
** configure username

```
$ git config --global user.name "Mona Lisa"
```

** configure email. Github allows to keep your email address private by using the 'noreply'-email address provided by github. see [setting-your-commit-email-address](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)

```
$ git config --global user.email "YOUR_EMAIL"
```

* authentication. I prefer SSH even though there is more setup and configuration involved. See detailed information below.
* clone the repository
    * in short: open git bash, cd to the workspaces directory (it will create a new folder with the name of your repostitory), run command `git clone <url>`
    * Here's the instructions: [cloning-a-repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)


## SSH configuration

### Create the local key files

In Git Bash, create a new key with this command

```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

Here is a good article about the ssh key passphrase: [working-with-ssh-key-passphrases](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases)


### Start SSH Agent and configure it

Start the agent in the background

```
eval "$(ssh-agent -s)"
```

Add the new key to the ssh agent

```
ssh-add ~/.ssh/id_ed25519
```


### Configure Github

Copy the public key and set it up in the github profile settings.

Command to copy the key

```
clip < ~/.ssh/id_ed25519.pub
```
