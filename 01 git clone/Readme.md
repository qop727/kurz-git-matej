# Cvičení git clone

## Cvičení 1

1. Vytvořte nový adresář u sebe na počítači.
2. Naklonujte do něj repozitář s projektem z GitHubu, např. https://github.com/KUTlime/Git-cheatsheet.git

### Řešení 1

```bash
cd C:\Users\mhlus\Documents\GitHub\
new-item -Type:directory "KurzGit"
cd C:\Users\mhlus\Documents\GitHub\KurzGit
git clone https://github.com/KUTlime/Git-cheatsheet.git
```

## Cvičení 2

1. Naklonujte veřejný projekt ze svého účtu na GitHubu na svůj počítač pomocí příkazu git clone.
2. Upravte nějaký soubor ve svém lokálním repozitáři.
3. S pomocí git příkazu, ověřte, že změny se neuložily na server a že na serveru je stále původní verze.

### Řešení 2

```bash
cd C:\Users\mhlus\Documents\GitHub\KurzGit
git clone https://github.com/qop727/Python
cd C:\Users\mhlus\Documents\GitHub\KurzGit\Python
remove-item try.py
remove-item py_lists
new-item -Type:file "to_try"
git status
```

## Cvičení 3

1. Zkuste naklonovat projekt z jiné větve pomocí příkazu git clone.
2. S pomocí git příkazu, ověřte, že jste úspěšně naklonovali projekt z požadované větve.

### Řešení 3

```bash
cd C:\Users\mhlus\Documents\GitHub\KurzGit
git clone --branch totry https://github.com/qop727/Python
cd C:\Users\mhlus\Documents\GitHub\KurzGit\Python
git status
git branch
```

## Cvičení 4

Uveďte všechny příkazy, které musíte zadat do příkazové řádky. Citlivé údaje pozměňte, aby nebyly zneužitelné (_tj. nekopírujte celé klíče_).

1. Naklonujte repozitář s projektem na vzdáleném serveru pomocí SSH.

### Řešení 4

```bash
ssh-keygen -t rsa -b 4096 -C "your_mail@gmail.com"     #Uložit soubor do ~/.ssh/nazev_souboru_s_ulozenym_SSH
cd ~/.ssh
new-item -Type:file "config"
@"
Host github.com
    HostName github.com
    User user_name
    IdentityFile ~/.ssh/nazev_souboru_s_ulozenym_SSH
    IdentitiesOnly yes
"@ > config
cat ~/.ssh/nazev_souboru_s_ulozenym_SSH.pub     #Zkopírovat zobrazený ssh klíč do nastavení GitHub účtu
git clone git@github.com:user_name
```
VS Code User settings.json:
{
    "git.autofetch": "all",
    "github.gitProtocol": "ssh",
    "workbench.colorTheme": "Monokai Dimmed",
    "powershell.powerShellAdditionalExePaths": {
    "Linux": "/opt/microsoft/powershell/7/pwsh"
    },
    "terminal.integrated.profiles.linux": {
    "bash": {
        "path": "/bin/bash"
    },
    "zsh": {
        "path": "/bin/zsh"
    },
    "PowerShell": {
        "path": "/opt/microsoft/powershell/7/pwsh"
    }
    },
    "terminal.integrated.defaultProfile.linux": "PowerShell",
    "python.analysis.useLibraryCodeForTypes": true
}