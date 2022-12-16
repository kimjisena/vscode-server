# Setting up a remote dev environment with VS Code Server
### Author: Kim Jisena
### GitHub: [@kimjisena](https://github.com/kimjisena)

<br />

So you want to develop on your remote machine but you don't want to stray from your favored VS Code?
VS Code Server has got you covered. Do the following to get started.

<br />

## 1. Install VS Code Server on your remote machine
Whether it's a VM, WSL, a Docker container or your Linux box; run the following 
command from your remote terminal to get VS Code Server:

```sh
# make sure `wget` is installed

$ wget -O- https://aka.ms/install-vscode-server/setup.sh | sh
```

## 2. Start VS Code Server on your remote machine
Run the following command on your remote terminal to start VS Code Server

```sh
$ code-server
```

Tip: Run `code-server -h` to see all the available options to launch and manage your server.

## 3. Set up VS Code Client on your local machine
If you already have a working installation of VS Code on your local machine (which obviously you do!), then you're all good.

- Install the extension `Remote - SSH (ms-vscode-remote.remote-ssh)`

Note: Make sure you have an OpenSSH compatible SSH client on your local machine.

- Next step, in your VS Code editor press `F1`, then search `Remote-SSH: Add SSH Host`, press enter.

- Add your remote machine `user@ipaddress`. You will be prompted for your `user`'s password.
Enter your password and you're done.

- VS Code will establish a SSH tunnel to your remote machine and you can now open folders right on your local VS Code editor.

That's it. You can now do what on remote environment what you normally do on your local machine.

Happy coding!
