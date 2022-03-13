# How to setup an Access Token for Github and use in Git CLI

## Generate new access token
* In Github go to ~Settings~ -> ~Developer settings~ -> ~Personal access token~
* Give the token a specific name for it's usecase and give it the least priveleges
* Save it somewhere secure, like LastPass

## Use access token in git cli
* In the `git` cli, you can now use this token in place of a password when prompted.

## Cache access token in git cli
* To cache the token so you don't need to provide it every time:
    * enter `git config --global credential.helper cache`
    * This will cache the credentials next time you enter them
