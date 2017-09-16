Prepare an environment for conjure-up

## Step 1
Enable client cert login to your root account on your server

## Step 2
Add your default ssh key to provisioning/files/authorized_keys/ANY_NAME.pub

## Step 3
Install ansible (and vagrant if you want to try alternative vagrant setup)

## Step 4 Run for remote server (replace IP_ADDRESS with the ip address of the server)
```bash
ansible-playbook -i ,$IP_ADDRESS provisioning/playbook.yml --extra-vars "ansible_port=22"
```

## Step 5
Afterwards run:

```bash
ssh mark@$IP_ADDRESS
lxd init
# accept defaults except select none for ipv6
conjure-up```

## Step 6  install kubernetes-core
Select kubernetes-core and accept defaults.

You won't need to set a sudo password as mark has passwordless sudo.
