# Redes de computadores

Conjunto de dispositivos interconectados por um meio de comunicação com **objetivo de compartilhar recursos.**

## Componentes
  - Dispositivos finais (hosts)
  - Dispositivos intermediários (switches, roteadores)
  - Meios de transmissão
  - Protocolos de comunicação
  - Serviços de rede (DNS, Web, E-mail)

## Meios de transmissão

Tabela: Meios de Transmissão – Guiados e Não Guiados

| **Tipo**                     | **Meio**                 | **Características**                                                                 | **Exemplos/Aplicações**                       |
|------------------------------|--------------------------|--------------------------------------------------------------------------------------|-----------------------------------------------|
| **Meios Guiados (Físicos)**  | **Par trançado (UTP/STP)** | - Dois fios de cobre entrelaçados<br>- UTP: sem blindagem<br>- STP: com blindagem    | Redes LAN, Ethernet (CAT5e, CAT6, CAT7)       |
|                              | **Cabo coaxial**         | - Condutor central + blindagem metálica<br>- Boa imunidade a ruídos                 | Redes antigas, TV a cabo, câmeras analógicas  |
|                              | **Fibra óptica**         | - Transmissão por pulsos de luz<br>- Imune a EMI<br>- Altíssima velocidade           | Backbone, data centers, operadoras            |
|                              | → Monomodo               | - Núcleo fino<br>- Longas distâncias<br>- Mais caro                                  | Redes troncais, interligação entre cidades    |
|                              | → Multimodo              | - Núcleo mais largo<br>- Curtas distâncias<br>- Mais barato                          | Ambientes internos, prédios corporativos      |
| **Meios Não Guiados (Sem fio)** | **Ondas de rádio**         | - Propagação por ar<br>- Sujeito a interferências<br>- Mobilidade                    | Wi-Fi, Bluetooth, 4G/5G                        |
|                              | **Infravermelho**        | - Comunicação ponto a ponto<br>- Não atravessa obstáculos                            | Controles remotos, sensores                   |
|                              | **Micro-ondas**          | - Linha reta (visada direta)<br>- Alta frequência                                    | Enlaces ponto-a-ponto, antenas parabólicas    |
|                              | **Satélite**             | - Comunicação via satélite geoestacionário<br>- Alta cobertura geográfica            | TV por assinatura, internet via satélite      |

### Par Trançado (UTP/STP)

Par trançado é um tipo de meio físico de transmissão, formado por **dois fios de cobre entrelaçados** (*twisted pairs*), geralmente usados em **redes locais (LAN)**. O entrelaçamento dos fios reduz a **interferência eletromagnética** (EMI) e a **diafonia** (*crosstalk*) entre pares.

Esse cabo pode ser de dois tipos principais:

| Tipo | Descrição |
|------|-----------|
| **UTP (Unshielded Twisted Pair)** | Par trançado **sem blindagem**, mais comum, menor custo e mais flexível |
| **STP (Shielded Twisted Pair)** | Par trançado **com blindagem**, possui proteção contra interferências externas (RFI/EMI), usado em ambientes com ruído elétrico |

- **Estrutura e Funcionamento**
  - **Fios de cobre:** Cada par é composto por dois fios de cobre isolados e entrelaçados. Em um cabo típico de rede, há **4 pares trançados** (8 fios no total).
  - **Trançamento:** O trançamento tem como objetivo:
    - **Reduzir interferências eletromagnéticas**
    - **Minimizar a diafonia** entre os pares

  - **Blindagem (STP)**
    No **STP**, cada par pode ter sua própria blindagem (individual) e/ou uma blindagem geral externa. Pode-se ter:
    - **FTP** (Foiled Twisted Pair): blindagem geral
    - **S/FTP**: blindagem geral + blindagem por par

- **Categorias de Cabo (Padronização ANSI/TIA/EIA)**
  As categorias indicam a **capacidade de transmissão de dados**, **frequência suportada** e aplicação recomendada. A seguir, as mais relevantes:

| Categoria | Tipo    | Velocidade                             | Frequência | Aplicação                                |
|-----------|---------|----------------------------------------|------------|------------------------------------------|
| **CAT5**  | UTP/STP | até 100 Mbps                           | 100 MHz    | Ethernet 100BASE-T                       |
| **CAT5e** | UTP/STP | até 1 Gbps                             | 100 MHz    | Gigabit Ethernet (1000BASE-T)            |
| **CAT6**  | UTP/STP | até 1 Gbps (a 100m) ou 10 Gbps (a 55m) | 250 MHz    | Redes Gigabit/10Gigabit                  |
| **CAT6a** | STP     | até 10 Gbps                            | 500 MHz    | Redes 10Gigabit (100 m)                  |
| **CAT7**  | STP     | até 10 Gbps                            | 600 MHz    | Alta interferência (uso profissional)    |
| **CAT8**  | STP     | até 25–40 Gbps                         | 2000 MHz   | Data centers, curta distância (até 30 m) |

> 🔍 **Observação**: A categoria 5e substituiu a CAT5 em aplicações modernas.

- **Aplicações em Cabeamento Estruturado (MARIN, 2009)**

    O par trançado é amplamente utilizado no **cabeamento horizontal** em sistemas de cabeamento estruturado. Deve-se considerar:
  - **Segmento máximo de 100 metros** (90m de cabo + 10m de patch cords)
  - Compatibilidade com normas **TIA/EIA-568-B** e **ISO/IEC 11801**
  - Requisitos de separação de cabos elétricos para evitar interferências

- **Vantagens e Desvantagens do Cabo de Par Trançado**
  - **Vantagens:**
    - Custo acessível
    - Facilidade de instalação e manutenção
    - Suporte a altas taxas de transmissão (CAT6+)
    - Compatível com topologia estrela
  - **Desvantagens**
    - Menor proteção contra interferências externas (UTP)
    - Distância limitada (100 metros sem repetidor)
    - Pode exigir blindagem adicional em ambientes industriais

- **Comparativo UTP vs STP**

  | Característica    | UTP                           | STP                                |
  |-------------------|-------------------------------|------------------------------------|
  | Custo             | Baixo                         | Médio/Alto                         |
  | Instalação        | Simples                       | Mais complexa                      |
  | Blindagem         | Não                           | Sim                                |
  | Imunidade a ruído | Menor                         | Maior                              |
  | Aplicações        | Escritórios, ambientes limpos | Ambientes industriais ou com ruído |


- **Questões comuns em prova**
> 1. Assinale a alternativa correta sobre o cabo de par trançado:  
> A) O cabo STP é mais barato que o UTP.  
> B) O CAT5e suporta até 10 Gbps a 100 metros.  
> C) O UTP não possui blindagem, sendo mais vulnerável a interferências.  
> D) O padrão CAT6 não pode ser usado em redes Gigabit.
>
> ✅ **Resposta correta: C**

## Classificação

### Escopo Geográfico
  
| Tipo | Sigla | Características |
|------|-------|------------------|
| Local | LAN | Pequenas áreas (escolas, escritórios) |
| Metropolitana | MAN | Áreas urbanas, campus universitários |
| Ampla | WAN | Grandes distâncias (Internet) |
| Sem fio | WLAN | Versão sem fio de LAN, padrão 802.11 |

####  LAN – Local Area Network

> **Tanenbaum (2011)**: LANs são projetadas para abranger distâncias curtas e possuem **altas taxas de transmissão** (tipicamente de 100 Mbps a 10 Gbps).

- Conecta dispositivos em **uma única localização física** (ex: escritório, escola, laboratório).
- Usa normalmente **Ethernet (IEEE 802.3)** ou **Wi-Fi (IEEE 802.11)**.
- **Gerência local** e **baixo custo de implantação**.
- Geralmente é **propriedade privada**.

#### MAN – Metropolitan Area Network

> **Soares, Lemos & Colcher (2001)**: MANs conectam várias LANs próximas entre si, como em **campi universitários**, **hospitais**, **órgãos públicos**, usando geralmente **fibra óptica**.

- Abrange **áreas urbanas** ou **cidades inteiras**.
- Usa tecnologias como **MPLS**, **Metro Ethernet** e **SONET/SDH**.
- Pode ser **administrada por operadoras** ou **instituições públicas**.
- Transmissão de **alta velocidade** e **média distância**.

#### WAN - Wide Area Network

> **Kurose & Ross (2014)**: WANs são responsáveis por **conectar redes LAN e MAN geograficamente distantes**, formando a base da **Internet**.

- Abrange **países, continentes ou o mundo inteiro**.
- Requer **roteadores**, **provedores de serviços** e protocolos como **IP/MPLS**.
- Menor velocidade e maior latência em relação às LANs.
- Ex: **Internet**, redes corporativas com filiais em diferentes estados ou países.

#### WLAN – Wireless Local Area Network

> **Torres (2009)**: WLANs são **LANs que utilizam meios não guiados**, geralmente ondas de rádio, para comunicação.

- Baseada no padrão **IEEE 802.11 (Wi-Fi)**.
- Permite **mobilidade** dos usuários sem cabeamento físico.
- Usa técnicas como **CSMA/CA** para acesso ao meio.
- Segurança é um aspecto crítico (WPA2, WPA3).

### Arquitetura

> A arquitetura de redes define a **organização lógica das funções de comunicação** entre dispositivos conectados em rede. As duas formas clássicas são: **Cliente-Servidor** e **Ponto-a-Ponto (P2P)**.

#### Cliente-servidor

> **Kurose & Ross (2014)**: A arquitetura cliente-servidor caracteriza-se por um dispositivo (cliente) requisitando serviços a outro dispositivo centralizado (servidor).

- **Conceito** 

  - A rede é organizada em torno de **servidores centrais**, que oferecem recursos ou serviços (como arquivos, páginas web, bancos de dados).
  - Os **clientes** solicitam esses serviços, e o **servidor os processa e responde**.

- **Características**

| Característica      | Descrição                                              |
|---------------------|--------------------------------------------------------|
| Papel distinto      | Cliente consome; servidor fornece.                     |
| Centralização       | Os dados e o controle estão centralizados no servidor. |
| Segurança           | Maior controle de acesso e autenticação.               |
| Escalabilidade      | Limitada, pois o servidor pode se tornar gargalo.      |
| Exemplo de serviços | HTTP (web), FTP, banco de dados, e-mail.               |

- **Exemplos práticos**

  - Acesso a um site (o navegador é o cliente, o servidor web responde).
  - Sistemas empresariais centralizados (ERP, sistemas de ponto eletrônico).
  - Aplicações de correio eletrônico (SMTP/IMAP).

- **Vantagens e Desvantagens**

| Vantagens                               | Desvantagens                              |
|-----------------------------------------|-------------------------------------------|
| Maior controle e segurança centralizada | Dependência de um único ponto: o servidor |
| Gerenciamento e backup mais fáceis      | Custos de manutenção e infraestrutura     |
| Escalabilidade com servidores dedicados | Gargalos podem surgir com muitos clientes |

> **Tanenbaum (2011)** destaca que, em redes corporativas, o modelo cliente-servidor é preferido pela **previsibilidade e controle administrativo**.

#### Ponto-a-ponto (P2P)

> **Kurose & Ross (2014)**: Em uma arquitetura ponto-a-ponto, os **nós funcionam simultaneamente como clientes e servidores**.

- **Conceito**

  - Todos os dispositivos conectados à rede podem **compartilhar recursos diretamente uns com os outros**.
  - Não há servidor centralizado; a comunicação é distribuída entre os pares (peers).

- **Características**

| Característica             | Descrição                                                       |
|----------------------------|-----------------------------------------------------------------|
| Descentralização           | Todos os nós podem prover e consumir serviços.                  |
| Distribuição de carga      | Compartilhamento da carga de trabalho entre os peers.           |
| Autonomia                  | Cada usuário gerencia seus próprios dados.                      |
| Eficiência em larga escala | Útil em redes com muitos dispositivos e grande volume de dados. |

- **Exemplos práticos**

  - Compartilhamento de arquivos via BitTorrent.
  - Redes Gnutella, eMule, Kazaa (redes P2P clássicas).
  - Aplicações modernas de blockchain (ex: IPFS, Ethereum).

- **Vantagens e Desvantagens**

| Vantagens                                          | Desvantagens                                           |
|----------------------------------------------------|--------------------------------------------------------|
| Escalabilidade horizontal                          | Difícil de controlar segurança e integridade dos dados |
| Menor custo de infraestrutura                      | Gestão e suporte descentralizados                      |
| Alta disponibilidade (não há ponto único de falha) | Performance pode ser imprevisível                      |

> **Torres (2009)** observa que o modelo P2P é eficiente para **compartilhamento de arquivos em grande escala**, mas apresenta **riscos quanto à segurança** e integridade.

##### Comparativo Resumido (Cliente-Servidor x | Ponto-a-Ponto (P2P)

| Aspecto              | Cliente-Servidor                          | Ponto-a-Ponto (P2P)                            |
|----------------------|--------------------------------------------|------------------------------------------------|
| Centralização        | Sim (servidor central)                     | Não (nós iguais)                               |
| Controle de acesso   | Centralizado                               | Distribuído                                    |
| Custo de implantação | Alto (infraestrutura de servidor)          | Baixo (compartilhamento entre peers)           |
| Escalabilidade       | Limitada ao servidor                       | Alta, distribuída entre os nós                 |
| Confiabilidade       | Sujeita a falha do servidor                | Resiliente, sem ponto único de falha           |
| Exemplos             | Web, e-mail, bancos de dados               | BitTorrent, blockchain, Gnutella               |

- **Questões**
Com relação às arquiteturas de rede, analise as afirmativas a seguir:

1. Na arquitetura cliente-servidor, os dispositivos clientes e servidores desempenham papéis bem definidos, sendo o servidor responsável por prover serviços centralizados, como e-mail ou banco de dados.
2. Em uma rede ponto-a-ponto (P2P), não existe hierarquia entre os dispositivos conectados, permitindo que qualquer nó atue como servidor e cliente simultaneamente.
3. Redes ponto-a-ponto são mais seguras e fáceis de gerenciar do que redes cliente-servidor, pois eliminam a necessidade de um servidor centralizado.

Assinale a alternativa correta:

A) Apenas as afirmativas 1 e 2 estão corretas.
B) Apenas as afirmativas 1 e 3 estão corretas.
C) Apenas as afirmativas 2 e 3 estão corretas.
D) Todas as afirmativas estão corretas.
E) Nenhuma afirmativa está correta.

✅ Gabarito: A


## Topologias de rede

A **topologia de rede** define a forma como os dispositivos (nós) estão **fisicamente ou logicamente organizados** dentro da rede. As escolhas de topologia impactam diretamente na **performance**, **resiliência**, **custo** e **facilidade de manutenção** da rede.

  - **Barramento (Bus)**: um único cabo conecta todos os nós.
  - **Anel (Ring)**: conexão circular entre os nós.
  - **Estrela (Star)**: todos os dispositivos conectam a um ponto central.
  - **Malha (Mesh)**: todos os nós conectados entre si.
  - **Árvore (Tree)**: hierarquia de dispositivos.
  - **Híbrida**: combinação de topologias anteriores.

![img.png](img.png)

### Barramento (Bus)

> **Tanenbaum (2011)**: A topologia em barramento é uma das mais antigas e simples. Todos os dispositivos compartilham um **único meio de transmissão** (cabo principal).

- **Características**
  - Todos os dispositivos são ligados a um **único cabo troncal** (backbone).
  - Transmissão ocorre em **difusão (broadcast)**.
  - Requer **terminadores** nas extremidades do cabo para evitar reflexões.

- **Vantagens**
  - Baixo custo de instalação.
  - Pouco cabeamento.

- **Desvantagens**
  - **Baixa escalabilidade** (quanto mais dispositivos, mais colisões).
  - **Difícil de diagnosticar falhas**.
  - Uma falha no cabo principal derruba toda a rede.

- **Aplicações históricas**
  - Redes **Ethernet 10BASE-2 / 10BASE-5**.

### Anel (Ring)

> **Torres (2009)**: Na topologia em anel, os dispositivos são conectados de forma **circular**, e os dados circulam em um único sentido ou ambos (em caso de anel duplo).

**Características**
  - Cada nó é conectado ao **vizinho anterior e ao próximo**, formando um círculo fechado.
  - A transmissão segue de nó em nó até chegar ao destino.
  - Em algumas implementações usa-se **token** para controlar o envio (ex: Token Ring da IBM).

**Vantagens**
  - Ordenamento natural do tráfego.
  - Reduz colisões de dados com uso de token.

**Desvantagens**
  - A falha de um único nó ou enlace **pode derrubar toda a rede** (salvo uso de anel redundante).
  - Dificuldade de reconfiguração.

### Estrela (Star)

> **Kurose & Ross (2014)**: É a topologia predominante em redes modernas (Ethernet com switches), onde todos os nós se conectam a um **ponto central**.

**Características**
  - Todos os dispositivos são conectados a um **ponto central** (hub ou switch).
  - A comunicação passa **obrigatoriamente pelo ponto central**.

**Vantagens**
  - **Fácil de instalar, configurar e diagnosticar problemas**.
  - Falha em um cabo afeta apenas o nó correspondente.
  - Alto desempenho com switches modernos.

**Desvantagens**
  - Dependência do **ponto central** (ponto único de falha).

**Aplicações**
  - **Ethernet moderna (100BASE-T, 1000BASE-T)**.
  - Redes corporativas e residenciais.

### Malha (Mesh)

> **Soares, Lemos & Colcher (2001)**: Na topologia em malha, cada dispositivo é conectado a **todos os outros dispositivos** da rede.

**Características**
  - Pode ser **completa** (todos os pares conectados) ou **parcial**.
  - Comunicação direta entre pares.
  - Tolerância a falhas muito elevada.

**Vantagens**
  - **Alta disponibilidade** e **resiliência**.
  - Roteamento múltiplo e eficiente.

**Desvantagens**
  - **Alto custo e complexidade** (crescimento exponencial de enlaces).
  - Instalação e manutenção complexas.

**Aplicações**
  - Backbones de redes críticas.
  - Redes de sensores sem fio (em malha parcial).

### Árvore (Tree)

> **Torres (2009)**: Topologia em **forma hierárquica**, combinando aspectos de **estrela** e **barramento**.

**Características**
  - Nós organizados de forma **hierárquica**, como em uma **árvore genealógica**.
  - Usa **switches ou roteadores intermediários**.

**Vantagens**
  - **Fácil de expandir**.
  - Estrutura organizada para grandes redes.

**Desvantagens**
  - A falha de um nó de nível superior pode afetar os nós subordinados.

**Aplicações**
  - **Redes corporativas** e **escolares** com múltiplos andares ou setores.

### Híbrida

> **Tanenbaum (2011)**: A topologia híbrida **combina duas ou mais topologias** para atender requisitos específicos de uma organização.

**Características**
  - Adaptações de topologias como estrela, anel, barramento, etc.
  - Flexível e personalizável.

**Vantagens**
  - **Aproveita os pontos fortes** das topologias combinadas.
  - Permite **ajustes conforme a necessidade da organização**.

**Desvantagens**
  - Planejamento e manutenção mais complexos.
  - Pode exigir diferentes tecnologias e equipamentos.

**Aplicações**
  - **Ambientes corporativos heterogêneos**.
  - Grandes redes com múltiplas filiais.

**Comparativo Resumido**

| Topologia  | Vantagens principais                 | Desvantagens principais                            |
|------------|--------------------------------------|----------------------------------------------------|
| Barramento | Simples, econômica                   | Colisões, difícil de diagnosticar, pouco escalável |
| Anel       | Ordenamento do tráfego, sem colisões | Uma falha derruba tudo, difícil de manter          |
| Estrela    | Fácil de gerenciar, falha isolada    | Ponto central é crítico                            |
| Malha      | Alta resiliência e redundância       | Custo e complexidade elevados                      |
| Árvore     | Boa organização e expansão           | Dependência de nós superiores                      |
| Híbrida    | Flexível, adaptável                  | Mais complexa para planejar e manter               |


- **Infraestrutura e organização**
  - Equipamentos de Rede
  
    | Equipamento | Função |
    |------------|--------|
    | Hub | Repetidor; envia dados para todos |
    | Switch | Comutador; filtra pacotes por MAC |
    | Roteador | Encaminha pacotes entre redes |
    | Access Point | Permite acesso wireless à re

  - Modelos de Referência

    - Modelo OSI (ISO/IEC 7498)
      ```
      1. Física
      2. Enlace
      3. Rede
      4. Transporte
      5. Sessão
      6. Apresentação
      7. Aplicação
      ```

    - **Modelo TCP/IP**
      ```
      1. Acesso à Rede
      2. Internet
      3. Transporte
      4. Aplicação
      ```
      
    - **Endereçamento IP**
      ```
      IPv4: 32 bits (ex: 192.168.0.1)
      IPv6: 128 bits (ex: 2001:db8::1)
      ```

  - Endereçamento e Protocolos

    - Protocolos importantes:
    
    | Protocolo | Finalidade |
    |----------|------------|
    | HTTP/HTTPS | Acesso à web |
    | FTP/SFTP | Transferência de arquivos |
    | SMTP/POP3/IMAP | E-mail |
    | TCP/UDP | Transporte de dados |
    | ICMP | Diagnóstico (ping) |
    | DNS | Resolução de nomes |
    | DHCP | Atribuição dinâmica de IP |

### Redes de computadores e sistemas distribuídos: arquiteturas de rede

### Equipamentos de interconexão e transmissão de redes de computadores
- Hubs
- Repetidores
- Switches
- roteadores

### Funcionamento e aplicação dos Modelos de referência ISO/OSI e TCP/IP

### Arquitetura e pilhas de protocolos TCP/IP
- camada de rede (IPv4 eIPv6) conceitos básicos de endereçamento e roteamento; 
- camada de transporte (TCP e UDP)
- níveisde aplicação TCP/IP:
  - FTP
  - SSH
  - DNS
  - NFS
  - TELNET
  - SMTP
  - HTTP
  - HTTPS
  - LDAP
  - IPSEC
  - SNMP
  - NAT
  - SSL
  - DNS
  - RDP
  - DHCP

---

## Infraestrutura e Sistemas Operacionais
### Gerenciamento e monitoramento de equipamentos de rede
### Ativos de rede
### Passivos de rede
### Softwares e métricas de monitoramento

## Gerenciamento e monitoramento de equipamentos de rede
### Conhecimento sobre ferramentas e métricas de monitoramento

## Virtualização de Servidores

## Virtual Lans (VLAN)

## Cabeamento estruturado
### Conceitos
### Técnicas e boas práticas de instalação

## Sistemas de comunicação óptica 
### técnicas e práticasde instalação

## Arquitetura das redes de comunicação

## Armazenamento
### SAN
### NAS
### RAID

## Noções de Backup
## Armazenamento
### Meios de armazenamento
### Sistemas e tipos de backup
### planos de contingência ferramentas

## Administração de sistemas operacionais
### LINU
### MS-WINDOWS

## Configuração e administração de servidores Windows Server 2016 e Linux

## Configuração e administração de serviços 
### AD
### DNS
### DHCP
### GPO

## Administração de usuários

## Noções de administração de serviços:
### apache
### NFS
### Samba
### SSH
### cron
### sistemas de arquivos

## Noções de Virtualização
### Hypervisors
### containers

## Tecnologia de roteamento de pacotes

## Gerência de redes

## Auditoria de redes

## Detecção e correço de problemas de nível físico e lógico; Segurança de redes

## Noções de tecnologias Voip e SIP

---

## Segurança da Informação

### conceitos básicos de confidencialidade, integridade e disponibilidade

### Segurança e proteção de redes

### Firewall
- conceito de firewall
- suas funções
- tipos

### Noções decriptografia

## Leis e Regulamentações
### Lei Geral de Proteção de Dados (Lei nº 13.709, de 14 de agosto de 2018, e suas alterações)
### Contratação de soluções de Tecnologia da Informação e Comunicação.




```javascript
console.log('Olá mundo!');
