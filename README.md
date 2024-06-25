# vm-setup
Setting up VMs:
1. Copy the files in this repo to your destination folder.
  
2. Open virtual-machines and edit:
- MAX_DISK_SIZE: Can generally retain 128G
- HOSTNAME: Give a meaningful name here, generally related to the project. Easier to keep track of running VMs.
- PORT array: Use this to define your port numbers for the VM(s).

3. You're all set! Run:
- ./virtual-machines setup
- ./virtual-machines start

During setup, you'll be prompted while enabling password based authentication for SSH on the virtual machines. <br />
Note: The default credentials for every VM is student / pass .

4. sudo netstat -tulnp
- Gives you the status of active TCP endpoints. You should be able to see the port numbers corresponding to the connections forwarding traffic to the VM.

5. Login to the VM(s), and change the password. Make it something a bit more secure than 'pass'!
- ssh -p <PORT NUMBER> student@localhost

6. Check the connection to each VM from your local machine:
- ssh -p <PORT NUMBER> student@SERVER-IP
