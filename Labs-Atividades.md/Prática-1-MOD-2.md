# 🌐 Prática 1: Automação de Redes — Implementando Servidor DHCP em Roteador Cisco

Prover conectividade eficiente em uma **LAN** exige mais do que conectar cabos. Exige **automação, escalabilidade e mitigação de erros operacionais**.

## 🎯 Objetivo do Projeto

Automatizar a entrega de parâmetros essenciais de rede para os dispositivos clientes.

Em vez de configurar máquina por máquina manualmente, o próprio roteador assume o papel de distribuir automaticamente:

* **Endereço IP:** identificador único do dispositivo.
* **Máscara de Sub-rede:** define os limites da rede lógica.
* **Gateway Padrão:** porta de saída para outras redes e para a Internet.
* **Servidor DNS:** traduz nomes de domínio em endereços IP.

## 🛠️ Recursos e Ferramentas Utilizadas

* **Cisco Packet Tracer:** simulador de ambientes de redes.
* **Roteador Cisco 2911:** atuando como Gateway e Servidor DHCP.
* **Switch Cisco 2960:** interligando os dispositivos locais.
* **Hosts:** 2 PCs clientes configurados para recebimento dinâmico de IP.

## ⚙️ Etapas da Implementação — Cisco IOS

### 1. Exclusão de IPs

Foi realizada a reserva do endereço IP utilizado pelo gateway, evitando conflitos de endereçamento.

```cisco
Router> enable
Router# configure terminal

Router(config)# ip dhcp excluded-address 192.168.1.1
```

### 2. Criação do Pool DHCP

Foi criado o pool DHCP denominado `MULHER_DIGITAL2026`.

```cisco
Router(config)# ip dhcp pool MULHER_DIGITAL2026
```

### 3. Definição dos Parâmetros de Rede

Foi definida a rede local `192.168.1.0/24`, juntamente com o gateway padrão e o servidor DNS.

```cisco
Router(dhcp-config)# network 192.168.1.0 255.255.255.0
Router(dhcp-config)# default-router 192.168.1.1
Router(dhcp-config)# dns-server 8.8.8.8
```

### 4. Configuração da Interface do Roteador

A interface `GigabitEthernet0/0` foi configurada com o endereço IP `192.168.1.1`.

```cisco
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
```

### 5. Persistência das Configurações

Para evitar a perda das configurações após o reinício do equipamento, foi utilizado o comando `write`.

```cisco
Router# write
```

## 🔄 Funcionamento do DHCP — Processo DORA

Ao alterar a configuração dos hosts de **Static** para **DHCP**, ocorreu automaticamente o processo **DORA**:

1. **Discover** — o cliente procura um servidor DHCP.
2. **Offer** — o servidor oferece um endereço IP.
3. **Request** — o cliente solicita o endereço oferecido.
4. **Acknowledge** — o servidor confirma a concessão do endereço.

## ✅ Validação e Resultados

Após a configuração, os computadores receberam automaticamente seus parâmetros de rede, sem necessidade de configuração manual.

| Dispositivo | Endereço IP   | Máscara               |
| ----------- | ------------- | --------------------- |
| **PC-0**    | `192.168.1.2` | `255.255.255.0 (/24)` |
| **PC-1**    | `192.168.1.3` | `255.255.255.0 (/24)` |

### 📌 Resultado

Os endereços foram preenchidos em **segundos**, sem intervenção manual e reduzindo o risco de **conflitos ou duplicidade de endereços IP**.

A prática demonstrou, na prática, como a automação de serviços de rede pode tornar a infraestrutura **mais eficiente, escalável, organizada e resiliente**.

## 💡 Conclusão

A implementação do servidor DHCP no roteador Cisco permitiu automatizar a distribuição dos principais parâmetros de rede aos dispositivos clientes.

Com isso, foi possível eliminar a necessidade de configuração manual de cada computador e demonstrar a importância da **automação de infraestrutura de redes** para ambientes que necessitam de eficiência, escalabilidade e redução de erros operacionais.

