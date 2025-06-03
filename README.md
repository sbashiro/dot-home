Configuration files for quick host setup.


## Installation

Examples are given for a user with
- name: John Doe
- email: johndoe@gmail.com
- login: jodo

Copy everything to the user's home directory
and change email address and SSH/GPG keys.

### Applications

```bash
sudo apt install openssh-client gpg \
                 git git-email git-pw \
                 screen \
                 neomutt urlscan lynx
```

### GPG

```bash
# Create new key for signing and encrypting
gpg --full-generate-key

# Edit neomutt passwords in plain text
vim ~/.neomutt/password

# Encrypt neomutt passwords
gpg --encrypt -r johndoe@gmail.com ~/.neomutt/password

# Remove neomutt passwords in plain text
rm -f ~/.neomutt/password
```
