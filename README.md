# Configurações do Teclado Led

Este é um repositório no GitHub contendo arquivos de configuração para o teclado LED em sistemas operacionais baseados em Linux, como Arch, Ubuntu e Debian. Esses arquivos podem ser úteis para usuários cujos teclados apresentam problemas com a iluminação do LED. Use-os com cautela, somente se for necessário.

## Bases Testadas

- Ubuntu. (Pop Os)
- Debian. (Kali Linux, Parrot Os)
- ArchLinux. (Archcraft, ArcoLinux, Arch Gui, Manjaro)

## Cuidado

Suporte a teclado brasileiros abnt e abnt2 100% funcionando, Teclado americanos não testados.

### Pré Requisitos

Esteja ciente que esses arquivos irão substituir os arquivos atuais de configuração do seu teclado que vem padrão no pós instalação.

- Realizar Backups dos seus arquivos originais.

### Realize o Backup

**Crie uma Pasta para guardar os arquivos**

```sh
  mkdir -p $HOME/Backups/Teclado-Backup
```

**Copie os Arquivos Originais para a pasta de backup**

```sh
  cp -r /usr/share/X11/xkb/symbols/* $HOME/Backups/Teclado-Backup/
 ```

### Passo a Passo

**Clone o Repositório do Github em alguma pasta** (Preferência na Pasta de Downloads)

```sh
  git clone https://github.com/akicodeoficial/configuracoes-teclado-led.git
```

**Copie os Arquivos de Configurações para a Pasta do sistema**

```sh
  sudo cp files/{us,br} /usr/share/X11/xkb/symbols/
```

### Reverter

Siga os passos abaixo para reverter caso tenha dado errado.

```sh
  cp $HOME/Backups/Teclado-Backup/{us,br} /usr/share/X11/xkb/symbols/
 ```
 
 ### Finalizando
 
 Ao realizar o passo de configuração, você deve reiniciar a máquina ou fazer logout do usuário. Para reverter é o mesmo caso, reiniciar ou faz logout.

![Hatsune Miku](./background.jpg)
