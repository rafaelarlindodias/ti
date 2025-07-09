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


---

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
