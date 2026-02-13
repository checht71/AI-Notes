This guide will show you some of he basics of Azure, especially with regards to storage and virtual machine management.

## SSH
Azure gives you a key that you are supposed to save onto your system. When you login via SSH, you must include a pointer to that key along with the IP address they give you and the username you set in your settings. By default it's `azureuser`.
Example:
```bash
ssh -i ~/.ssh/id_rsa azureuser@10.111.12.123
```

Check out [[SSH for Cloud Computing]] and [The Official Microsoft Guide](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/ssh-from-windows) for more.

## Downloading from Storage with Azcopy
Azcopy has some strange commands, but the gist of it is this. When you start a VM, you can "easily" download all of your stuff from their data container using the format `azcopy copy "[source][sas]" "[destination]" --recursive=true`. *SAS* is a secure asshole service key. You can get one by going to your data container then `Security & Networking -> Secure access Signature`. Then you can generate the key. You have to paste it with the question mark in the quotations with the source. If your destination is on azure you need an SAS key for that too.
You can get the *source* by going to your data container, clicking `properties` and then copying the URL. The destination is usually a location on your hard drive.
[More on that horseshit](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10)

## Setting Up a Remote Desktop
Follow this guide as soon as you start your instance:
https://learn.microsoft.com/en-us/azure/virtual-machines/linux/use-remote-desktop?tabs=azure-cli

## Installing Azcopy:
For some reason it's not installed by default on some of their VMs. Kill me. This command will install it.
`curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash`
