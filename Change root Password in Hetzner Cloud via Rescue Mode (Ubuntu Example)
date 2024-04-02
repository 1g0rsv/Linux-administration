
# How to Change the root Password in Hetzner Cloud via Rescue Mode (Ubuntu Example)

Occasionally, while managing a server, you might find yourself in a situation where you need to reset or change the `root` user's password. This article describes how to change the `root` password on a Hetzner Cloud server using Rescue Mode, with a specific focus on servers running Ubuntu.

## Step 1: Activating Rescue Mode

Rescue Mode is a special boot mode provided by Hetzner for recovery and diagnostics. Here's how to activate it:

1. Log in to the **[Hetzner Cloud Console](https://console.hetzner.cloud/)**.
2. Select your project and navigate to your server management.
3. In the "Servers" section, select the desired server.
4. Find the "Rescue" section and activate it by selecting an OS for the rescue mode and its version. For Ubuntu servers, select the corresponding Ubuntu rescue image.
5. Click on "Enable Rescue & Power Cycle" to reboot the server into Rescue Mode.

## Step 2: Connecting to the Server via SSH

Use the temporary credentials provided to connect to the server via SSH:

```bash
ssh root@<server IP address>
```

## Step 3: Mounting the File System

To mount the server's root filesystem, execute:

```bash
lsblk # to identify the correct device
mount /dev/sda1 /mnt # assuming /dev/sda1 is the root partition
```

## Step 4: Changing the root Password

Enter the chroot environment and change the password:

```bash
chroot /mnt
passwd
```

Enter the new root password when prompted.

## Step 5: Rebooting the Server

After changing the password, you need to exit chroot and unmount the filesystems:

```bash
exit
umount /mnt
```

Reboot the server to exit Rescue Mode and boot into the regular mode:

```bash
reboot
```

Now, you should be able to log into the system with the new root password.

## Conclusion

Using Rescue Mode in Hetzner Cloud is a powerful tool for regaining access to your server in case of lost root password or other critical situations. This guide focused on servers running Ubuntu, but the process is similar for other Linux distributions. We hope this guide helps you quickly and safely resolve access issues.

