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

| **Tipo**                        | **Meio**                   | **Características**                                                               | **Exemplos/Aplicações**                      |
|---------------------------------|----------------------------|-----------------------------------------------------------------------------------|----------------------------------------------|
| **Meios Guiados (Físicos)**     | **Par trançado (UTP/STP)** | - Dois fios de cobre entrelaçados<br>- UTP: sem blindagem<br>- STP: com blindagem | Redes LAN, Ethernet (CAT5e, CAT6, CAT7)      |
|                                 | **Cabo coaxial**           | - Condutor central + blindagem metálica<br>- Boa imunidade a ruídos               | Redes antigas, TV a cabo, câmeras analógicas |
|                                 | **Fibra óptica**           | - Transmissão por pulsos de luz<br>- Imune a EMI<br>- Altíssima velocidade        | Backbone, data centers, operadoras           |
|                                 | → Monomodo                 | - Núcleo fino<br>- Longas distâncias<br>- Mais caro                               | Redes troncais, interligação entre cidades   |
|                                 | → Multimodo                | - Núcleo mais largo<br>- Curtas distâncias<br>- Mais barato                       | Ambientes internos, prédios corporativos     |
| **Meios Não Guiados (Sem fio)** | **Ondas de rádio**         | - Propagação por ar<br>- Sujeito a interferências<br>- Mobilidade                 | Wi-Fi, Bluetooth, 4G/5G                      |
|                                 | **Infravermelho**          | - Comunicação ponto a ponto<br>- Não atravessa obstáculos                         | Controles remotos, sensores                  |
|                                 | **Micro-ondas**            | - Linha reta (visada direta)<br>- Alta frequência                                 | Enlaces ponto-a-ponto, antenas parabólicas   |
|                                 | **Satélite**               | - Comunicação via satélite geoestacionário<br>- Alta cobertura geográfica         | TV por assinatura, internet via satélite     |

### Par Trançado (UTP/STP)

Par trançado é um tipo de meio físico de transmissão, formado por **dois fios de cobre entrelaçados** (*twisted pairs*), geralmente usados em **redes locais (LAN)**. O entrelaçamento dos fios reduz a **interferência eletromagnética** (EMI) e a **diafonia** (*crosstalk*) entre pares.

Esse cabo pode ser de dois tipos principais:

| Tipo                              | Descrição                                                                                                                       |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| **UTP (Unshielded Twisted Pair)** | Par trançado **sem blindagem**, mais comum, menor custo e mais flexível                                                         |
| **STP (Shielded Twisted Pair)**   | Par trançado **com blindagem**, possui proteção contra interferências externas (RFI/EMI), usado em ambientes com ruído elétrico |

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
  
| Tipo          | Sigla | Características                       |
|---------------|-------|---------------------------------------|
| Local         | LAN   | Pequenas áreas (escolas, escritórios) |
| Metropolitana | MAN   | Áreas urbanas, campus universitários  |
| Ampla         | WAN   | Grandes distâncias (Internet)         |
| Sem fio       | WLAN  | Versão sem fio de LAN, padrão 802.11  |

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

| Aspecto              | Cliente-Servidor                  | Ponto-a-Ponto (P2P)                  |
|----------------------|-----------------------------------|--------------------------------------|
| Centralização        | Sim (servidor central)            | Não (nós iguais)                     |
| Controle de acesso   | Centralizado                      | Distribuído                          |
| Custo de implantação | Alto (infraestrutura de servidor) | Baixo (compartilhamento entre peers) |
| Escalabilidade       | Limitada ao servidor              | Alta, distribuída entre os nós       |
| Confiabilidade       | Sujeita a falha do servidor       | Resiliente, sem ponto único de falha |
| Exemplos             | Web, e-mail, bancos de dados      | BitTorrent, blockchain, Gnutella     |

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


## Infraestrutura e organização

> Com base no modelo **OSI** e no **modelo TCP/IP**, os equipamentos de rede atuam em diferentes camadas, com finalidades específicas no tráfego de dados, controle de rede e conectividade.

### Tabela Comparativa

| **Equipamento**  | **Função**                                            | **Camada OSI**    | **Camada TCP/IP** | **Gerenciamento**    | **Velocidade comum**           | **Observações**                                       |
|------------------|-------------------------------------------------------|-------------------|-------------------|----------------------|--------------------------------|-------------------------------------------------------|
| **Hub**          | Repetidor físico; envia dados para todas as portas    | Camada 1 (Física) | Acesso à Rede     | Não gerenciável      | 10/100 Mbps                    | Obsoleto, causa colisões, sem inteligência            |
| **Switch**       | Comutador; encaminha quadros com base no endereço MAC | Camada 2 (Enlace) | Acesso à Rede     | Pode ser gerenciável | 100 Mbps, 1 Gbps, 10 Gbps      | Reduz colisões, suporta VLANs (gerenciável)           |
| **Roteador**     | Encaminha pacotes entre redes distintas (IP)          | Camada 3 (Rede)   | Internet          | Gerenciável          | 100 Mbps a 10 Gbps             | Usa tabelas de roteamento e protocolos como OSPF, BGP |
| **Access Point** | Permite conexões sem fio a uma rede cabeada           | Camada 2 (Enlace) | Acesso à Rede     | Pode ser gerenciável | 300 Mbps a +1 Gbps (Wi-Fi 5/6) | Opera em 2,4 GHz e 5 GHz; suporta SSID, autenticação  |


### Hub

> **Tanenbaum (2011)**: Equipamento simples que apenas **repete os sinais elétricos** recebidos em uma porta para todas as outras.

- Opera na **camada física (OSI – camada 1)**.
- Não tem inteligência de rede (não lê endereços MAC).
- Sujeito a **colisões** (CSMA/CD em Ethernet legado).
- Usado em topologias **estrela com lógica de barramento**.
- Foi substituído por **switches** em redes modernas.

### Switch

> **Kurose & Ross (2014)**: Atua na **comutação de quadros** com base no endereço MAC de destino.

- Opera na **camada de enlace (OSI – camada 2)**.
- Mantém uma **tabela MAC** para encaminhamento eficiente.
- Reduz o domínio de colisão (uma porta = um domínio).
- **Switches gerenciáveis** suportam:
  - VLANs (IEEE 802.1Q)
  - SNMP para monitoramento
  - QoS, espelhamento de portas

> **Torres (2009)** destaca que switches modernos podem ter funções da camada 3 (roteamento interno).

### Roteador

> **Kurose & Ross (2014)**: Atua na **camada de rede (OSI – camada 3)**, com base em **endereços IP**.

- Encaminha pacotes entre **redes diferentes**.
- Mantém **tabelas de roteamento** (estáticas e dinâmicas).
- Utiliza protocolos como:
  - **OSPF**, **BGP**, **RIP**
- Realiza funções como:
  - NAT (Network Address Translation)
  - DHCP (servidor/cliente)
  - Firewall (em roteadores avançados)
- É essencial em redes domésticas e corporativas (ex: roteador Wi-Fi).

### Access Point (AP)

> **Torres (2009)**: Permite **acesso sem fio** a uma rede cabeada, funcionando como uma **ponte** entre dispositivos Wi-Fi e a LAN com fio.

- Opera na **camada de enlace (OSI – camada 2)**.
- Suporte a padrões:
  - **IEEE 802.11a/b/g/n/ac/ax** (Wi-Fi 4 a 6)
- Configurações típicas:
  - SSID (nome da rede)
  - Criptografia (WPA2, WPA3)
  - Controle de acesso por MAC
- Pode ser:
  - **Autônomo** (stand-alone)
  - **Controlado** (por controladora wireless)

```
Questão 1

Com relação aos equipamentos utilizados na infraestrutura de redes de computadores, analise as afirmações a seguir:
1. O switch opera, por padrão, na camada de enlace do modelo OSI e realiza comutação com base nos endereços MAC dos dispositivos conectados.
2. O roteador atua na camada de transporte, sendo responsável por controlar o fluxo de pacotes entre dispositivos da mesma rede local.
3. O hub é um equipamento inteligente que realiza encaminhamento de pacotes com base em endereços IP.
4. O Access Point (AP) possibilita a conexão de dispositivos sem fio a uma rede com fio, funcionando como uma ponte na camada de enlace.

Assinale a alternativa correta:

A) Apenas as afirmativas 1 e 2 estão corretas.
B) Apenas as afirmativas 1 e 4 estão corretas.
C) Apenas a afirmativa 2 está correta.
D) Apenas as afirmativas 3 e 4 estão corretas.
E) Todas as afirmativas estão incorretas.

Gabarito: B
```

### CSMA/CD x CSMA/CA


## Modelo OSI (ISO/IEC 7498)

> O modelo OSI (Open Systems Interconnection), desenvolvido pela **ISO** em parceria com a **IEC**, define uma arquitetura em **7 camadas** para a **comunicação em redes de computadores**. Ele promove **interoperabilidade**, **padronização de protocolos** e **modularidade** na construção de redes.

### Estrutura Geral

| Camada | Nome            | Função principal                        | Unidade de dados |
|--------|-----------------|-----------------------------------------|------------------|
| 7      | Aplicação       | Interface com o usuário final           | Dados            |
| 6      | Apresentação    | Codificação, criptografia e compressão  | Dados            |
| 5      | Sessão          | Gerência de conexões e sessões          | Dados            |
| 4      | Transporte      | Controle fim a fim, confiabilidade      | Segmentos        |
| 3      | Rede            | Endereçamento lógico e roteamento       | Pacotes          |
| 2      | Enlace de Dados | Endereçamento físico, detecção de erros | Quadros (Frames) |
| 1      | Física          | Transmissão de bits no meio físico      | Bits             |

### Camada 1 - Física 

> **Tanenbaum (2011)**

- Responsável pela **transmissão bruta de bits** no meio físico (cabos, rádio, fibra).
- Define características elétricas, mecânicas e funcionais dos meios de transmissão.
- **Não interpreta dados**, apenas os transmite como sinais elétricos, ópticos ou de rádio.

#### Principais funções

- Codificação de sinais (NRZ, Manchester, etc.)
- Taxa de transmissão (bps)
- Tipo de conector e pinagem
- Meio de transmissão (UTP, fibra óptica, etc.)

#### Equipamentos

- Hub
- Repetidores
- Meios físicos (cabos, conectores)

### Camada 2 - Enlace

> **Kurose & Ross (2014)**

- Estabelece uma **ligação confiável entre dois nós diretamente conectados**.
- Controla **erro**, **fluxo** e **delimitação de quadros**.
- Adiciona **endereçamento físico (MAC)**.

#### Principais funções

- Framing (estruturação dos quadros)
- Detecção e correção de erros (CRC, paridade)
- Controle de acesso ao meio (CSMA/CD, CSMA/CA, Token)
- Controle de fluxo

#### Protocolos

- Ethernet (IEEE 802.3)
- PPP (Point-to-Point Protocol)
- HDLC

#### Equipamentos

- Switches
- Access Points (operam também na 2)


### Camada 3 - Rede

> **Tanenbaum (2011)**

- Responsável pelo **endereçamento lógico (IP)** e **roteamento de pacotes entre redes diferentes**.
- Define como os pacotes são **encaminhados** através da rede.

#### Principais funções

- Roteamento (estático e dinâmico)
- Fragmentação e remontagem de pacotes
- Endereçamento lógico (IP)
- Controle de congestionamento

#### Protocolos

- IP (IPv4, IPv6)
- ICMP (ping, traceroute)
- OSPF, BGP, RIP

#### Equipamentos
- Roteadores

### Camada 4 - Transporte

> **Kurose & Ross (2014)**
 
- Responsável pelo **transporte fim a fim confiável (ou não)** entre dois hosts.
- Divide os dados em **segmentos** e garante a entrega correta.

#### Principais funções

- Controle de conexão (estabelecimento, manutenção e término)
- Controle de fluxo fim a fim
- Detecção e retransmissão de pacotes perdidos
- Multiplexação de conexões

### Protocolos

- TCP (confiável, orientado à conexão)
- UDP (não confiável, sem conexão)

### Camada 5 - Sessão

> **Torres (2009)**

- Gerencia **sessões de comunicação entre aplicações**.
- Fornece **controle de diálogo**, sincronização e recuperação.

#### Principais funções

- Estabelecimento e encerramento de sessões
- Diálogo full-duplex ou half-duplex
- Sincronização de pontos de verificação

#### Exemplos

- RPC (Remote Procedure Call)
- Gerência de sessão em aplicações multimídia (VoIP, videoconferência)


### Camada 6 - Apresentação

> **Kurose & Ross (2014)**

- Tradução dos dados entre **formato da aplicação e formato da rede**.
- Responsável por **codificação, compressão e criptografia**.

#### Principais funções
- Conversão de formatos (EBCDIC ↔ ASCII)
- Compressão de dados (JPEG, MP3)
- Criptografia (SSL/TLS)

#### Exemplos
- Codificações MIME
- Protocolos de sessão segura como TLS/SSL

### Camada 7 - Aplicação

Camada 7 – Aplicação

> **Tanenbaum (2011)**

- Camada que interage diretamente com o **usuário ou a aplicação**.
- Proporciona **serviços de rede para as aplicações**.

#### Principais funções
- Acesso à rede e aos serviços de aplicação
- Manipulação de arquivos, e-mail, navegação, etc.

#### Protocolos
- HTTP (web)
- FTP (transferência de arquivos)
- SMTP/IMAP (e-mail)
- DNS (resolução de nomes)

### Observações Importantes

- O modelo OSI é **conceitual**, enquanto o modelo TCP/IP é **prático e implementado**.
- As **camadas 1 a 4** tratam de **transporte de dados** (camadas inferiores).
- As **camadas 5 a 7** tratam da **interface com o usuário e aplicação**.
- Muitas aplicações atuais combinam funções das camadas 5, 6 e 7.

## Modelo TCP/IP (DARPA)   

> O modelo TCP/IP é um **modelo de arquitetura de protocolos** desenvolvido pelo **Departamento de Defesa dos EUA (DARPA)** e se tornou a **base da Internet**. É um modelo **prático** e amplamente **implementado**, composto por **4 ou 5 camadas**, dependendo da forma de apresentação.

### Estrutura Geral

| Camada (TCP/IP) | Função principal                            | Equivalente no OSI | Protocolos Principais                                    |
|-----------------|---------------------------------------------|--------------------|----------------------------------------------------------|
| Aplicação       | Serviços para aplicações do usuário         | Camadas 5, 6 e 7   | HTTP, FTP, DNS, SSH, SMTP, NFS, TELNET, SNMP, RDP        |
| Transporte      | Comunicação fim a fim entre processos       | Camada 4           | TCP, UDP                                                 |
| Internet        | Endereçamento lógico e roteamento           | Camada 3           | IP, ICMP, ARP, IGMP, IPsec                               |
| Acesso à Rede   | Acesso físico ao meio (MAC e meios físicos) | Camadas 1 e 2      | Ethernet, Wi-Fi, Token Ring, PPP, drivers de dispositivo |

> Observação: Alguns autores apresentam uma **5ª camada** chamada **Camada Física**, separando da subcamada de enlace. No entanto, em muitas abordagens simplificadas, ela está embutida na **camada de acesso à rede**.

### 1. Camada de Acesso à Rede (Link Layer)

#### Funções

- Acesso físico ao meio de transmissão
- Endereçamento físico (MAC)
- Controle de acesso ao meio (CSMA/CD, CSMA/CA)
- Encapsulamento em quadros

#### Tecnologias e Protocolos:

| Protocolo/Tecnologia      | Descrição                           |
|---------------------------|-------------------------------------|
| **Ethernet** (IEEE 802.3) | Rede cabeada LAN (comutação)        |
| **Wi-Fi** (IEEE 802.11)   | Redes sem fio                       |
| **PPP**                   | Redes ponto a ponto                 |
| **Token Ring**            | Topologia baseada em token (legado) |
| **Frame Relay, ATM**      | Tecnologias WAN (obsoletas)         |
| **Drivers de interface**  | Interface com hardware              |

### 2. Camada de Internet (Internet Layer)

#### Funções

- Endereçamento lógico
- Roteamento entre redes
- Fragmentação de pacotes
- Diagnóstico e controle

#### Protocolos

| Protocolo | Descrição                                                |
|-----------|----------------------------------------------------------|
| **IPv4**  | Endereçamento de 32 bits, cabeçalho variável             |
| **IPv6**  | Endereçamento de 128 bits, sem fragmentação por roteador |
| **ICMP**  | Diagnóstico de rede (ping, traceroute)                   |
| **ARP**   | Mapeia IP para MAC (IPv4)                                |
| **IGMP**  | Gerência de grupos multicast                             |
| **IPsec** | Segurança na camada IP (criptografia, tunelamento)       |
| **NAT**   | Tradução de endereços IP privados ↔ públicos             |

#### Roteamento

- **Estático**: configurado manualmente
- **Dinâmico**: via RIP, OSPF, BGP (usados em roteadores)

#### IPv4 (Internet Protocol version 4)

**Características gerais:**

- 32 bits, aproximadamente 4,3 bi de endereços
- Notado em decimal: `192.168.0.1`
- Cabeçalho mínimo de 20 bytes

**Estrutura do cabeçalho (simplificada)**

| Campo               | Tamanho | Função               |
|---------------------|---------|----------------------|
| Version             | 4 bits  | Versão (4)           |
| IHL                 | 4 bits  | Tamanho do cabeçalho |
| TTL                 | 8 bits  | Tempo de vida        |
| Protocol            | 8 bits  | Indica TCP, UDP etc. |
| Source Address      | 32 bits | IP de origem         |
| Destination Address | 32 bits | IP de destino        |

**Limitações**

- Escassez de endereços
- Cabeçalho complexo
- Sem segurança nativa

#### IPv6 (Internet Protocol version 6)

**Características gerais**

- 128 bits, formato hexadecimal: `2001:db8::1`
- Cabeçalho fixo de 40 bytes
- Suporte a autoconfiguração e IPsec embutido

**Estrutura do cabeçalho (simplificada)**

| Campo               | Tamanho  | Função                       |
|---------------------|----------|------------------------------|
| Version             | 4 bits   | Versão (6)                   |
| Payload Length      | 16 bits  | Tamanho dos dados            |
| Next Header         | 8 bits   | Protocolo superior (TCP/UDP) |
| Hop Limit           | 8 bits   | Substitui TTL                |
| Source Address      | 128 bits | IP de origem                 |
| Destination Address | 128 bits | IP de destino                |

**Vantagens**

- Mais endereços
- Cabeçalho mais simples
- IPsec e mobilidade nativas
- Sem broadcast (usa multicast)

### 3. Camada de Transporte (Transport Layer)

#### Funções

- Entrega fim a fim
- Multiplexação por portas
- Controle de fluxo e congestionamento

#### Protocolos

| Protocolo | Características                                       |
|-----------|-------------------------------------------------------|
| **TCP**   | Confiável, orientado à conexão, 3-way handshake, ACKs |
| **UDP**   | Sem conexão, sem garantia, menor overhead             |

#### Exemplos de portas

- TCP/80: HTTP
- UDP/53: DNS
- TCP/443: HTTPS

### 4. Camada de Aplicação (Application Layer)

#### Funções

- Interface com o usuário final
- Fornece serviços de rede às aplicações

#### Protocolos por categoria

**1. Transferência de Arquivos**

| Protocolo | Porta | Descrição                 |
|-----------|-------|---------------------------|
| FTP       | 21    | Transferência de arquivos |
| NFS       | 2049  | Compartilhamento em rede  |

**2. Acesso Remoto**

| Protocolo | Porta | Descrição             |
|-----------|-------|-----------------------|
| SSH       | 22    | Terminal seguro       |
| TELNET    | 23    | Terminal inseguro     |
| RDP       | 3389  | Acesso remoto gráfico |

**3. Web**

| Protocolo | Porta | Descrição            |
|-----------|-------|----------------------|
| HTTP      | 80    | Web sem criptografia |
| HTTPS     | 443   | Web com SSL/TLS      |

**4. E-mail**

| Protocolo | Porta | Função           |
|-----------|-------|------------------|
| SMTP      | 25    | Envio de e-mails |
| IMAP      | 143   | Leitura remota   |
| POP3      | 110   | Download local   |

**5. Infraestrutura**

| Protocolo | Porta | Função                    |
|-----------|-------|---------------------------|
| DNS       | 53    | Resolução de nomes        |
| DHCP      | 67/68 | Atribuição de IP          |
| SNMP      | 161   | Gerência de redes         |
| LDAP      | 389   | Diretórios e autenticação |

**6. Segurança**

| Protocolo | Função                     |
|-----------|----------------------------|
| IPsec     | Segurança IP (IPv6 nativo) |
| SSL/TLS   | Criptografia ponto a ponto |

#### Tabela Geral por Camada

| Camada TCP/IP | Protocolos Principais                                     |
|---------------|-----------------------------------------------------------|
| Aplicação     | HTTP, HTTPS, FTP, SSH, DNS, TELNET, SMTP, SNMP, DHCP, RDP |
| Transporte    | TCP, UDP                                                  |
| Internet      | IP (v4/v6), ICMP, ARP, IGMP, NAT, IPsec                   |
| Acesso à Rede | Ethernet, Wi-Fi, PPP                                      |

## Comparativo OSI x TCP/IP

| OSI              | TCP/IP                    |
|------------------|---------------------------|
| 7 – Aplicação    |                           |
| 6 – Apresentação |                           |
| 5 – Sessão       |                           |
| 4 – Transporte   | Transporte                |
| 3 – Rede         | Internet                  |
| 2 – Enlace       | Acesso à Rede             |
| 1 – Física       | Acesso à Rede             |
|                  | Aplicação (combina 5,6,7) |

---

## Infraestrutura e Sistemas Operacionais
## Gerenciamento e monitoramento de equipamentos de rede

### Objetivos do Gerenciamento

- **Monitorar desempenho** e utilização de recursos
- **Detectar falhas** e eventos anômalos
- **Gerenciar configuração** de dispositivos de rede
- **Controlar acesso e segurança**
- **Realizar manutenção preditiva e corretiva**

### Áreas Funcionais (FCAPS - ISO/ITU)
| Área              | Descrição                                                        |
|-------------------|------------------------------------------------------------------|
| **Fault**         | Gerenciamento de falhas (detecção, notificação e correção)       |
| **Configuration** | Gerenciamento de configuração (inicialização, alteração, backup) |
| **Accounting**    | Medição de uso (para cobrança ou estatística)                    |
| **Performance**   | Monitoramento da performance e análise de gargalos               |
| **Security**      | Controle de acesso, logs de autenticação, detecção de intrusões  |

### Protocolos e Ferramentas de Monitorament
- **Camada:** Aplicação (Modelo TCP/IP)
- **Portas:** UDP 161 (consulta), 162 (trap)
- **Componentes:**
  - *Manager:* sistema de gerenciamento (ex: Zabbix, PRTG, Nagios)
  - *Agent:* software no dispositivo gerenciado (switch, roteador)
  - *MIB (Management Information Base):* base de dados hierárquica
- **Versões:**
  - SNMPv1: básico, sem segurança
  - SNMPv2c: melhorias de desempenho
  - SNMPv3: segurança com autenticação e criptografia

### Syslog
- Protocolo de **log centralizado**
- Utilizado por switches, roteadores, firewalls e servidores
- Permite auditoria e resposta a incidentes
- Porta UDP 514

### NetFlow / sFlow
- Coleta de **estatísticas de tráfego** e fluxos de dados
- Muito usado por roteadores Cisco (NetFlow) e switches de camada 3
- Auxilia no diagnóstico e análise de tráfego em tempo real

### Exemplos de Equipamentos Monitoráveis

| Equipamento      | Parâmetros Monitorados                               |
|------------------|------------------------------------------------------|
| **Switch**       | Taxa de uso de porta, status das VLANs, erros de CRC |
| **Roteador**     | Roteamento ativo, latência, descarte de pacotes      |
| **Access Point** | Conexões ativas, sinal, interferência, SSIDs         |
| **Firewall**     | Tentativas de acesso negado, tráfego bloqueado       |
| **Servidor**     | Interface de rede, carga da CPU, memória             |

### Ferramentas Populares

| Ferramenta    | Tipo                  | Características principais                       |
|---------------|-----------------------|--------------------------------------------------|
| **Zabbix**    | NMS completo          | Gráficos, alertas, mapas, SNMP, agentes          |
| **Nagios**    | NMS modular           | Muito usado com plugins, foco em disponibilidade |
| **PRTG**      | Comercial             | Interface intuitiva, discovery automático        |
| **Wireshark** | Analizador de pacotes | Captura e inspeção detalhada do tráfego de rede  |

## Segurança no Gerenciamento

- Utilizar **SNMPv3** sempre que possível (criptografia e autenticação)
- **Restringir acesso** por IP ou VPN aos sistemas de gerenciamento
- **Auditar logs** gerados por SNMP, Syslog, etc.
- **Isolar redes de gerenciamento** do tráfego de produção

### Questão de Concurso Exemplo

O protocolo SNMP permite o monitoramento de dispositivos de rede. Em relação ao SNMPv3, assinale a alternativa correta:

a) Não oferece recursos de autenticação.  
b) Utiliza criptografia para proteger os dados.  
c) Substitui o protocolo IP no monitoramento de redes.  
d) Funciona exclusivamente com switches de camada 3.

> **Resposta:** b) Utiliza criptografia para proteger os dados.

## Ativos de rede

São os **equipamentos físicos e dispositivos eletrônicos** responsáveis pela comunicação, conectividade e gerenciamento da rede de computadores.

### Características principais

- Possuem **endereçamento lógico e/ou físico**
- Podem operar em diferentes **camadas do modelo OSI**
- Realizam **funções de comutação, roteamento, segurança, acesso ou repetição de sinais**
- Necessitam de **energia elétrica**, firmware e gerenciamento

### Tipos de Ativos de Rede
| Equipamento      | Camada OSI    | Função principal                                       |
|------------------|---------------|--------------------------------------------------------|
| **Hub**          | 1 - Física    | Repetidor de sinais; transmite a todos os dispositivos |
| **Switch**       | 2 - Enlace    | Comutador de quadros com base em MAC address           |
| **Bridge**       | 2 - Enlace    | Liga segmentos de rede, filtra quadros                 |
| **Roteador**     | 3 - Rede      | Encaminha pacotes entre redes diferentes (IP)          |
| **Access Point** | 2 - Enlace    | Permite acesso Wi-Fi, conecta-se via switch/roteador   |
| **Firewall**     | 3/4/7         | Controle e filtragem de tráfego, segurança de rede     |
| **Gateway**      | 4-7           | Converte protocolos de diferentes arquiteturas         |
| **Modem**        | 1 - Física    | Modula/demodula sinal digital ↔ analógico              |
| **Servidor**     | 7 - Aplicação | Executa serviços de rede (web, DNS, arquivos)          |

### Descrição detalhada dos principais ativos

- **Hub**
  - **Camada:** Física (1)
  - Transmite o sinal para **todas as portas** indiscriminadamente
  - Sem inteligência de comutação
  - Obsoleto nas redes modernas

- **Modem**
  - **Camada:** Física (1)
  - Realiza **modulação e demodulação**
  - Conecta a rede local à rede da operadora (ADSL, cabo, fibra)
  - Comumente incorporado ao roteador doméstico

- **Switch**
  - **Camada:** Enlace de Dados (2)
  - Aprende os **endereços MAC** das máquinas conectadas
  - Encaminha quadros **somente para a porta correta**
  - Pode operar em modo **gerenciado** (configurável) ou **não-gerenciado**

- **Access Point (AP)**
  - **Camada:** Enlace (2)
  - Conecta dispositivos **sem fio (Wi-Fi)** à rede cabeada
  - Opera sob padrão **IEEE 802.11**
  - Pode ser configurado em modo bridge ou roteador

- **Bridge**
  - **Camada:** Enlace (2)
  - Filtra e encaminha quadros com base nos MACs
  - Separa domínios de colisão
  - Antecessor funcional do switch
- 
- **Roteador**
  - **Camada:** Rede (3)
  - Utiliza endereços **IP** para encaminhar pacotes
  - Decide o **melhor caminho** para o destino
  - Pode aplicar **NAT, firewall, DHCP, VPN**
  - Equipamento fundamental para conexão com a Internet

- **Firewall**
  - **Camadas:** 3 (rede), 4 (transporte) e 7 (aplicação)
  - Controla entrada e saída de pacotes com base em regras
  - Tipos:
    - *Packet-filtering (estático)*
    - *Stateful inspection (dinâmico)*
    - *Application-layer firewall (proxy)*
  - Pode ser **software (iptables, pfSense)** ou **hardware (Cisco ASA, Fortigate)**

- **Gateway**
  - **Camadas:** 4 a 7 (camadas superiores)
  - Faz a conversão entre **protocolos e formatos distintos**
  - Ex: e-mail → SMS, IPv4 ↔ IPv6, rede IP ↔ rede Token Ring
  - Pode ser incorporado ao roteador ou servidor


- **Servidor**
  - **Camada:** Aplicação (7)
  - Oferece serviços como **DNS, DHCP, HTTP, FTP, banco de dados**
  - Possui IP fixo ou mapeado dinamicamente
  - Pode ser local ou remoto (em nuvem)

### Questão
Qual equipamento de rede opera na camada 2 do modelo OSI, encaminha quadros com base no endereço MAC de destino e é amplamente utilizado para segmentar redes locais?

a) Roteador  
b) Hub  
c) Switch  
d) Modem  
e) Gateway

> **Resposta correta:** c) Switch

## Passivos de rede

Passivos de rede são os **elementos físicos que compõem a infraestrutura de comunicação**, porém **não processam dados diretamente**. São responsáveis por **transmitir, organizar e proteger os sinais**.

Diferentemente dos ativos (como switches e roteadores), os passivos **não têm inteligência própria**. São essenciais para garantir **conectividade, desempenho e segurança física da rede**.

Principais Componentes Passivos

| Componente                                         | Função Principal                                                             |
|----------------------------------------------------|------------------------------------------------------------------------------|
| **Cabos de rede (UTP/STP, coaxial, fibra óptica)** | Transmissão física de sinais elétricos ou ópticos                            |
| **Patch cords**                                    | Cabos curtos para interligação de pontos (patch panel ↔ switch, por exemplo) |
| **Patch panels**                                   | Painéis organizadores de conexões de rede                                    |
| **Racks e gabinetes**                              | Estrutura metálica para organizar e proteger os equipamentos e cabeamento    |
| **Keystones / Tomadas RJ-45**                      | Interfaces de conexão entre o cabo e o equipamento                           |
| **Canaletas, calhas e eletrocalhas**               | Organização e proteção do cabeamento em ambientes internos                   |
| **Etiquetas e identificação**                      | Padronização e rastreabilidade dos pontos de rede                            |


### Tipos de Cabeamento

- **Par Trançado (UTP/STP)**
  - **UTP (Unshielded Twisted Pair):** Sem blindagem, mais econômico
  - **STP (Shielded Twisted Pair):** Com blindagem, usado em ambientes com interferência eletromagnética

| Categoria | Largura de Banda | Velocidade Máxima  | Observações                       |
|-----------|------------------|--------------------|-----------------------------------|
| CAT5e     | 100 MHz          | 1 Gbps             | Mais comum em redes LAN           |
| CAT6      | 250 MHz          | 10 Gbps (até 55m)  | Melhor blindagem                  |
| CAT6A     | 500 MHz          | 10 Gbps (até 100m) | Blindado, para ambientes ruidosos |
| CAT7      | 600 MHz          | 10 Gbps            | Uso industrial e data centers     |

- **Fibra Óptica**
  - Alta largura de banda
  - Imune a interferências
  - Maior custo de instalação

| Tipo      | Modo           | Distância  | Uso                                |
|-----------|----------------|------------|------------------------------------|
| Multimodo | Vários feixes  | até 2 km   | Redes locais, campus universitário |
| Monomodo  | Um único feixe | até 100 km | Redes de longa distância (WAN)     |


### Normas de Cabeamento Estruturado (segundo MARIN, 2009)

- **ANSI/TIA-568**: Padrão norte-americano de cabeamento estruturado
- **ISO/IEC 11801**: Padrão internacional
- **Cores de pares padrão**: azul, laranja, verde e marrom
- **Comprimento máximo recomendado**: 100 metros para par trançado (90 m + 10 m patch cords)
- **Padrões de crimpagem**: T568A e T568B

### Organização Física

- Racks
  - Tamanhos padronizados (ex: 19 polegadas)
  - Podem ser **abertos** ou **fechados (com portas e ventilação)**
  - Classificados em **rack de piso** e **rack de parede**

- Patch Panel
  - Centraliza as conexões de rede de um ambiente
  - Permite remanejamento rápido com patch cords
  - Numerado e identificado conforme padrão do projeto

### Questão
Assinale a alternativa que apresenta apenas componentes passivos de uma rede de computadores:

a) Roteador, switch e servidor  
b) Modem, firewall e access point  
c) Cabo de rede, patch panel e rack  
d) Hub, gateway e bridge  
e) Antena, roteador e impressora de rede

> **Resposta correta:** c) Cabo de rede, patch panel e rack

## Softwares e métricas de monitoramento

### Softwares de Monitoramento (NMS – Network Management Systems)

Softwares de monitoramento são sistemas utilizados para **supervisionar continuamente** a infraestrutura de rede e seus dispositivos. Eles atuam principalmente na **camada de aplicação do modelo TCP/IP** e utilizam protocolos como **SNMP, ICMP, NetFlow, Syslog**, entre outros.

### Principais Softwares

| Software             | Tipo        | Características Principais                                            |
|----------------------|-------------|-----------------------------------------------------------------------|
| **Zabbix**           | Open-source | Monitoramento de rede, servidores, aplicações, com alertas e gráficos |
| **Nagios**           | Open-source | Modular, com foco em disponibilidade, plugins diversos                |
| **PRTG**             | Comercial   | Interface gráfica intuitiva, auto-descoberta, múltiplos sensores      |
| **Cacti**            | Open-source | Focado em gráficos via SNMP e RRDTool                                 |
| **WhatsUp Gold**     | Comercial   | Monitoramento visual com alertas em tempo real                        |
| **SolarWinds**       | Comercial   | Alta escalabilidade, foco em grandes redes                            |
| **NetFlow Analyzer** | Comercial   | Específico para tráfego e análise de fluxos                           |

### Protocolos Comuns Utilizados

| Protocolo           | Porta | Função                                                |
|---------------------|-------|-------------------------------------------------------|
| **SNMP**            | 161   | Coleta de dados de dispositivos de rede               |
| **ICMP**            | —     | Verifica disponibilidade (ping, traceroute)           |
| **Syslog**          | 514   | Armazena mensagens e logs gerados por dispositivos    |
| **NetFlow / sFlow** | —     | Coleta estatísticas detalhadas de tráfego             |
| **WMI**             | —     | (Windows) Acesso a informações de sistema operacional |
| **Zabbix Agent**    | 10050 | Instalado em hosts para coleta ativa                  |

### SNMP (Simple Network Management Protocol)**

- **Estrutura**
  - **Manager:** Sistema que coleta dados
  - **Agent:** Software no equipamento monitorado
  - **MIB (Management Information Base):** Estrutura hierárquica com variáveis de estado
  - 
- **Tipos de mensagens SNMP**

| Tipo        | Descrição                                                   |
|-------------|-------------------------------------------------------------|
| **GET**     | Solicita valor de um parâmetro                              |
| **SET**     | Altera valor de um parâmetro                                |
| **TRAP**    | Enviado automaticamente pelo agente em caso de falha/alerta |
| **GETNEXT** | Solicita próximo parâmetro na MIB                           |

### Métricas de Monitoramento de Rede

As métricas são **indicadores-chave de desempenho (KPIs)** que ajudam a avaliar a saúde e o desempenho da rede.

| Métrica                      | Descrição                                                                    |
|------------------------------|------------------------------------------------------------------------------|
| **Disponibilidade (uptime)** | Percentual de tempo que o serviço está acessível                             |
| **Latência**                 | Tempo para um pacote ir e voltar (RTT - Round Trip Time)                     |
| **Perda de pacotes**         | Percentual de pacotes que não chegam ao destino                              |
| **Vazão (throughput)**       | Quantidade de dados transmitidos por segundo (ex: Mbps)                      |
| **Utilização de banda**      | Porcentagem da largura de banda utilizada                                    |
| **Jitter**                   | Variação no tempo de chegada dos pacotes (importante em VoIP)                |
| **Erros de interface**       | Pacotes corrompidos, descartados ou com colisão em portas de switch/roteador |
| **Temperatura e tensão**     | Condições físicas dos equipamentos (em data centers)                         |
| **Carga de CPU/RAM**         | Utilização de recursos nos hosts monitorados                                 |
| **Status de serviço**        | Se um serviço (como HTTP, DNS) está em execução                              |


### Exemplos práticos de uso de métricas

| Situação                        | Métrica relevante               | Ação esperada                    |
|---------------------------------|---------------------------------|----------------------------------|
| Reclamações de lentidão na rede | Latência, perda de pacotes      | Verificar roteadores, links WAN  |
| Voz sobre IP com cortes         | Jitter, perda, latência         | Ajustar QoS ou verificar link    |
| Alta carga em servidor web      | CPU, memória, conexões ativas   | Balanceamento ou upgrade         |
| Link de internet saturando      | Vazão, uso de banda             | Planejar upgrade ou controle QoS |
| Porta de switch com quedas      | Erros de interface, logs Syslog | Substituir cabo/dispositivo      |


### Benefícios do Monitoramento

- Prevenção de falhas
- Diagnóstico rápido de problemas
- Otimização da performance
- Segurança operacional
- Base para planejamento de capacidade (capacity planning)


### Questão de Concurso

1. Um administrador deseja medir a variação no tempo de chegada dos pacotes em uma chamada VoIP. A métrica mais adequada para essa finalidade é:
a) Latência  
b) Throughput  
c) Jitter  
d) Perda de pacotes  
e) Round Trip Time

> **Resposta correta:** c) Jitter

2. O protocolo padrão para o gerenciamento de dispositivos de rede, baseado em um conjunto hierárquico de variáveis chamado MIB, é:

a) ICMP  
b) SNMP  
c) Telnet  
d) SSH  
e) HTTP

> **Resposta correta:** **b) SNMP*

## Virtualização de Servidores

Virtualização é a **abstração de recursos computacionais**, permitindo que **múltiplas máquinas virtuais (VMs)** operem sobre um mesmo hardware físico. Cada VM **emula um sistema completo**, incluindo SO, CPU, memória e armazenamento.

### Tipos de Virtualização

| Tipo                                 | Descrição                                                             |
|--------------------------------------|-----------------------------------------------------------------------|
| **Virtualização de Servidor**        | Vários servidores virtuais sobre um mesmo hardware físico             |
| **Virtualização de SO (containers)** | Compartilham o mesmo kernel, são mais leves (ex: Docker)              |
| **Virtualização de Armazenamento**   | Abstração do armazenamento em múltiplas unidades lógicas              |
| **Virtualização de Rede**            | Criação de redes virtuais sobre infraestrutura física (ex: VLAN, SDN) |
| **Virtualização de Desktop (VDI)**   | Infraestrutura de desktop virtual, acessada remotamente               |

### Hypervisores (Monitor de Máquina Virtual)

### Tipo 1 – Nativo ou Bare-metal
Executa **diretamente no hardware** físico.

| Exemplo                             | Fabricante   |
|-------------------------------------|--------------|
| VMware ESXi                         | VMware       |
| Microsoft Hyper-V (modo bare-metal) | Microsoft    |
| KVM                                 | Kernel Linux |
| Xen                                 | Citrix/Linux |

### Tipo 2 – Hospedado
Executa **sobre um sistema operacional host**.

| Exemplo            | Fabricante |
|--------------------|------------|
| VMware Workstation | VMware     |
| Oracle VirtualBox  | Oracle     |
| Parallels Desktop  | Parallels  |

### Benefícios da Virtualização

| Vantagem                               | Explicação                                                      |
|----------------------------------------|-----------------------------------------------------------------|
| **Consolidação de servidores**         | Reduz o número de equipamentos físicos                          |
| **Alta disponibilidade**               | VMs podem ser migradas automaticamente em falhas (vMotion etc.) |
| **Melhor utilização de recursos**      | Compartilhamento de CPU, RAM, disco                             |
| **Facilidade de backup e recuperação** | Snapshots e clones facilitam restauração rápida                 |
| **Escalabilidade**                     | VMs podem ser criadas sob demanda                               |
| **Isolamento**                         | VMs funcionam de forma independente umas das outras             |

### Desvantagens / Desafios

| Desvantagem                | Descrição                                               |
|----------------------------|---------------------------------------------------------|
| **Overhead de desempenho** | Recursos físicos são compartilhados                     |
| **Gerência mais complexa** | Exige soluções robustas de orquestração e monitoramento |
| **Licenciamento**          | Custo de licenças (ex: VMware vSphere)                  |
| **Segurança**              | Ataques entre VMs ou contra o hipervisor (VM escape)    |

### Exemplo de Arquitetura

```
[Hardware Físico]
     ↓
[Hypervisor]
     ↓
+-------------+    +-------------+
| VM: WebSrv  |    | VM: DBSrv   |
| Ubuntu      |    | CentOS      |
+-------------+    +-------------+
```

### Questão de Concurso Exemplo
No contexto da virtualização de servidores, o software responsável por gerenciar as máquinas virtuais e intermediar o acesso aos recursos de hardware é denominado:

a) Container  
b) Guest OS  
c) Host OS  
d) Hypervisor  
e) Switch Virtual

> **Resposta correta:** d) Hypervisor

### Virtualização vs Containers

| Comparativo            | Máquinas Virtuais (VMs) | Containers          |
|------------------------|-------------------------|---------------------|
| Kernel próprio         | Sim                     | Compartilham o host |
| Overhead               | Maior                   | Menor               |
| Isolamento             | Forte                   | Moderado            |
| Leveza                 | Mais pesado             | Mais leve           |
| Tempo de inicialização | Lento                   | Rápido              |
| Exemplo                | VMware, VirtualBox      | Docker, Podman      |

### Softwares/Ferramentas Relacionadas

| Ferramenta        | Função                                |
|-------------------|---------------------------------------|
| VMware vSphere    | Gerenciamento de clusters de VMs      |
| Proxmox           | Hypervisor open-source                |
| KVM + Libvirt     | Virtualização nativa no Linux         |
| Vagrant           | Automatiza VMs para desenvolvimento   |
| Docker            | Containers (virtualização leve)       |
| OpenStack         | Nuvem privada baseada em VMs          |


## Virtual Lans (VLAN)

**VLAN (Virtual Local Area Network)** é uma técnica de **segmentação lógica de redes LAN**, permitindo que dispositivos físicos, mesmo em locais distintos, se comportem como se estivessem na **mesma rede local**.

### Objetivos da VLAN

- **Segmentação lógica da rede**
- **Segurança e isolamento de tráfego**
- **Redução de broadcast**
- **Melhor gerenciamento da rede**
- **Flexibilidade de realocação de estações**

### Como funciona?

- Cada porta do switch é **associada a uma VLAN**
- O tráfego de cada VLAN é **isolado** dos demais
- VLANs são identificadas por um **ID VLAN (VID)** – número entre 1 e 4094
- A comunicação entre VLANs exige um **roteador** ou um **switch L3**

### Tag VLAN – IEEE 802.1Q

- Adiciona um campo de **4 bytes** no cabeçalho Ethernet
- Permite identificar a qual VLAN um quadro pertence

### Estrutura do Tag 802.1Q:

| Campo         | Bits | Função                                |
|---------------|------|---------------------------------------|
| TPID          | 16   | Identificador do protocolo (0x8100)   |
| Priority      | 3    | QoS / prioridade                      |
| CFI           | 1    | Indica se é compatível com Token Ring |
| VLAN ID (VID) | 12   | Identificador da VLAN (1–4094)        |

### Tipos de Porta no Switch

| Tipo de Porta | Descrição                                                             |
|---------------|-----------------------------------------------------------------------|
| **Access**    | Porta comum, associada a uma única VLAN. Usada por hosts              |
| **Trunk**     | Transporta tráfego de **várias VLANs** entre switches ou com roteador |
| **Hybrid**    | Transporta VLAN nativa e tagged simultaneamente (menos comum)         |


### Exemplo Prático

```
[PC1]---[Switch]---[PC2]
   |         |        |
 VLAN 10   VLAN 20  VLAN 10

> PC1 e PC3 se comunicam (VLAN 10)
> PC1 e PC2 NÃO se comunicam (VLANs diferentes)
```

### Comunicação entre VLANs

- Exige um dispositivo de **camada 3**:
  - **Router tradicional**
  - **Switch camada 3 (L3 switch)** com **roteamento interno**

### Benefícios da VLAN

| Benefício              | Explicação                                                  |
|------------------------|-------------------------------------------------------------|
| **Segurança**          | Tráfego isolado por departamento (RH, TI, Financeiro etc.)  |
| **Eficiência**         | Redução de broadcast                                        |
| **Flexibilidade**      | Mudança de local física sem recabeamento                    |
| **Gerenciamento**      | Administra grupos de dispositivos com políticas específicas |

### Desvantagens

| Desvantagem                   | Descrição                                     |
|-------------------------------|-----------------------------------------------|
| **Complexidade**              | Requer planejamento de endereçamento          |
| **Gerência adicional**        | Requer switches gerenciáveis                  |
| **Necessidade de roteamento** | VLANs diferentes não se comunicam diretamente |

### VLAN Nativa

- VLAN **sem tag** (untagged) usada em links **trunk**
- Por padrão é a **VLAN 1**, mas pode ser alterada
- Usada quando o dispositivo de origem não suporta 802.1Q

### Exemplo de Questão de Concurso
Em uma rede corporativa, o tráfego de diferentes departamentos deve ser isolado para aumentar a segurança e reduzir o domínio de broadcast. A solução mais adequada é:

a) Substituir os switches por hubs  
b) Ativar o protocolo DHCP em todos os equipamentos  
c) Configurar VLANs nos switches gerenciáveis  
d) Dividir fisicamente a rede em vários switches  
e) Adicionar repetidores entre os departamentos

> **Resposta correta:** c) Configurar VLANs nos switches gerenciáveis

## Cabeamento estruturado

**Cabeamento Estruturado** é um sistema padronizado para conectar dispositivos de rede (dados, voz, vídeo e controle) com **organização, flexibilidade e escalabilidade**, independentemente do fabricante.

- Facilita manutenção e expansão
- Suporta múltiplas aplicações simultaneamente
- Reduz custo e complexidade a longo prazo

### Subsistemas do Cabeamento Estruturado

| Subsistema                    | Função Principal                                                      |
|-------------------------------|-----------------------------------------------------------------------|
| **Entrada de Serviços**       | Conecta a rede interna à operadora/ISP                                |
| **Sala de Equipamentos (ER)** | Centraliza switches, roteadores, servidores                           |
| **Backbone Vertical**         | Liga salas de telecomunicação em andares/prédios diferentes           |
| **Sala de Telecomunicações**  | Interface entre backbone vertical e cabos horizontais                 |
| **Backbone Horizontal**       | Conecta a sala de telecomunicações à área de trabalho (usuário final) |
| **Área de Trabalho**          | Conecta dispositivos finais às tomadas (PCs, IP phones etc.)          |

### Componentes Principais

- Cabos de par trançado (UTP, STP, FTP, S/FTP)
- Patch panels
- Racks e organizadores verticais/horizontais
- Tomadas modulares (faceplates)
- Patch cords (cabos de conexão)
- Dutos, eletrocalhas, canaletas
- Etiquetas e identificadores (TIA/EIA-606)
- Testadores e certificadores de rede

### Categorias de Cabo (TIA/EIA-568)

| Categoria | Velocidade Máxima | Frequência   | Aplicação                               |
|-----------|-------------------|--------------|-----------------------------------------|
| CAT5e     | 1 Gbps            | 100 MHz      | Redes gigabit residenciais/corporativas |
| CAT6      | 1–10 Gbps         | 250 MHz      | Ambientes corporativos exigentes        |
| CAT6a     | 10 Gbps           | 500 MHz      | Data centers, alta interferência        |
| CAT7      | 10 Gbps+          | 600–1000 MHz | Ambientes industriais e críticos        |


###  Técnicas de Instalação e Boas Práticas

- Instalação física

| Boa prática                                   | Justificativa                         |
|-----------------------------------------------|---------------------------------------|
| Distância mínima de 30 cm de cabos elétricos  | Reduz interferência eletromagnética   |
| Curvas suaves (raio > 4x o diâmetro do cabo)  | Evita atenuação e danos ao sinal      |
| Fixação adequada sem apertos excessivos       | Mantém integridade do par trançado    |
| Evitar cruzamento com fluorescentes e motores | Minimiza ruídos e EMI                 |
| Seguir padrão de crimpagem (TIA-568A ou B)    | Garante compatibilidade e organização |
| Organização em canaletas ou dutos             | Facilita manutenção e visualização    |

### Documentação e Identificação (TIA/EIA-606)

- Identificar ambos os extremos dos cabos (painel e tomada)
- Mapear posições no rack, patch panel e área de trabalho
- Usar etiquetas permanentes (não autoadesivas simples)
- Manter registros atualizados em software ou planilha

### Normas TIA/EIA Relacionadas

| Norma           | Descrição                                            |
|-----------------|------------------------------------------------------|
| **TIA/EIA-568** | Padrões de cabeamento para telecomunicações          |
| **TIA/EIA-569** | Espaços e caminhos físicos (dutos, salas, canaletas) |
| **TIA/EIA-606** | Administração, rotulagem e identificação             |
| **TIA/EIA-607** | Aterramento e ligação equipotencial                  |

### Certificação de Cabeamento

| Tipo de Teste         | O que mede                            | Equipamento necessário     |
|-----------------------|---------------------------------------|----------------------------|
| Teste de continuidade | Verifica se os pares estão conectados | Testador de cabos simples  |
| Certificação (Fluke)  | Verifica NEXT, PS-NEXT, atenuação     | Certificador profissional  |
| Teste de mapeamento   | Verifica a ordem dos pinos (T568A/B)  | Testadores de par trançado |

### Problemas comuns sem seguir boas práticas

| Erro                                | Consequência                            |
|-------------------------------------|-----------------------------------------|
| Cabos dobrados ou prensados         | Perda de desempenho (sinal degradado)   |
| Mistura de cabos de energia e dados | Interferência eletromagnética (EMI)     |
| Falta de identificação              | Dificuldade de manutenção e rastreio    |
| Instalação sem planejamento         | Rede desorganizada e sem escalabilidade |


### Topologia Física Recomendada

- **Topologia Estrela:**  
  Cada estação se conecta diretamente ao switch.  
  Permite isolamento de falhas e facilita a expansão.


### Vantagens do Cabeamento Estruturado

| Vantagem                     | Explicação                                              |
|------------------------------|---------------------------------------------------------|
| **Padronização**             | Compatível com equipamentos e serviços variados         |
| **Facilidade de manutenção** | Troca de equipamentos e reorganização simples           |
| **Flexibilidade**            | Suporta múltiplos protocolos e tecnologias (voz, dados) |
| **Documentação**             | Organização lógica com etiquetas e mapas de rede        |
| **Escalabilidade**           | Expansão modular conforme a necessidade do ambiente     |

### Questão Modelo de Concurso

No contexto do cabeamento estruturado, qual das alternativas está correta?

a) A categoria do cabo não afeta sua capacidade de transmissão  
b) O cabeamento horizontal conecta edifícios distintos  
c) O sistema deve seguir normas como TIA/EIA-568  
d) A topologia física padrão é em anel  
e) Pode-se dobrar o cabo até 90° sem prejuízo

> **Gabarito: c)**

### Conclusão

O Cabeamento Estruturado é **fundamental** para a confiabilidade, segurança e desempenho de redes modernas. Estar familiarizado com seus **subsistemas, normas e boas práticas** é essencial para qualquer profissional de TI — e frequentemente cobrado em concursos.

## Sistemas de Comunicação Óptica: Técnicas e Práticas de Instalação

A **comunicação óptica** utiliza **luz modulada** como meio de transmissão, guiada por um **meio dielétrico** (fibra óptica) para transportar dados com **alta velocidade**, **baixa perda** e **imunidade a ruídos eletromagnéticos**.

### Vantagens da Fibra Óptica

| Vantagem                   | Descrição                                     |
|----------------------------|-----------------------------------------------|
| Altíssima largura de banda | Velocidades de Gbps a Tbps                    |
| Imunidade eletromagnética  | Não sofre interferência como cabos metálicos  |
| Longo alcance              | Até centenas de km sem regeneração            |
| Segurança                  | Difícil de interceptar sem detecção           |
| Peso e tamanho reduzidos   | Menor que cabos de cobre com mesma capacidade |

### Tipos de Fibra Óptica

| Tipo               | Núcleo (core)  | Aplicação                           | Distância | Fonte de luz |
|--------------------|----------------|-------------------------------------|-----------|--------------|
| **Monomodo** (SM)  | ~8–10 µm       | Longas distâncias (WAN, operadoras) | > 10 km   | Laser (LD)   |
| **Multimodo** (MM) | ~50 ou 62,5 µm | Curtas distâncias (LAN, campus)     | Até 2 km  | LED ou VCSEL |

### Identificação de cores (ANSI/TIA-598-C):
- Monomodo: Amarelo
- Multimodo 62,5/125 µm: Laranja
- Multimodo 50/125 µm (laser otimizada): Aqua ou azul claro

### Componentes da Instalação Óptica

| Componente                  | Função                                |
|-----------------------------|---------------------------------------|
| Fibra óptica                | Meio de transmissão                   |
| Conectores                  | Junção entre cabos e equipamentos     |
| Emendas (fusão ou mecânica) | Conexão de fibras                     |
| Patch cords                 | Cabos para interligação no rack       |
| Bandejas de emenda          | Proteção e organização das emendas    |
| Distribuidor Óptico (DIO)   | Painel de terminação e organização    |
| Splitters                   | Dividem o sinal óptico (em redes PON) |

### Técnicas de Instalação

1. Preparação do Cabo
- Remoção da capa externa com ferramenta adequada
- Exposição da fibra sem danificar revestimentos
- Limpeza com álcool isopropílico e lenço não abrasivo

2. Conectorização
- Polimento do conector (PC, UPC, APC)
- Conectores mais comuns: **SC, LC, ST**
- Utilização de kits de terminação óptica (quick connectors)

3. Emenda por fusão
- Método preferido (baixa perda, alta confiabilidade)
- Utiliza **emendadora de fusão** e protetores térmicos

4. Dobramento mínimo
- Obedecer raio de curvatura mínimo (ex: 10x o diâmetro externo)
- Curvas muito fechadas causam **perda por microcurvatura**

### Boas Práticas

| Prática                            | Justificativa                                |
|------------------------------------|----------------------------------------------|
| Etiquetagem dos cabos e conectores | Facilita manutenção e rastreabilidade        |
| Testes após instalação             | Garantir atenuação dentro dos padrões        |
| Documentação completa              | Registro de rotas, conectores e resultados   |
| Evitar dobras e tensão mecânica    | Protege a integridade da fibra               |
| Aterramento de DIO (não da fibra)  | Segurança elétrica (apenas partes metálicas) |

### Testes em Fibra Óptica

| Teste        | Equipamento          | Finalidade                                     |
|--------------|----------------------|------------------------------------------------|
| Atenuação    | Power Meter + Fonte  | Mede a perda (em dB) entre dois pontos         |
| OTDR         | OTDR (reflectômetro) | Detecta eventos (emendas, quebras, curvaturas) |
| Continuidade | Laser visível (VFL)  | Verifica se a fibra está fisicamente intacta   |

### Comparativo: Cobre x Fibra

| Característica           | Par trançado (cobre) | Fibra óptica       |
|--------------------------|----------------------|--------------------|
| Velocidade               | Até 10 Gbps (CAT6a)  | 10 Gbps – Tbps     |
| Distância                | Até 100 m            | Até centenas de km |
| Interferência            | Alta (EMI)           | Imune              |
| Segurança                | Menor                | Alta               |
| Custo por metro          | Mais barato          | Mais caro          |
| Facilidade de instalação | Mais simples         | Mais especializada |

### Conclusão

A comunicação óptica é essencial para redes modernas de **alto desempenho e longo alcance**. Sua instalação exige **técnica apurada, ferramentas específicas** e **aderência a normas**, garantindo confiabilidade, segurança e escalabilidade da infraestrutura.


###  Questão modelo de concurso
Qual das alternativas descreve corretamente uma boa prática na instalação de sistemas de comunicação óptica?

a) A curvatura da fibra pode ser feita em ângulos de até 90°  
b) A conectorização óptica não necessita de polimento  
c) O raio mínimo de curvatura deve ser respeitado para evitar perdas  
d) Fibra óptica é ideal apenas para redes locais curtas  
e) A limpeza da fibra pode ser feita com água e sabão

> **Gabarito: c)**

## Arquitetura das redes de comunicação

A **arquitetura de redes de comunicação** define **como os dispositivos se comunicam entre si**, organizando funções em **camadas** e especificando os **protocolos** e **interfaces** que regem a troca de dados.

### Modelos de Arquitetura

1. **Modelo OSI (ISO/IEC 7498)**

- Padrão conceitual de 7 camadas
- Separação clara de responsabilidades
- Mais usado para ensino e documentação

| Camada          | Função Principal                           |
|-----------------|--------------------------------------------|
| 7. Aplicação    | Interface com usuário e aplicações         |
| 6. Apresentação | Formatação, compressão, criptografia       |
| 5. Sessão       | Controle de sessão e diálogo               |
| 4. Transporte   | Entrega fim a fim, confiabilidade          |
| 3. Rede         | Roteamento e endereçamento lógico (IP)     |
| 2. Enlace       | Acesso ao meio, endereçamento físico (MAC) |
| 1. Física       | Transmissão de bits no meio físico         |

2. **Modelo TCP/IP (Prático e implementado)**

- Baseado em protocolos reais
- Utilizado na Internet e redes modernas
- Mais enxuto: 4 camadas principais

| Camada TCP/IP        | Equivalente OSI                   | Protocolos Típicos        |
|----------------------|-----------------------------------|---------------------------|
| Aplicação            | Aplicação + Apresentação + Sessão | HTTP, FTP, DNS, SMTP, SSH |
| Transporte           | Transporte                        | TCP, UDP                  |
| Internet             | Rede                              | IPv4, IPv6, ICMP, ARP     |
| Acesso à Rede (Link) | Enlace + Física                   | Ethernet, Wi-Fi, PPP      |

### Arquiteturas de Comunicação

1. **Cliente/Servidor**

| Característica          | Descrição                                         |
|-------------------------|---------------------------------------------------|
| Centralização           | Servidor fornece serviços para múltiplos clientes |
| Escalabilidade limitada | Sobrecarrega o servidor com muitos acessos        |
| Segurança e controle    | Mais fácil de auditar e gerenciar                 |
| Exemplo                 | Web (HTTP), E-mail (SMTP/IMAP/POP3)               |

2. **Ponto-a-Ponto (P2P)**

| Característica      | Descrição                                     |
|---------------------|-----------------------------------------------|
| Descentralização    | Todos os nós podem ser clientes e servidores  |
| Alta escalabilidade | Compartilhamento de recursos entre pares      |
| Menor controle      | Difícil de gerenciar segurança e consistência |
| Exemplo             | BitTorrent, eMule, Skype (antigo)             |

### Classificação de Redes por Escopo

| Tipo          | Sigla | Abrangência                | Exemplo                  |
|---------------|-------|----------------------------|--------------------------|
| Local         | LAN   | Prédio ou campus           | Escritórios, escolas     |
| Metropolitana | MAN   | Cidade ou região urbana    | TV a cabo, universidades |
| Ampla         | WAN   | Países/continentes         | Internet                 |
| Sem fio       | WLAN  | LAN com Wi-Fi              | Redes domésticas, cafés  |
| PAN           | PAN   | Curtíssimo alcance pessoal | Bluetooth, wearables     |

### Topologias de Rede

| Topologia  | Característica                                          |
|------------|---------------------------------------------------------|
| Barramento | Todos os dispositivos compartilham um único cabo        |
| Estrela    | Cada dispositivo se conecta a um ponto central (switch) |
| Anel       | Nós conectados circularmente                            |
| Malha      | Todos os dispositivos conectados entre si               |
| Árvore     | Hierarquia em níveis (switches interligados)            |
| Híbrida    | Combinação de duas ou mais topologias                   |

### Tipos de Comunicação

| Tipo            | Descrição                                            |
|-----------------|------------------------------------------------------|
| **Simplex**     | Comunicação unidirecional (ex: rádio FM)             |
| **Half-Duplex** | Bidirecional, mas um de cada vez (ex: walkie-talkie) |
| **Full-Duplex** | Bidirecional simultâneo (ex: telefone)               |

### Protocolos de Comunicação por Camada (TCP/IP)

| Camada        | Protocolos                       |
|---------------|----------------------------------|
| Aplicação     | HTTP, HTTPS, DNS, FTP, SMTP, SSH |
| Transporte    | TCP, UDP                         |
| Internet      | IPv4, IPv6, ICMP, ARP, NAT       |
| Acesso à Rede | Ethernet, Wi-Fi, PPP             |

### Conclusão

A **arquitetura de redes** define os fundamentos sobre os quais toda comunicação digital se apoia. Conhecer seus **modelos, camadas, protocolos e formas de organização** é essencial para compreender a infraestrutura de redes e sistemas distribuídos modernos — e um tema **quase sempre presente em provas de concurso**.

### Questão modelo de concurso
Sobre os modelos de arquitetura de redes de computadores, assinale a opção correta:

a) O modelo TCP/IP é composto por sete camadas conceituais.  
b) No modelo OSI, a camada de transporte oferece roteamento entre redes.  
c) A topologia estrela exige que todos os nós estejam conectados entre si diretamente.  
d) A camada de rede do modelo OSI é responsável por endereçamento lógico.  
e) A arquitetura cliente/servidor distribui igualmente os serviços entre os clientes.

> **Gabarito: d)**


## Armazenamento: SAN, NAS, RAID

O armazenamento em redes corporativas pode ser feito de diversas formas, mas os principais conceitos giram em torno de:

- **RAID** – Organização de discos para redundância e desempenho
- **NAS** – Armazenamento em nível de **arquivo** via rede
- **SAN** – Armazenamento em nível de **bloco**, com alta performance

## RAID (Redundant Array of Independent Disks)

RAID é uma tecnologia de armazenamento que **combina múltiplos discos rígidos** para obter **redundância**, **tolerância a falhas**, **aumento de desempenho**, ou uma combinação desses objetivos.

> RAID pode ser implementado:
> - via **hardware** (controladoras RAID dedicadas)
> - via **software** (em sistemas operacionais como Linux ou Windows)

### Níveis de RAID mais comuns

| Nível   | Nome                    | Características                                        | Redundância | Desempenho |
|---------|-------------------------|--------------------------------------------------------|-------------|------------|
| RAID 0  | Striping                | Divide os dados entre dois ou mais discos sem paridade | Não         | Alta       |
| RAID 1  | Espelhamento (Mirror)   | Cópia exata dos dados em dois discos                   | Sim         | Leitura    |
| RAID 5  | Paridade distribuída    | Usa paridade distribuída, exige pelo menos 3 discos    | Sim         | Equilíbrio |
| RAID 6  | Paridade dupla          | Como o RAID 5, mas com paridade dupla (mín. 4 discos)  | Sim         | Moderado   |
| RAID 10 | Espelhamento + Striping | Combina RAID 1 + RAID 0 (mínimo 4 discos)              | Sim         | Alta       |

### Conceitos importantes

- **Paridade**: Informação gerada para permitir reconstrução de dados em caso de falha
- **Striping**: Distribuição de blocos de dados em vários discos
- **Espelhamento**: Cópia fiel de dados em discos diferentes

### Exemplos de uso

| Aplicação                           | Nível RAID sugerido |
|-------------------------------------|---------------------|
| Desempenho sem importância de falha | RAID 0              |
| Backup local ou pessoal             | RAID 1              |
| Servidores corporativos             | RAID 5 ou 6         |
| Bancos de dados críticos            | RAID 10             |

- RAID não é Backup: RAID protege contra **falhas de hardware**, mas não substitui cópias de segurança externas. Riscos como:
  - Exclusão acidental
  - Vírus/Ransomware
  - Desastres físicos (fogo, água)
  
### RAID: Hardware x Software

| Tipo         | Vantagens                        | Desvantagens                       |
|--------------|----------------------------------|------------------------------------|
| **Hardware** | Melhor desempenho, transparência | Mais caro, depende da controladora |
| **Software** | Flexível, sem custo adicional    | Maior uso da CPU, menor desempenho |

### Conclusão

O conhecimento sobre **RAID** é essencial em redes corporativas, servidores e sistemas de armazenamento. Saber quando e como aplicar cada nível de RAID é uma habilidade exigida para concursos e prática profissional.

### Questão de Concurso (Exemplo)
O RAID 1 fornece:

a) Aumento de velocidade sem tolerância a falhas  
b) Redundância por paridade distribuída  
c) Espelhamento, garantindo redundância total dos dados  
d) Striping com paridade dupla  
e) Armazenamento em bloco com compressão

> **Gabarito: c)**

## SAN (Storage Area Network)

SAN (**Storage Area Network**) é uma **rede dedicada e de alta velocidade** que interconecta dispositivos de armazenamento (como discos e fitas) a servidores, permitindo acesso em **nível de bloco**, como se fossem discos locais.

### Arquitetura da SAN

- Cria uma **rede separada** da LAN principal
- Utiliza **protocolos específicos**, como Fibre Channel ou iSCSI
- É altamente escalável, confiável e usada em **datacenters e ambientes críticos**

### Componentes principais:

| Componente                        | Função                                                |
|-----------------------------------|-------------------------------------------------------|
| **Dispositivos de armazenamento** | Discos, arrays, bibliotecas de fita                   |
| **Switches SAN**                  | Conectam servidores e dispositivos de armazenamento   |
| **Host Bus Adapter (HBA)**        | Placa do servidor que conecta à SAN via Fibre Channel |
| **Cabling**                       | Cabos de fibra óptica ou Ethernet (iSCSI)             |

### Protocolos utilizados

| Protocolo         | Descrição                                   |
|-------------------|---------------------------------------------|
| **Fibre Channel** | Alta velocidade, baixa latência (2–32 Gbps) |
| **iSCSI**         | Usa TCP/IP sobre redes Ethernet             |
| **FCoE**          | Fibre Channel over Ethernet                 |


### Vantagens da SAN

- Alta **velocidade e performance**
- **Baixa latência**
- Ideal para **bancos de dados e servidores virtualizados**
- Escalabilidade e disponibilidade
- Pode ser replicada ou espelhada para **disaster recovery**

### Desvantagens

- Custo elevado
- Alta complexidade de configuração e manutenção
- Exige equipe especializada

### Casos de uso comuns

- Datacenters corporativos
- Hospedagem de máquinas virtuais (VMware, Hyper-V)
- Bancos de dados críticos (Oracle, PostgreSQL, SQL Server)
- Ambientes com alta disponibilidade (HA)


### Conclusão

SAN é a escolha ideal para **ambientes críticos**, onde o desempenho e a confiabilidade do armazenamento são cruciais. Seu uso exige infraestrutura especializada, mas oferece escalabilidade e performance superiores — conhecimentos cobrados em concursos de infraestrutura, redes e servidores.

## Armazenamento: NAS (Network Attached Storage)

NAS é a sigla para **Network Attached Storage**, ou seja, **armazenamento conectado à rede**.  
É um **dispositivo dedicado** que oferece **compartilhamento de arquivos** por meio da rede local, funcionando como um **servidor de arquivos autônomo**.

### Características do NAS

| Aspecto                | Detalhes                                        |
|------------------------|-------------------------------------------------|
| Tipo de acesso         | **Arquivo** (file-level)                        |
| Protocolo de rede      | SMB/CIFS (Windows), NFS (Linux/Unix), FTP, HTTP |
| Sistema operacional    | Sim (Linux embarcado, FreeNAS, TrueNAS etc.)    |
| IP próprio             | Sim                                             |
| Facilidade de uso      | Interface gráfica via navegador (Web UI)        |
| Nível de gerenciamento | Médio (fácil instalação e configuração)         |
| Redundância suportada  | Suporte a RAID 0/1/5/6/10 (varia por modelo)    |
| Backup e replicação    | Recursos nativos em modelos avançados           |

### Como o NAS funciona?

- Fica conectado na LAN via cabo Ethernet ou Wi-Fi
- Permite que múltiplos usuários acessem arquivos simultaneamente
- Pode ser acessado via IP e protocolo de compartilhamento
- Age como um "servidor de arquivos" com capacidade de gerenciamento

### Vantagens

- **Fácil de instalar e configurar**
- **Acesso multiusuário por IP**
-  **Custo mais baixo** do que soluções SAN
-  **Suporte a RAID** e backup em alguns modelos
-  **Compatível com sistemas Windows, Linux, macOS**

### Desvantagens

- **Desempenho inferior** a SAN (limitação da rede TCP/IP)
- Vulnerável a sobrecarga se muitos usuários acessarem simultaneamente
- Segurança depende de boa configuração de permissões

### Exemplos de uso

- Compartilhamento de arquivos em pequenas empresas
- Servidor de mídia doméstico
- Backup automatizado de máquinas da rede
- Armazenamento central para departamentos

### Protocolos mais comuns no NAS

| Protocolo    | Descrição                                  | Porta padrão |
|--------------|--------------------------------------------|--------------|
| **SMB/CIFS** | Compartilhamento de arquivos no Windows    | 445          |
| **NFS**      | Compartilhamento de arquivos em Linux/Unix | 2049         |
| **FTP**      | Transferência de arquivos                  | 21           |
| **HTTP**     | Interface Web e compartilhamento leve      | 80           |

### Conclusão

O NAS é uma solução acessível e amplamente usada para **compartilhamento de arquivos via rede**, com **instalação simples** e **compatibilidade multiplataforma**, sendo ideal para pequenas e médias empresas, e frequentemente citado em provas de concurso para analista de redes e suporte técnico.

### NAS x SAN x DAS

| Recurso        | NAS               | SAN                   | DAS                     |
|----------------|-------------------|-----------------------|-------------------------|
| Tipo de acesso | Arquivo           | Bloco                 | Bloco                   |
| Conexão        | Ethernet (TCP/IP) | Fibre Channel / iSCSI | Direto ao host          |
| Facilidade     | Fácil de instalar | Requer especialistas  | Simples                 |
| Custo          | Médio             | Alto                  | Baixo                   |
| Desempenho     | Médio             | Alto                  | Alto (limitado ao host) |


### Questão modelo de concurso
Acerca das redes de armazenamento, assinale a opção correta:

a) A rede SAN fornece acesso em nível de arquivo, sendo ideal para compartilhamento entre usuários.  
b) A SAN é uma rede dedicada de armazenamento com acesso a blocos e uso de protocolos como iSCSI.  
c) A SAN utiliza apenas redes Ethernet e protocolo FTP para acesso rápido a dados.  
d) A SAN substitui a necessidade de discos locais em servidores NAS.  
e) A SAN é composta por switches comuns de rede e compartilhamentos CIFS.

> **Gabarito: b)**

### Questão modelo de concurso
Assinale a alternativa que descreve corretamente uma solução NAS:

a) Fornece acesso em nível de bloco para servidores de banco de dados.  
b) Requer protocolos Fibre Channel e switches dedicados.  
c) Atua como um servidor de arquivos, acessado via rede local.  
d) É uma tecnologia de acesso direto aos discos de armazenamento.  
e) Implementa armazenamento de backup exclusivamente em nuvem.

>  **Gabarito: c)**

## Noções de Backup: Armazenamento, Tipos, Contingência e Ferramentas

Backup é a cópia segura dos dados de um sistema para garantir sua recuperação em caso de falhas, desastres, ataques ou perda acidental. É parte essencial da segurança e continuidade de negócios.

### Meios de Armazenamento

| Meio                 | Características                          | Vantagens                        | Desvantagens                      |
|----------------------|------------------------------------------|----------------------------------|-----------------------------------|
| HD externo           | USB, portátil                            | Custo acessível, fácil uso       | Risco de perda física             |
| SSD externo          | Alta velocidade                          | Rápido, resistente               | Custo mais elevado                |
| Fita magnética (LTO) | Corporativo                              | Alta capacidade, durabilidade    | Leitura sequencial, mais lento    |
| NAS                  | Armazenamento em rede (file-level)       | Multiusuário, RAID               | Performance dependente da rede    |
| SAN                  | Armazenamento em bloco, uso profissional | Alta performance, escalabilidade | Alto custo, configuração complexa |
| Mídias ópticas       | DVD, Blu-ray                             | Barato                           | Obsoleto, pouca capacidade        |
| Nuvem (Cloud)        | Amazon S3, Azure, Google Drive etc.      | Escalável, redundante            | Dependente de internet, custo     |

> **Regra 3-2-1 de backup:** 3 cópias, 2 mídias diferentes, 1 externa.

### Sistemas de Backup

| Sistema       | Descrição                                             |
|---------------|-------------------------------------------------------|
| Manual        | Executado por operador, sem agendamento               |
| Agendado      | Realizado em intervalos definidos                     |
| Automatizado  | Agendamento + relatórios e alertas                    |
| Em tempo real | Backup contínuo: cópia imediata de arquivos alterados |
| Centralizado  | Todos os dados da rede salvos em um servidor central  |
| Distribuído   | Cada dispositivo faz seu próprio backup               |

### Tipos de Backup

| Tipo            | O que copia?                                     | Vantagens                  | Desvantagens                       |
|-----------------|--------------------------------------------------|----------------------------|------------------------------------|
| Completo        | Todos os arquivos selecionados                   | Fácil restauração          | Demorado, ocupa mais espaço        |
| Incremental     | Somente arquivos alterados desde último backup   | Rápido, ocupa pouco espaço | Restauração lenta (cadeia)         |
| Diferencial     | Arquivos alterados desde o último completo       | Restauração mais rápida    | Ocupa mais espaço que incremental  |
| Espelhamento    | Cópia idêntica dos dados (mirror)                | Sincronização rápida       | Risco de sobrescrever exclusões    |
| Snapshot        | Foto instantânea de um sistema/volume            | Restauração instantânea    | Requer recursos de sistema         |
| Imagem de disco | Clona o sistema completo (SO, aplicações, dados) | Restauração completa       | Arquivo grande, ocupa muito espaço |

### Periodicidade e Estratégias

| Tipo        | Frequência          | Uso comum                       |
|-------------|---------------------|---------------------------------|
| Diário      | Toda noite          | Dados de sistemas de produção   |
| Semanal     | Toda semana         | Sistemas com baixa alteração    |
| Mensal      | Fim de cada mês     | Armazenamento legal/regulatório |
| Sob demanda | Conforme necessário | Antes de atualizações críticas  |

> Exemplo prático: Backup completo aos domingos, incrementais nos dias úteis.

### Planos de Contingência e Recuperação

| Termo                          | Definição                                       |
|--------------------------------|-------------------------------------------------|
| RTO (Recovery Time Objective)  | Tempo máximo aceitável para restaurar o sistema |
| RPO (Recovery Point Objective) | Tempo máximo de perda aceitável (entre backups) |

### Elementos do plano:

- Análise de risco e impacto
- Ambientes alternativos: **Cold**, **Warm**, **Hot Site**
- Documentação e procedimentos testáveis
- Testes e auditorias regulares

### Ferramentas e Softwares

| Nome          | Plataforma      | Nível       | Características principais                       |
|---------------|-----------------|-------------|--------------------------------------------------|
| Cobian Backup | Windows         | Pessoal     | Grátis, agendamento, compactação                 |
| Bacula        | Linux/Windows   | Corporativo | CLI e interface web, agendamentos, segurança     |
| Veeam         | Multiplataforma | Enterprise  | Física/virtual/cloud, replicação, snapshots      |
| Acronis       | Windows/Linux   | Comercial   | Imagem de disco, proteção contra ransomware      |
| Duplicati     | Multiplataforma | Pessoal/SMB | Backup em nuvem, criptografia, agendamento       |
| Timeshift     | Linux           | Desktop     | Snapshots de sistema, ideal para ambientes Linux |

### Segurança em Backup

- **Criptografia** dos dados em trânsito e em repouso
- **Controle de acesso** com autenticação e permissões
- **Isolamento** dos backups (desconectados ou separados da rede)
- **Auditoria e logs** de acesso e restauração

### Diferença entre Backup e Arquivamento

| Fator        | Backup                   | Arquivamento                 |
|--------------|--------------------------|------------------------------|
| Objetivo     | Recuperação de desastres | Armazenamento de longo prazo |
| Frequência   | Regular                  | Esporádico                   |
| Tipo de dado | Ativo (em uso)           | Inativo (histórico)          |
| Local comum  | HDD, SSD, nuvem, fita    | Fita, NAS, repositórios      |
| Restauração  | Imediata, frequente      | Rara, mas precisa            |

### Termos Técnicos para Concursos

- **Dump**: cópia completa de banco de dados ou sistema
- **Cold Backup**: sistema parado durante cópia
- **Hot Backup**: sistema ativo durante cópia
- **Deduplicação**: remoção de arquivos duplicados
- **Compressão**: redução de tamanho dos arquivos
- **Versionamento**: manutenção de várias versões do mesmo arquivo

### Questão de Concurso

Um backup que realiza apenas a cópia dos arquivos modificados desde o último backup completo é denominado:

a) Completo  
b) Espelho  
c) Diferencial  
d) Incremental  
e) Imagem

> **Gabarito: d) Incremental**

## Administração de sistemas operacionais: LINUX

### Distribuições Linux

| Distribuição | Finalidade                     | Gerenciador de Pacotes |
|--------------|--------------------------------|------------------------|
| Ubuntu       | Uso geral, servidores, desktop | `apt` (Debian-based)   |
| Debian       | Estável, servidores            | `apt`                  |
| CentOS       | Corporativo, baseado em RHEL   | `yum`, `dnf`           |
| Fedora       | Inovação, testes para Red Hat  | `dnf`                  |
| Arch Linux   | Avançado, personalizado        | `pacman`               |
| Red Hat      | Corporativo, com suporte pago  | `yum`, `dnf`           |

### Gerenciamento de Pacotes

- **APT (Debian/Ubuntu)**
```bash
sudo apt update && sudo apt upgrade
sudo apt install <pacote>
sudo apt remove <pacote>
```

- **YUM/DNF (RHEL/CentOS/Fedora)**
```bash
sudo yum install <pacote>
sudo yum update
sudo yum remove <pacote>
```

### Zypper (OpenSUSE)
```bash
sudo zypper install <pacote>
```

### Gerenciamento de Usuários e Permissões

| Comando     | Função                              |
|-------------|-------------------------------------|
| `adduser`   | Adiciona novo usuário               |
| `passwd`    | Define ou altera senha              |
| `usermod`   | Modifica atributos de usuários      |
| `groupadd`  | Cria novo grupo                     |
| `chown`     | Altera dono de arquivo              |
| `chmod`     | Altera permissões de acesso         |
| `id`        | Mostra UID, GID e grupos de usuário |

**Exemplo**

```bash
sudo adduser rafael
sudo usermod -aG sudo rafael
chmod 755 arquivo.sh
chown rafael:rafael arquivo.sh
```

### Sistema de Arquivos

| Comando  | Descrição                    |
|----------|------------------------------|
| `df -h`  | Mostra uso de disco          |
| `du -sh` | Mostra tamanho de diretórios |
| `mount`  | Monta sistemas de arquivos   |
| `umount` | Desmonta volumes             |
| `lsblk`  | Lista blocos de disco        |
| `fdisk`  | Particionamento de discos    |

### Serviços e Daemons

| Comando            | Descrição                         |
|--------------------|-----------------------------------|
| `systemctl start`  | Inicia um serviço                 |
| `systemctl stop`   | Encerra um serviço                |
| `systemctl status` | Exibe status do serviço           |
| `systemctl enable` | Habilita serviço na inicialização |
| `cron`, `crontab`  | Agendamento de tarefas periódicas |

**Exemplo (agendar backup)**

```bash
crontab -e
0 2 * * * /home/rafael/scripts/backup.sh
```

### Comandos de Rede

| Comando                | Função                                                                |
|------------------------|-----------------------------------------------------------------------|
| `ip a`                 | Mostra interfaces de rede                                             |
| `ip link`              | Mostra e configura links (interfaces)                                 |
| `ip route`             | Exibe tabela de roteamento                                            |
| `ping`                 | Testa conectividade com outro host                                    |
| `traceroute destino`   | Exibe caminho percorrido até o destino                                |
| `netstat -tuln`        | Lista portas abertas (TCP/UDP)                                        |
| `ss -tuln`             | Mostra conexões de rede (substituto moderno do netstat)               |
| `dig dominio.com`      | Consulta DNS (resolução de nomes)                                     |
| `nslookup dominio.com` | Consulta DNS (alternativo ao dig)                                     |
| `host dominio.com`     | Consulta DNS simples                                                  |
| `whois dominio.com`    | Informações de registro de domínios                                   |
| `curl http://site.com` | Requisições HTTP diretamente no terminal                              |
| `wget http://site.com` | Faz download de arquivos via HTTP, FTP, etc.                          |
| `nmap IP`              | Escaneia portas e serviços de rede (necessita instalação)             |
| `ethtool eth0`         | Mostra e configura parâmetros da interface (ex: velocidade)           |
| `nmcli`                | Gerenciador de conexões de rede via linha de comando (NetworkManager) |
| `iwconfig`             | Configura rede wireless (substituído por `iw`)                        |
| `iw dev`               | Exibe interfaces Wi-Fi e status                                       |
| `tcpdump`              | Sniffer de pacotes (análise de tráfego)                               |
| `ip neigh`             | Mostra tabela ARP (equivalente ao `arp -a`)                           |
| `arping IP`            | Envia requisições ARP (verifica se IP responde na rede local)         |
| `route -n`             | Mostra tabela de roteamento legada                                    |
| `firewalld-cmd`        | Gerencia regras do firewall com firewalld                             |
| `ufw`                  | Firewall simplificado (Ubuntu)                                        |
| `ifconfig`             | Configura IPs e interfaces (obsoleto, mas ainda usado)                |

> **Dica**: comandos como `tcpdump`, `nmap`, `ethtool` e `dig` podem precisar ser instalados via `apt`, `yum` ou `dnf`.

### Logs do Sistema

| Caminho              | Descrição                   |
|----------------------|-----------------------------|
| `/var/log/syslog`    | Log geral do sistema        |
| `/var/log/auth.log`  | Log de autenticação         |
| `/var/log/dmesg`     | Mensagens do kernel         |
| `journalctl`         | Visualização com systemd    |

### Gerenciamento de Processos

| Comando            | Função                              |
|--------------------|-------------------------------------|
| `ps aux`           | Lista todos os processos            |
| `top`              | Monitoramento em tempo real         |
| `htop`             | Interface interativa                |
| `kill PID`         | Mata processo com ID                |
| `nice`             | Define prioridade de processo       |
| `jobs`, `bg`, `fg` | Gerencia processos em segundo plano |

### Shell Scripting

**Exemplo simples**

```bash
#!/bin/bash
echo "Início do backup em: $(date)"
tar -czf /home/rafael/backup.tar.gz /home/rafael
echo "Fim do backup em: $(date)"
```

```bash
chmod +x backup.sh
./backup.sh
```

### SSH – Acesso Remoto Seguro

| Comando                | Descrição                            |
|------------------------|--------------------------------------|
| `ssh user@ip`          | Acesso remoto ao servidor            |
| `scp arquivo user@ip:` | Envia arquivo via SSH                |
| `ssh-keygen`           | Gera chave pública/privada           |
| `ssh-copy-id`          | Envia chave pública para host remoto |


### Backup no Linux

| Ferramenta  | Descrição                              |
|-------------|----------------------------------------|
| `rsync`     | Sincronização de arquivos e diretórios |
| `tar`       | Compressão e backup local              |
| `dd`        | Clonagem bit a bit de discos           |
| `timeshift` | Snapshots do sistema (Linux Desktop)   |
| `bacula`    | Backup empresarial em rede             |

### Questão de Concurso

Em sistemas Linux, o comando utilizado para alterar as permissões de um arquivo é:

a) chown  
b) chmod  
c) ps  
d) kill  
e) mount

> **Gabarito: b)** `chmod


## Administração de sistemas operacionais: MS-WINDOWS

### Edições do Windows

| Edição             | Finalidade                                                       |
|--------------------|------------------------------------------------------------------|
| Windows Home       | Uso doméstico                                                    |
| Windows Pro        | Profissional, recursos de domínio                                |
| Windows Enterprise | Corporativo, com recursos avançados de segurança e gerenciamento |
| Windows Server     | Servidores, AD, DHCP, DNS, Hyper-V                               |

### Ferramentas Administrativas

| Ferramenta                                   | Finalidade                              |
|----------------------------------------------|-----------------------------------------|
| **Painel de Controle**                       | Configurações clássicas do sistema      |
| **Gerenciador de Tarefas**                   | Monitoramento de processos e desempenho |
| **Gerenciamento do Computador**              | Acesso a logs, serviços e discos        |
| **Editor de Diretiva de Grupo (gpedit.msc)** | Políticas locais                        |
| **Editor de Registro (regedit)**             | Configurações do sistema em nível baixo |
| **msconfig**                                 | Configuração de inicialização           |
| **Services.msc**                             | Gerencia serviços e daemons             |
| **Eventvwr.msc**                             | Visualiza logs de eventos               |
| **Task Scheduler**                           | Agendamento de tarefas automatizadas    |
| **DISKPART**                                 | Gerenciamento de partições via CLI      |
| **PowerShell**                               | Automação e administração avançada      |

### Gerenciamento de Usuários

| Ferramenta ou comando     | Função                                             |
|---------------------------|----------------------------------------------------|
| `lusrmgr.msc`             | Gerencia usuários e grupos locais (exceto no Home) |
| `net user`                | Cria, remove ou modifica usuários via CLI          |
| Painel de Controle        | Gerenciamento básico de contas                     |
| Active Directory (AD)     | Em servidores Windows, gerencia rede e domínios    |

```powershell
net user rafael /add
net localgroup administradores rafael /add
```

### Segurança e Controle de Acesso

- **UAC (User Account Control)**: controle de permissões elevadas
- **Permissões NTFS**: leitura, gravação, modificação, controle total
- **Firewall do Windows**: regras de entrada/saída por perfil (domínio, público, privado)
- **BitLocker**: criptografia de disco nativa
- **Windows Defender**: antivírus e antimalware padrão
- **Políticas de Grupo (GPO)**: controle granular de configurações

### Gerenciamento de Disco

| Ferramenta           | Finalidade                                |
|----------------------|-------------------------------------------|
| Gerenciador de Disco | Criação, formatação e expansão de volumes |
| `diskpart`           | CLI para particionamento                  |
| `chkdsk`             | Verifica integridade do disco             |
| `defrag`             | Desfragmenta disco (HDD)                  |
| `format`             | Formata volumes via CLI                   |

```cmd
diskpart
list disk
select disk 0
create partition primary
format fs=ntfs quick
```

### Comandos de Rede no Windows

| Comando       | Função                               |
|---------------|--------------------------------------|
| `ipconfig`    | Mostra IPs e interfaces de rede      |
| `ping`        | Testa conectividade                  |
| `tracert`     | Rastreia rota até destino            |
| `nslookup`    | Consulta servidores DNS              |
| `netstat -an` | Lista conexões de rede e portas      |
| `tasklist`    | Lista processos ativos               |
| `net use`     | Mapeia/unmapeia unidades de rede     |
| `net share`   | Compartilhamento de pastas           |
| `net view`    | Visualiza computadores na rede local |
| `arp -a`      | Exibe tabela ARP                     |
| `route print` | Mostra tabela de rotas IP            |

### PowerShell (CLI avançada)

```powershell
# Criar usuário
New-LocalUser -Name "rafael" -Password (ConvertTo-SecureString "Senha@123" -AsPlainText -Force)

# Habilitar serviço
Start-Service -Name wuauserv

# Listar processos
Get-Process

# Listar atualizações instaladas
Get-HotFix

# Ver espaço em disco
Get-PSDrive
```

### Logs e Diagnóstico

| Ferramenta              | Descrição                            |
|-------------------------|--------------------------------------|
| Visualizador de Eventos | Logs de sistema, segurança e apps    |
| `perfmon`               | Monitoramento de desempenho          |
| `dxdiag`                | Diagnóstico gráfico e som            |
| `Reliability Monitor`   | Histórico de estabilidade do sistema |

### Backup e Restauração

- **Histórico de Arquivos**: cópias automáticas de bibliotecas
- **Backup e Restauração (Windows 7)**: imagem do sistema
- **Ponto de Restauração**: snapshots do sistema
- **OneDrive**: sincronização e backup na nuvem
- **Ferramentas externas**: Cobian Backup, Acronis, Veeam Agent

### Recursos Avançados (Servidor)

| Recurso              | Função                                  |
|----------------------|-----------------------------------------|
| Active Directory     | Autenticação centralizada e políticas   |
| DNS e DHCP           | Gerência de nomes e IPs na rede         |
| Hyper-V              | Virtualização de servidores/desktops    |
| RDP (Remote Desktop) | Acesso remoto ao sistema                |
| WSUS                 | Atualizações centralizadas              |
| Serviços de Arquivo  | Compartilhamento com cotas e permissões |

### Questão de Concurso

A ferramenta usada para editar políticas locais de segurança em estações Windows é:

a) msconfig  
b) regedit  
c) services.msc  
d) gpedit.msc  
e) taskmgr

> **Gabarito: d)** gpedit.msc

## Configuração e administração de servidores Windows Server 2016 e Linux

### Windows Server

| Ferramenta         | Descrição                                           |
|--------------------|-----------------------------------------------------|
| PowerShell DSC     | Desired State Configuration – automação declarativa |
| Group Policy (GPO) | Políticas de segurança, login, scripts              |
| Task Scheduler     | Agendamento de tarefas e scripts                    |
| Event Forwarding   | Coleta centralizada de logs com `wecutil` e `winrm` |

```powershell
# Exemplo PowerShell - Criar novo usuário e adicionar a grupo
New-LocalUser "usuario1" -Password (ConvertTo-SecureString "Senha123!" -AsPlainText -Force)
Add-LocalGroupMember -Group "Administradores" -Member "usuario1"
```

### Linux

| Ferramenta     | Finalidade                                   |
|----------------|----------------------------------------------|
| Cron / Anacron | Agendamento de tarefas em background         |
| Systemd timers | Alternativa moderna ao cron                  |
| Bash scripts   | Automatização de tarefas administrativas     |
| Ansible        | Gerenciamento de configuração e orquestração |

```bash
# Exemplo cron: backup diário às 2h
0 2 * * * /usr/local/bin/backup.sh
```

### Segurança Avançada

| Item               | Windows Server              | Linux                                    |
|--------------------|-----------------------------|------------------------------------------|
| Auditoria          | Event Viewer, AuditPol      | AuditD, `ausearch`, `auditctl`           |
| Hardening          | STIG, SecPol.msc            | CIS Benchmarks, `lynis`, `chkrootkit`    |
| Controle de acesso | ACLs, GPO                   | `setfacl`, `getfacl`, PAM                |
| Autenticação       | Active Directory + Kerberos | LDAP, SSSD, Kerberos, sudoers            |
| VPN                | RRAS, Always On VPN         | OpenVPN, WireGuard, strongSwan           |
| Firewall           | Windows Defender Firewall   | `iptables`, `firewalld`, `ufw`           |
| SELinux / AppArmor | —                           | Mandatory Access Control (MAC) no kernel |

### Diagnóstico, Logs e Monitoramento

| Ferramenta             | Windows Server                             | Linux                                          |
|------------------------|--------------------------------------------|------------------------------------------------|
| Logs                   | Event Viewer, `Get-WinEvent`               | `journalctl`, `/var/log/`, rsyslog             |
| Diagnóstico de rede    | `netsh`, `ping`, `tracert`, `telnet`       | `ss`, `ip`, `tcpdump`, `nmap`, `wireshark`     |
| Performance            | PerfMon, Resource Monitor                  | `htop`, `iotop`, `vmstat`, `dstat`             |
| Monitoramento central  | Zabbix, Nagios, PRTG                       | Zabbix, Prometheus, Netdata                    |

### Serviços de Infraestrutura e Domínio

| Serviço          | Windows Server           | Linux (equivalente)                      |
|------------------|--------------------------|------------------------------------------|
| Active Directory | Gerenciamento de domínio | Samba4 AD/DC, OpenLDAP                   |
| DNS              | DNS Manager              | BIND, dnsmasq                            |
| DHCP             | DHCP Manager             | `isc-dhcp-server`, `dhcpd.conf`          |
| GPO              | `gpedit.msc`, `gpmc.msc` | Políticas via Puppet, Ansible ou scripts |
| WSUS             | Atualizações locais      | Espelhos de repositório (APT/YUM proxy)  |

### Virtualização e Contêineres

| Tecnologia        | Windows Server                                       | Linux                                       |
|-------------------|------------------------------------------------------|---------------------------------------------|
| Hyper-V           | Nativo a partir do Server 2012                       | Não nativo, possível com drivers especiais  |
| Docker            | Desde Server 2016 (com suporte a containers Windows) | Nativo: Docker CE/EE, Podman                |
| KVM/QEMU          | —                                                    | Kernel-based VM com boa performance         |
| Proxmox / Libvirt | —                                                    | Ambiente de virtualização e gestão completa |
| LXC               | —                                                    | Contêineres de sistema (não só apps)        |


### Backup, Restauração e Alta Disponibilidade

| Ferramenta/Conceito | Windows Server                   | Linux                          |
|---------------------|----------------------------------|--------------------------------|
| Backup              | Windows Backup, Veeam, Acronis   | `rsync`, `tar`, Bacula, Amanda |
| Shadow Copy         | VSS – Volume Shadow Copy         | LVM Snapshots, ZFS snapshots   |
| Failover Cluster    | Cluster Manager + Shared Storage | Pacemaker + Corosync, DRBD     |
| Replicação          | DFS-R (File Server)              | `rsync`, GlusterFS, DRBD       |
| Imagem de sistema   | Sysprep + WIM / DISM             | `dd`, Clonezilla, `partclone`  |

### Compartilhamento e Arquivos

| Recurso          | Windows Server                       | Linux                               |
|------------------|--------------------------------------|-------------------------------------|
| Compartilhamento | SMB (via Explorador, `net share`)    | Samba (via `smb.conf`)              |
| NFS              | Instalável via Roles                 | `nfs-kernel-server`, `/etc/exports` |
| FTP              | IIS FTP Server                       | `vsftpd`, `proftpd`, `pure-ftpd`    |
| DFS              | Distributed File System (Enterprise) | GlusterFS, CephFS                   |


### Questão Simulada (Estilo CEBRASPE)

Um analista precisa configurar autenticação de usuários Linux contra um servidor Windows Server 2016 com Active Directory. Qual das opções abaixo representa o método mais indicado?

a) Utilizar NFS com compartilhamento LDAP  
b) Configurar Samba apenas com arquivos locais  
c) Usar SSSD com Kerberos e LDAP integrados ao AD  
d) Instalar um servidor FTP e autenticar via radius  
e) Utilizar rsync com SSH e firewall ativo

> **Gabarito: c)** Usar SSSD com Kerberos e LDAP integrados ao AD



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
