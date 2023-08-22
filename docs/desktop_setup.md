# Desktop Setup Instructions

## Generating a new SSH key
1.	Open Git Bash.

2.	Paste the text below, substituting in your GitHub email address.
```
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

```
This creates a new ssh key, using the provided email as a label.

> Generating public/private rsa key pair.

3.	When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
> Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]

4.	At the prompt, type a secure passphrase. For more information, see [Working with SSH key passphrases](https://docs.github.com/en/free-pro-team@latest/articles/working-with-ssh-key-passphrases).

5.	> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]

## [Adding your SSH key to the ssh-agent](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent)

Before adding a new SSH key to the ssh-agent to manage your keys, you should have [checked for existing SSH keys](https://docs.github.com/en/free-pro-team@latest/articles/checking-for-existing-ssh-keys) and [generated a new SSH key](https://docs.github.com/en/free-pro-team@latest/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key).
If you have [GitHub Desktop](https://desktop.github.com/) installed, you can use it to clone repositories and not deal with SSH keys.

1.	Ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in [Working with SSH key passphrases](https://docs.github.com/en/free-pro-team@latest/articles/working-with-ssh-key-passphrases), or start it manually:

2.	# start the ssh-agent in the background

```
$ eval $(ssh-agent -s)

```
> Agent pid 59566

3.	Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.

```
$ ssh-add ~/.ssh/id_rsa

```

Before adding a new SSH key to your GitHub account, you should have:

•	[Checked for existing SSH keys](https://docs.github.com/en/free-pro-team@latest/articles/checking-for-existing-ssh-keys)

•	[Generated a new SSH key and added it to the ssh-agent](https://docs.github.com/en/free-pro-team@latest/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

After adding a new SSH key to your GitHub account, you can reconfigure any local repositories to use SSH. For more information, see [Switching remote URLs from HTTPS to SSH.](https://docs.github.com/en/free-pro-team@latest/articles/changing-a-remote-s-url/#switching-remote-urls-from-https-to-ssh)
Note: DSA keys (SSH-DSS) are no longer supported. Existing keys will continue to function, but you cannot add new DSA keys to your GitHub account.

1.	Copy the SSH key to your clipboard.
If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.
$ clip < ~/.ssh/id_rsa.pub
# Copies the contents of the id_rsa.pub file to your clipboard
Tip: If clip isn't working, you can locate the hidden .ssh folder, open the file in your favorite text editor, and copy it to your clipboard.

2.	In the upper-right corner of any page, click your profile photo, then click Settings.

![Step2](https://github.dxc.com/AET/example-java-sb-maven/blob/master/docs/images/ds_01.png)

3.	In the user settings sidebar, click SSH and GPG keys.

![Step3](https://github.dxc.com/AET/example-java-sb-maven/blob/master/docs/images/ds_03.png)
 
4.	Click New SSH key or Add SSH key.

![Step4](https://github.dxc.com/AET/example-java-sb-maven/blob/master/docs/images/ds_04.png)


5.	In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".

6.	Paste your key into the "Key" field.
 
![Step6](https://github.dxc.com/AET/example-java-sb-maven/blob/master/docs/images/ds_06.png)
 

7.	Click Add SSH key.

![Step7](https://github.dxc.com/AET/example-java-sb-maven/blob/master/docs/images/ds_07.png)

8.	If prompted, confirm your GitHub password.

![Step8](https://github.dxc.com/AET/example-java-sb-maven/blob/master/docs/images/ds_08.png)


Then 

Git clone project url 
