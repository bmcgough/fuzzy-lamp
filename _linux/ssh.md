# SSH -or- Secure SHell

In order to connect to a remote system, you need a method or protocol to perform the communication. The method used today to make a connection to a remote server or host is called SSH (Secure SHell). This is a bit of misnomer as SSH is not a shell itself, just a method of running a shell (or other process) on a remote system.

## Secure

The key feature that SSH has is that it encrypts all communication. Using a public/private key pair, you can even avoid the use of passwords entirely.

## Basic use

The simplest way to use ssh is to simply supply the hostname as the only argument: `ssh rhino`. The most common adjustment to this is to specify your username as well. This is often necessary if the username on your local system is no the same as your username on the remote system. For example, I am `Ben` on my macOS system, but `bmcgough` on our Linux servers. So I run `ssh bmcgough@rhino` from my macOS laptop.
