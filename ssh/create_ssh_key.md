### Checking for existing SSH keys 
``ls -al ~/.ssh``

### Generating a new SSH key 
``ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`` 

This creates a new ssh key, using the provided email as a label.

> Generating public/private rsa key pair.

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

> Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]

At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".

> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]

### Start the ssh-agent in the background.
``eval "$(ssh-agent -s)"``
> Agent pid 59566


### Adding your SSH key to the ssh-agent 
``ssh-add ~/.ssh/id_rsa`` 

