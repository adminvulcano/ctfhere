## What this does
* Quickly create container with current directory mounted using the alias `ctfhere`
* Attach other shells to this container with `alsoctf`
* Mounted directory (/mnt/) files always have the same permissions as the host user
* Pwninit's solve.py GDB argument will work from host, and will running both gdb pwndbg and the binary from the container while being in a new terminal on the host machine.

## Install
```bash
git clone https://github.com/pilvar222/ctfhere/
cd ctfhere
bash build.sh
```

## Disclaimer

The setup is cursed and even dangerous. Your computer *shouldn't* break, but I would suggest quickly going through build.sh before running it. I will clean this sooner or later. In the meantime, I'd be happy to receive contributions.

## TODO

* The chown bash loop is resource expensive. Change to something more viable.
* Make build.sh work for different shells.
* Change ssh connection method. As of now, it only works with rsa and non-password protected keys
* patch pwninit so that it also makes binaries whose libs are linked with a relative path have them linked with an absolute path.
