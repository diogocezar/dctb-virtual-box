# Virtual Box Hacks

##Alterando o UUID

```
C:\Program Files\Oracle\VirtualBox>
VBoxManage.exe internalcommands sethduuid "G:\Máquinas Virtuais\batvirtual.vdi"
VBoxManage.exe internalcommands sethduuid "G:\Máquinas Virtuais\batretroarch.vdi"
VBoxManage.exe internalcommands sethduuid "G:\Máquinas Virtuais\batdocker.vdi"
VBoxManage.exe internalcommands sethduuid "C:\VirtualMachines\batbuster.vdi"
```

## Diminuindo o tamanho

Ref: http://www.mundomoderno.net/reduza-a-imagem-do-virtualbox/

```
sudo dd if=/dev/zero of=/emptyfile bs=1M
sudo rm -rf /emptyfile
```

Agora encerre o sistema operacional na maquina virtual e feche a maquina virtual (VirtualBox).

Feito isso, agora, reduza a imagem! Para tanto para tanto abra o processador de comandos (CMD na busca) e da pasta onde esta o VirtualBox execute a ferramenta VBoxManage com a modificação de disco, modifyhd.

```
C:\Program Files\Oracle\VirtualBox>
VBoxManage modifyhd minhaImagem.vdi --compact
VBoxManage.exe modifyhd "G:\Máquinas Virtuais\batvirtual.vdi" --compact
VBoxManage.exe modifyhd "C:\VirtualMachines\batbuster.vdi" --compact
```
