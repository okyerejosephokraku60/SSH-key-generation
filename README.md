# SSH-key-generation
How to generate SSH Keys using Termux

To generate SSH keys in Termux, you can follow these steps:

1. Install Termux:
   - Download and install the Termux app from the Google Play Store or F-Droid.
   - Open the app and wait for it to initialize.

2. Update packages:
   - Run the following command in Termux to update the package repositories:
     ```
     apt update
     ```

3. Install OpenSSH:
   - Run the following command to install OpenSSH in Termux:
     ```
     pkg install openssh -y
     ```

4. Generate SSH keys:
   - Run the following command to start the SSH key generation process:
     ```
     ssh-keygen -t rsa -b 4096
     ```
   - You will be prompted to enter a file path to save the SSH keys. You can press Enter to accept the default file path (usually `/data/data/com.termux/files/home/.ssh/id_rsa`).
   - You will also be prompted to enter a passphrase for the SSH key. You can choose to set a passphrase or leave it blank for no passphrase. Press Enter after making your choice.
   - The SSH key pair (public and private keys) will be generated and saved in the specified file path.

5. View the SSH public key:
   - Run the following command to view the SSH public key:
     ```
     cat ~/.ssh/id_rsa.pub
     ```
   - The SSH public key will be displayed in the terminal. You can copy the entire key (including the "ssh-rsa" prefix) for use in configuring remote servers or services.

You have now generated SSH keys in Termux. The private key is saved in the specified file path (default: `~/.ssh/id_rsa`), and the public key can be viewed using the `cat` command.
