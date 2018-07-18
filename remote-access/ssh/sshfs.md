# SSHFS (SSH Filesystem)

SSHFS allows you to mount a Raspberry Pi's files over an SSH session.

## Install

### Linux

Install SSHFS on your computer with:

```bash
sudo apt-get install sshfs
```

(This assumes you are using a Debian-based system)

### Mac

See [osxfuse](https://github.com/osxfuse/osxfuse/wiki/SSHFS)

### Windows

See [SSHFS For Windows (sshfs-win)](https://github.com/billziss-gh/sshfs-win#how-to-install)

## Usage

### Linux and Mac

First, create a directory on your host computer:

```bash
mkdir pi
```

Then mount the Raspberry Pi's filesystem to this location:

```bash
sshfs pi@192.168.1.3: pi
```

Now enter this directory as if it is a regular folder; you should be able to see and access the contents of the Raspberry Pi:

```bash
cd pi
ls
```

You can also browse the Pi's filesystem using your computer's file manager (including drag-and-drop to copy files between devices), and use your computer's applications (text editors, image processing tools, and so on) to edit files directly on the Pi.

### Windows

With Pi's defaults
 - Use the network drive path \\\\sshfs\\pi@raspberrypi
 - Password: raspberry
 
 [Map Network Drive](https://github.com/billziss-gh/winfsp#winfsp---windows-file-system-proxy)
