# ☁️ Resumo do Lab: Benefícios da Nuvem com Microsoft Azure AZ-900
Este repositório reúne os principais aprendizados adquiridos durante o curso de **Benefícios da Computação em Nuvem** da plataforma [DIO.me](https://web.dio.me), Conceitos Iniciais de Cloud com Azure - Módulo 1. O foco está nos benefícios e aplicações práticas da plataforma Microsoft Azure, explorando seus recursos e funcionalidades. O Bootcamp oferece uma base sólida em tecnologias de nuvem, abordando desde os conceitos fundamentais até os componentes essenciais da arquitetura Azure. Entre os temas estudados estão: criação e gerenciamento de máquinas virtuais, configuração de bancos de dados e soluções de armazenamento, além de tópicos avançados como arquitetura em nuvem, governança, monitoramento e segurança de ambientes cloud. 

---

## 📘 Tópicos Abordados

### 🌐 Introdução à Computação em Nuvem
- A computação em nuvem permite acesso remoto a recursos de TI via internet, com alta disponibilidade e flexibilidade.
- O Microsoft Azure é uma das principais plataformas de nuvem, oferecendo soluções em IaaS, PaaS e SaaS.

### 🚀 Benefícios da Nuvem Azure

#### 🔄 Escalabilidade e Elasticidade
- **Escalabilidade**: capacidade de aumentar ou reduzir recursos conforme a demanda.
- **Elasticidade**: ajuste automático dos recursos para atender variações de carga, otimizando custos e desempenho.

#### 🔒 Confiabilidade
- Alta disponibilidade garantida por uma rede global de data centers.
- Redundância e recuperação de desastres integradas.

#### 📊 Previsibilidade
- Modelos de cobrança sob demanda e métricas de uso que facilitam o planejamento financeiro.
- Monitoramento contínuo para prever consumo e evitar surpresas.

#### 🛡️ Segurança
- Criptografia de dados, autenticação multifator e políticas de acesso.
- Conformidade com normas internacionais e responsabilidade compartilhada.

#### 🧭 Governança
- Ferramentas para controle de políticas, auditoria e conformidade.
- Definição de regras de uso e rastreamento de atividades.

#### 🧰 Gerenciabilidade
- Interface intuitiva e automações via scripts e APIs.
- Monitoramento centralizado, alertas e relatórios para facilitar a administração.

### ☁️ Criando Máquinas Virtuais na Azure
Este guia apresenta os passos essenciais para criar e gerenciar uma máquina virtual (VM) na plataforma Microsoft Azure, utilizando o PowerShell ou o Portal da Azure.
O SLA é o compromisso da Microsoft com a **disponibilidade e confiabilidade** dos serviços. Ele garante que os recursos estarão disponíveis por um percentual mínimo de tempo.

### Principais Garantias de SLA

| Configuração da VM                      | SLA de Disponibilidade |
|----------------------------------------|------------------------|
| VM única                               | 99.9%                 |
| VM em Conjunto de Disponibilidade      | 99.95%                |
| VM em Zonas de Disponibilidade         | 99.99%                |

### Vantagens do SLA

- Redução de tempo de inatividade: com um SLA claro, as empresas podem planejar suas operações e mitigar riscos de interrupções, sabendo que o serviço tem uma garantia de estabilidade.
- Compensações financeiras em caso de falhas: o SLA estabelece métricas claras sobre a qualidade do serviço, como tempo de atividade, desempenho e suporte técnico, garantindo transparência na relação entre o provedor e o cliente.
- Confiabilidade para aplicações críticas: o SLA oferece uma garantia de que o serviço estará disponível por uma porcentagem de tempo acordada (por exemplo, 99,9%). Se o provedor não cumprir essa meta, podemos ser compensados financeiramente, o que aumenta a confiança na plataforma.

---

## 🧱 Opções de Disponibilidade na Azure
Ao criarmos uma máquina virtual no Azure, temos várias opções para garantir a alta disponibilidade e a resiliência do nosso serviço.
A escolha depende do nível de proteção que a aplicação precisa:

### 1. Conjunto de Disponibilidade (Availability Set)

- Distribui VMs entre múltiplos racks físicos
- Protege contra falhas de hardware local
- Ideal para redundância dentro da mesma região

### 2. Zonas de Disponibilidade (Availability Zones)
São locais físicos separados e independentes dentro de uma região do Azure. Cada zona tem sua própria infraestrutura de energia, refrigeração e rede.
Ao distribuir as VMs entre várias zonas, protegemos nossa aplicação contra falhas de datacenter. Se uma zona ficar inoperante, as VMs em outras zonas continuarão funcionando.

### 3. Conjuntos de Escala (Scale Sets)

- Cria múltiplas VMs idênticas
- Permite escalabilidade automática e balanceamento de carga

---

## 🗄️ Contas de Armazenamento e Tipos de Disco

Ao criar uma VM, é necessário escolher o tipo de disco e a conta de armazenamento.

### Tipos de Disco

| Tipo de Disco   | Desempenho | Uso Ideal                          |
|-----------------|------------|------------------------------------|
| HDD Standard    | Baixo      | Testes, cargas leves               |
| SSD Standard    | Médio      | Produção com custo acessível       |
| SSD Premium     | Alto       | Aplicações críticas, bancos de dados|

### Tipos de Conta de Armazenamento
* Ao criar uma conta de armazenamento no Azure, precisamos escolher uma opção de redundância para garantir a durabilidade e a alta disponibilidade dos dados. A escolha certa é crucial e depende do nível de proteção que a empresa precisa, além do orçamento disponível.

- **Standard Storage**: Suporta HDD e SSD padrão. 
- **Premium Storage**: Necessária para discos SSD premium
- **ZRS (Zone Redundant Storage)**: Redundância entre zonas
1. LRS (Locally Redundant Storage): é a opção de menor custo e menos redundante
2. ZRS (Zone-Redundant Storage): replica os dados três vezes em diferentes Zonas de Disponibilidade (Availability Zones) dentro da mesma região.
3. GRS (Geo-Redundant Storage): replica os dados para uma região secundária distante, a centenas de quilômetros da região primária.
4. GZRS (Geo-Zone-Redundant Storage): é a opção de redundância mais robusta.

---

## 📦 Considerações ao Criar uma VM

Ao configurar a máquina virtual, podemos definir:

- Região (localização geográfica)
- Tipo de disco e desempenho
- Conjunto ou zona de disponibilidade
- Conta de armazenamento
- Rede virtual e IP público
- Arquitetura com base no SLA desejado

---

## ✅ Conclusão

O laboratório sobre **Benefícios da Nuvem e Criação de Máquinas Virtuais na Azure** reforçou a importância da computação em nuvem como uma solução moderna, escalável e segura para empresas e desenvolvedores. Através da plataforma Microsoft Azure, foi possível compreender:

- Como o **SLA (Service Level Agreement)** garante previsibilidade, confiabilidade e compensações em caso de falhas, fortalecendo a confiança na infraestrutura de nuvem.
- As diferentes **opções de disponibilidade**, como Conjuntos de Disponibilidade e Zonas de Disponibilidade, que aumentam a resiliência dos sistemas.
- A escolha adequada de **tipos de disco e contas de armazenamento**, que impactam diretamente no desempenho e custo das aplicações.
- A facilidade de **criar, configurar e gerenciar VMs** com flexibilidade, seja via Portal da Azure ou por meio de automações com PowerShell e CLI.

Esses conhecimentos são fundamentais para arquitetar soluções robustas, econômicas e preparadas para escalar conforme a demanda. A nuvem não é apenas uma tendência — é uma base estratégica para inovação.

> Este conteúdo faz parte do projeto **Criando máquinas Virtuais na Azure - Laboratório** da plataforma DIO.me.

---
 
## 📚 Recursos Complementares
- [Início Rápido: criar Instância Gerenciada de SQL do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
- [Tutorial oficial para criar e gerenciar VMs Windows](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/tutorial-manage-vm)
- [Guia rápido para criar instância gerenciada de SQL](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql&tabs=cli) 

📎 Link do curso: [Microsoft Azure AZ-900 - DIO.me](https://web.dio.me/track/microsoft-azure-az-900)
