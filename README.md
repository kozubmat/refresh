# refresh
Repo used for installing Windows PC 

# Azure addons insctructions
## Installers:

### Using Chocolatey:
#### 1. Install Chocolatey [LINK](https://chocolatey.org/install#individual)
    >  Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1')) \

#### 2. Config GIT [LINK](https://git-scm.com)
   
    > choco install git
    OR
    > winget install --id Git.Git -e --source winget
    
    > git config --global user.name "Mona Lisa"
    > git config --global user.email "mona.lisa@gmail.com"
    
#### 3. Install tools
    
    > choco install filezilla 7zip putty notepadplusplus keepas  
    > choco install packer terraform postman vscode  
    > choco install yubikey-manager gpg4win
    > choco install gcloudsdk azure-cli
    > choco install microsoft-teams.install zoom
    
    
//
### Using Exec:
1. Azure CLI [LINK](https://learn.microsoft.com/en-us/cli/azure)
    > // Prefered way to install is tp use package MSI \
    > winget install -e --id Microsoft.AzureCLI \

    or

    > PS C:/user/system32> Install-Module AZ

    after install

    > Set-ExecutionPolicy Unrestricted
//
