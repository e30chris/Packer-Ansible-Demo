# Packer Ansible Windows

Demo of Packer calling Ansible to build a Windows GCE VM Image.

Notes:

## Windows Host Prep
Ansible docs link:

https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#winrm-setup

```
$url = "https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1"
$file = "$env:temp\ConfigureRemotingForAnsible.ps1"

(New-Object -TypeName System.Net.WebClient).DownloadFile($url, $file)

powershell.exe -ExecutionPolicy ByPass -File $file
```

## Linux Host Prep

```
sudo apt-get install ansible wget unzip
```

