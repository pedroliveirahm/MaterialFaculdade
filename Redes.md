# Arquitetura de Computadores
* 
# Arquitetura em Camadas
* Camada OSI : Proporciona um modo estruturado de se organizar a Internet
    * Aplicação
    * ...
* Camada TCP-Ip
    * Aplicação
    * ...

# Ethernet
* È uma arquitetura de interconexão cabeada para redes locais
* A tecnologia executa as funções definidas nas camadas 1 e 2 da arquitetura TCP/IP.

# Tipos de Redes
* Sufixo `AN` - Àrea Network
* `PAN` - Rede de área pessoal : usada para que dispositivos se comuniquem dentro de uma distância bem limitada
* `LAN` - Rede local : interligam computadores dentro de um mesmo espaço físico
* `MAN` - Rede metropolitana : muito utilizado por empresas que possuem dois escritórios dentro de uma mesma cidade e desejam que os computadores permaneçam interligados
* `WAN` - Rede de longa distância (países e continentes)
* `WLAN` - Rede local sem fio
* `WMAN` - Rede metropolitana s/ fio
* `WWAN` - Rede de longa distância s/ fio
* `SAN` - Rede de área de armazenamento
# Protocolos - Conceitos
• Quando você usa a Internet, está usando uma variedade de protocolos diferentes. Para navegar, você usa HTTP. Para enviar e receber mensagens instantâneas, você usa XMPP.

• TCP / IP - Nome da família de protocolos
* Protocolo padrão da internet
* Dividido em aplicação, transporte, rede e interface

• Firewall - Mecanismo de segurança que controla o que entra e o que sai

# Camada de Aplicação

• Possuem um número (porta)

• HTTP (Hyper Text Transfer Protocol)
* Transferência de páginas 
* A URL é o endereço eletrônico da página de acesso

• HTTPS (Hyper Text Transfer Protocol Secure)
* Transferência de página seguras
* Esse protocolo é seguro pois possui metodos de criptografia

```bash
$Exemplo

https://www.github.com

https (protocolo) -> www (web) -> github.com (dominio)
```

• FTP (File Transfer Protocol)
* Conjunto de regras para transferência de arquivos do servidor para o computador cliente ou vice-versa (download/upload)

• SMTP | IMAP | POP - Estão ligados a correio eletrônico (emails)

* POP3: Recebe os email's

* SMTP: Envia as mensagens de email

* IMAP: Permite acessar as mensagens no servidor

• TELNET
* Usado para acesso remoto a uma máquina a distância (outra rede)

• DNS (Domain Name System)
* Conversão do nome de domínio em endereço IPV4

* IPV4 é o endereço padrão de uma máquina na rede (semelhante a um CPF), sendo o V4 a versão atual

* IPV6, após os esgotamento dos IPV4, veio o IPV6, usando o sistema HEXADECIMAL 

* Nós entendemos nomes, e a máquina, números

# Camada de Transporte

• DHCP - Também chamado de servidor DHCP
* Responsável pela distribuição dinânima do endereço IP, Máscara de sub-rede e o Gateway padrão

* Ao conectar a uma rede é recebido um número de IP designado pelo DHCP

• TCP ou UDP - Realiza o transporte de pacote de uma máquina a outra
* TCP: Realiza o transporte com a entrega garantida
* UDP: Realiza transporte de pacote sem garantia, tem maior velocidade

---
Made with by 💙 Pedro PC 👋 <a href="https://github.com/pedroliveirahm">Seen my GitHub</a>
* <strong>Fale comigo : <a href="https://bio.link/pedroliveirahm" target="_blank">Contato</a></strong>