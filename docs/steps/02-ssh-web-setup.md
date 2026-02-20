# SSH Web Setup

**Project Section**: SSH key setup and web server installation for the deployed VM.

**Goal**: Configure secure SSH access and install Nginx; verify service runs locally on the VM.

## Steps taken

1. Generate SSH key pair locally and copy the public key into the VM provisioning step.
   ![Key generation](../images/13-VM-KeyGenerator.png)
2. Locate the new VM resource and confirm it's running.
   ![Deployed VM resource](../images/14-VM-Deployed.png)
3. Connect via SSH using the assigned username and provided private key.
   ![SSH connect attempt](../images/16-VM-SSH_Connect.png)
4. Install Nginx and start the service; confirm installation finishes without errors.
   ![Install nginx](../images/17-VM-SSH-InstallWeb.png)
   ![Install complete](../images/18-VM-SSH-InstallComplete.png)

**Validation**: On the VM, `systemctl status nginx` returned active and the service was reachable on localhost (further network validation in next section).
