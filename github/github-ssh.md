### Gitbash
[Gitbash download link](https://git-scm.com/downloads "Gitbash download link")

### Generating a New SSH key

1. Open Git Bash.

2. Paste the text below, substituting in your GitHub email address. <br/>
`$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` <br/>
sample comand <br/>
`$ ssh-keygen -t rsa -b 4096 -C "test@hotmail.com"` <br/>
![](https://github.com/Learning-101/DevOps/blob/master/github/githubimages/1-github.png)
3. When you are prompted to "Enter a file in which to save the key," <br/>
 press Enter. This accepts the default file location. <br />
 ![](github/githubimages/2-github.png)
4. At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".

### Adding your SSH key to the ssh-agent

- Ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in "Working with SSH key passphrases", or start it manually:
$ eval ``ssh-agent -s``
Agent pid 59566

### Adding a new SSH key to your GitHub account
1. Copy the SSH public key to your clipboard. <br />
`clip < ~/.ssh/id_rsa.pub` <br />
![](github/githubimages/3-github.png)
2. In the upper-right corner of github.com page, click your profile photo, then click Settings. <br />
![](github/githubimages/4-github.png)

3. In the user settings sidebar, click SSH and GPG keys.  <br />
![](github/githubimages/5-github.png)

4. Click New SSH key or Add SSH key.<br />
![](github/githubimages/6-github.png)

5. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal myssh key".


6. Paste your key into the "Key" field.

7. Click Add SSH key.

8. If prompted, confirm your GitHub password.
