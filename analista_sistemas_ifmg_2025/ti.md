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

  - Por Escopo Geográfico
  
| Tipo | Sigla | Características |
|------|-------|------------------|
| Local | LAN | Pequenas áreas (escolas, escritórios) |
| Metropolitana | MAN | Áreas urbanas, campus universitários |
| Ampla | WAN | Grandes distâncias (Internet) |
| Sem fio | WLAN | Versão sem fio de LAN, padrão 802.11 |

  - Por Arquitetura

    - **Cliente-servidor**: cliente solicita, servidor fornece.
    - **Ponto-a-ponto (P2P)**: todos os nós são iguais.
    
**Topologias de rede**
  - **Barramento (Bus)**: um único cabo conecta todos os nós.
  - **Anel (Ring)**: conexão circular entre os nós.
  - **Estrela (Star)**: todos os dispositivos conectam a um ponto central.
  - **Malha (Mesh)**: todos os nós conectados entre si.
  - **Árvore (Tree)**: hierarquia de dispositivos.
  - **Híbrida**: combinação de topologias anteriores.

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
