### Sumário
[Aula 01](#aula-01)
[Aula 02](#aula-02)
[Aula 03](#aula-03)
[Aula 04](#aula-04)

# Aula 01 
## Ataque DDOS
* Tem como objetivo causar uma sobrecarga no servidor através de várias requisições, de forma que o programa fique fora do ar para os demais usuários 
    * Nível de complexidade : Média-baixa
### Como é Feito
* Para o hacker conseguir fazer milhares de requisições em um servidor, ele toma posse de determinadas máquinas e/ ou redes
* Para tanto, uma botnet - rede de computadores infectada que podem ser controladas remotamente - usa um malware em segundo plano em milhares de computadores infectados, e em dia e hora sincronizados, fazem requisições sucessivas para o servidor
## Seg.Info
### O Que é ?
* Segurança : é a `sensação` de estar livre de perigos, riscos e incertezas
* È a proteção de um conjunto de informações, de modo a preservar o seu `valor` para um indivíduo ou uma organização
### Propriedades Básicas - C.I.D.A.L
* `Confidencialidade` : propriedade particular não disponível a divulgação
* `Integridade` :  de natureza íntegra
* `Disponibilidade` : resistentes a falhas de hardware, software, energia e outros
* `Autenticidade` : que provêm de fontes conhecidas e confiáveis
* `Legalidade` : dentro do permitido
### Regulamentação
* ABNT NBR ISO/IEC 27002:2013 - Código de prática para controles da segurança da informação
### O que Queremos Proteger 
* O Dado (40), que através de um contexto, gera uma informação (temperatura do paciente = 40graus), que gera um conhecimento (paciente está com febre), levando a uma ação (tomar remédio)
# Aula 02
## Segurança Física
* Tem como objetivo proteger `equipamentos` e `informações` contra usuários que não possuem autorização de acessa-los
* Tradicionalmente, a segurança física é provida pela equipe de redes ou gestão de ativos
### Tópicos
* `Proteção de documentos`
* `Furto`
* `Vandalismo`
* `Sabotagem`
* `Acesso não autorizado`
* `Acidentes` e `desastres naturais`
### Sala Cofre
* Ela é uma unidade de armazenagem segura para hardwares, classificada como resistente por diversos métodos
* NBR 15.247/2004 - Aquela que protege os equipamentos de informática críticos e dados armazenados
    * Composta por pilares, portas e paredes que não permitem a passagem de fogo
    * As suas entradas precisam ter dispositivos de fechamento automático e também aberturas para casos de incêndio
    * Os materiais não podem ser tóxicos
    * Possuir NOC - Centro de Operações de Rede
#### Utilidade de Apoio
* Energia de Emegência
     * Baterias
     * Fonte initerrupta de alimentação
     * Gerador de energia
* Resfriamento
    * Em sala de servidores, o ar tem que ser resfriado, desumificado e filtrado
### Sensores de Segurança
* Detecção passiva por infravermelho
* Câmeras
* Sensor de vibração
* Sensores de quebra de vidro
* Contato magnético - detecta quando porta ou janela é aberta
### Anéis de Proteção
* Anel externo : área em torno das intalações
    * Proteções arquitetônicas como : cercas, arame farpado e muros.
    * As barreiras devem empregar uma identificação pessoal e/ou eletrônica (cartão de acesso, verificação biométrica)
* O prédio : o acesso às instalações
    * Proteção arquitetônica: incluem vidro resistente, portas com estrutura correta e mecanismos que evitem o arrombamento fácil
* O local de trabalho : as salas dentro das instalações, também conhecido como anel interno
* O objeto : o ativo que deve ser protegido
### Controles de Entrada
A área entre o anel externo e o anel interno pode ser usada para vigilância, por um guarda de segurança, e para serviços auxiliares(estacionamento)
* Devem ser bem iluminadas e resguardadas por câmeras de vigilância
### Identificação por Radiofrequência (RFID)
* Método de identificação automática através de sinais de rádio
### Dicas de Controle de Acesso
* Foto na credencial
* Ter um único usuário
* Não coloque o nome ou logotipo da empresa, usar estilo neutro
* Tanto funcionários quanto visitantes devem ser obrigados a usar uma credencial de forma visível
### Médidas de Seg Adicionais
* Algo que você saiba (PIN)
* Algo que você possui (Cartão)
* Algo que só tenha em você (Biometria)
## Segurança Lógica
* Tem como objetivo proteger o sistema, dados e programas contra tentativas de acesso, tanto de pessoas quanto programas, não autorizados
* A identificação e autenticação do usuário é feita pelo processo de login
### Médidas de Seg. Lógica
* Firewall de hardware e softwares
* Senhas de acesso
* Sistema de detecção de intrusão
* Redes privadas
* Criptografia
* Antivirus
* Protocolos de acesso e uso
## Seg. Lógica vs Seg. Física
* Tópicos de convergência 
    * A segurança da organização começa pelo ambiente físico, dando ênfase no controle de acesso
    * A segurança lógica deve ocorrer depois da segurança física
    * Ambas devem se complementarem de acordo com suas responsabilidades