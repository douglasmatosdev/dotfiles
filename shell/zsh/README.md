Install ZSH

```bash
sudo apt install zsh -y
```

Define `ZSH` as default SHELL

```bash
sudo usermod -s /usr/bin/zsh $(whoami)
```

> ### Troubleshot: if returns error below
> `usermod: user 'YOUR_USER' does not exist in /etc/passwd`
Add your user to `passwd`

Make login root
```bash
sudo su
```

Now add you user to passwd
```bash
echo "YOUR_USER:x:1000:1000:douglas,,,:/home/YOUR_USER:/bin/bash" >> /etc/passwd
```

Close terminal and open again

Verify 
```bash
echo $SHELL
```
