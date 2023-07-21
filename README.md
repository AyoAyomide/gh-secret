# How to use git secret

First follow this installation instruction [here](https://sobolevn.me/git-secret/installation).

## Generate gpg key

To generate a RSA key-pair, run:

```gpg --gen-key```

To export your public key, run:

```gpg --armor --export your.email@address.com > public-key.gpg```

To import the public key of someone else (to share the secret with them for instance), run:

```gpg --import public-key.gpg```

To list all exiting gpg keys use

```gpg --list-keys```

## Using the git secret

Step 1: Initalize git secret

```git secret init```

Step 2: Add user as viewer

```git secret tell [user gpg by there email]```

Step 3: Add a secret file

```git secret add [the filename to hide]```

Step 4: Hide the file

```git secret hide```

To remove a user use

```git secret removeperson [there email]```

## Backup keys

To export gpg private key

```gpg --armor --export-secret-key [user email]```

You can use [bitwarden](https://bitwarden.com/) to backup your secret keys