# SSH On Steamdeck (Work in progress)

SSH stands for Secure Shell Protocol. It allows one to securely remote into their computers from a different computer. With SSH, one can send commands, or even copy files, between 2 computers. OpenSSH is a common SSH implementation that is installed on the Steam Deck by default. However, while the Steam Deck is able to connect to other computers via SSH, it does not allow other computers to connect to it via SSH. This is because the SSH Daemon (SSHD), or SSH Server is disabled by default. From a security perspective, this makes sense. The average user of the Steam Deck is probably never going to remote into it via SSH, so Valve most likely decided to disable it by default so any unfriendly hackers don't try to brute force their way into your Steam Deck and cause problems.

## Enter desktop mode

Hit the Steam button and scroll down to the Power option. Then select Switch to Desktop.

## Set a password

Open Konsole and type `passwd` to set a password for the deck user.

## Enable SSHD

In Konsole:

```
sudo systemctl enable sshd
sudo systemctl start sshd
```

## Find steamdeck IP

```
ip a
```

## Login to the Steamdeck

### From linux

Open your favorite terminal and ssh into the deck

```
ssh deck@<deck_ip>
```
