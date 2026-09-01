

Docs:


## Templates 

- Instalar ISOS no proxmox e cria-las
- Instalar os serviços de Open SSH (No ubuntu server existe essa opção de download) e Cloud-Init
- Transportar sua chave ssh via github, caso tenha várias crie uma especifica e edite o arquivo: ~/.ssh/authorized_keys
- Excluir chaves ssh host (cd etc/ssh > sudo rm ssh_host_*)
- Excluir id do Host (cat /etc/machine-id > sudo truncate -s 0 /etc/machine-id)
- Verificar se tem link simbolico com: - ls -l /var/lib/dbus/machine-id | sido ln -s /etc/lib/dbus/machine-id
- Instalar o Agente QEMU
- Ativar o Agente QEMU na interface do Proxmox
- Limpar a vm com apt clean e apt autoremove e cloud-init clean
- Instalar quaisquer aplicativos ou processo/configurações desejadas 
- Desligar a máquina sudo poweroff
- Na interface do proxmox clicar com o botão direito > convert to template
- Dentro do template ir em Hardware > remover a ISO de instalação da imagem
- Adicionar na aba de Hardware a opção cloud-Init
- Na aba de cloud init > IP Config > Edit > Selecionar as duas opções DHCP

## Como usar o template:

- Clique botão direito no seu template > Clone > Full clone para que seja totalmente independente
- Dentro do clone da VM:

- Alterar o ID da máquina nova > sudo nano /etc/hostname
- Alterar o nome em sudo nano /etc/hosts
- Reboot para confirmar que as alterações foram devidamente aplicadas
- 
