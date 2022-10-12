# refresh
Repo used for installing Windows PC 

# Azure addons insctructions
## Installers:
### Using Exec:
1. Azure CLI [LINK](https://learn.microsoft.com/en-us/cli/azure)
    > // Prefered way to install is tp use package MSI \
    > winget install -e --id Microsoft.AzureCLI \

    or

    > PS C:/user/system32> Install-Module AZ

    after install

    > Set-ExecutionPolicy Unrestricted
2. GIT [LINK](https://git-scm.com)
    > winget install --id Git.Git -e --source winget

    > git config --global user.name "Mona Lisa"

    > git config --global user.email "mona.lisa@gmail.com"

### Using Chocolatey:
1. Install Chocolatey [LINK](https://chocolatey.org/install#individual)
    > Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1')) \

2. Install tools
    > choco install git filezilla 7zip putty notepadplusplus keepas  

    > choco install packer terraform postman vscode  

    > choco install yubikey-manager gpg4win

    > choco install gcloudsdk azure-cli

