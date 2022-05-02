# Linux Fedora
Qué hacer después de instalar Fedora

## Asignar contraseña a root
Es necesario asignarle una contraseña al usuario root después de iniciar el SO, ya que durante la instalación no solicita la contraseña para el usuario root

```bash
sudo passwd root
```

## Actualizando Fedora

```bash
sudo dnf -y update
```

## Repositorios extra
Es muy importate contar con este tipo de repositorios ya que muchas de las apps que solemos utilizar los linuxeros no se encuentran en los repositorios oficiales.

A) Fedora Workstation
De la manera siguiente instalas los repositorios de la Fedora Workstation.

```bash
sudo dnf install fedora-workstation-repositories
```

Muchas de las apps que son muy útiles dentro del entorno Fedora Workstation vienen en estos repositorios.

B) RPMFusion en Fedora 35
Con estos repositorios puedes acceder a apps que no vienen comúnmente en los repositorios oficiales de Fedora.

```bash
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

C) United RPMs
Estos otros repositorios aun enriquecen más el campo de apps que podrás instalar en tu Fedora 35.

```bash
sudo rpm --import https://raw.githubusercontent.com/UnitedRPMs/unitedrpms/master/URPMS-GPG-PUBLICKEY-Fedora
```

Ahora ejecutas el siguiente comando,

```bash
sudo dnf -y install https://github.com/UnitedRPMs/unitedrpms/releases/download/17/unitedrpms-$(rpm -E %fedora)-17.fc$(rpm -E %fedora).noarch.rpm
```

https://www.yocupicio.com/que-hacer-despues-de-instalar-fedora-35/

## GNOME Shell Extensions

```bash
sudo dnf -y install gnome-shell-extension gnome-tweak-tool chrome-gnome-shell
```

## Gnome Console

```bash
sudo dnf install gnome-console
```

## ZSH para la terminal

```bash
sudo dnf -y install git zsh util-linux-user
```

```bash
git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
```

```bash
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

```bash
cp ~/.zshrc ~/.zshrc.orig
```

```bash
sudo chsh -s /bin/zsh user-name
```
