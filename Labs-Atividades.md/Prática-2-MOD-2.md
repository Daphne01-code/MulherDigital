# 🌐 PRÁTICA 2: MÓDULO 2

## Configuração de Serviços (HTTP/DNS) e Análise de Protocolos

Este relatório descreve o laboratório prático de montagem de uma topologia de rede local, focado no fornecimento de serviços da camada de aplicação e no acompanhamento do fluxo de dados no nível de transporte.

Neste laboratório prático, construí uma rede funcional do zero para configurar serviços de aplicação e analisar o comportamento dos protocolos na camada de transporte.

---

## 🛠️ Recursos Utilizados

| Recurso                         | Descrição                         |
| ------------------------------- | --------------------------------- |
| 💻 **Ambiente de Simulação**    | Cisco Packet Tracer               |
| 🖥️ **Servidor Multifuncional** | Hospedando os serviços HTTP e DNS |
| 🔀 **Ativo de Rede**            | Switch Cisco 2960 (Camada 2)      |
| 🖥️ **Estação de Trabalho**     | PC Cliente (*End Device*)         |

---

## ⚙️ Procedimento Experimental e Configurações

### 1. 🔌 Montagem da Rede

PC e servidor conectados ao switch no Cisco Packet Tracer.

### 2. 🌐 Configuração de IP

Definição dos endereços IP estáticos do PC e do servidor.

### 3. 🌎 Servidor Web

Ativação dos serviços **HTTP/HTTPS** e personalização da página `index.html`.

### 4. 🔎 Servidor DNS

Criação do domínio:

```text
www.aula.com
```

O domínio foi configurado para apontar para o endereço IP do servidor.

### 5. 📡 Teste de Conectividade

Utilização do comando `ping` para verificar a comunicação entre os dispositivos da rede.

```bash
ping <IP_DO_SERVIDOR>
```

### 6. 🔍 Teste do DNS

Utilização do comando `nslookup` para confirmar a resolução do domínio:

```bash
nslookup www.aula.com
```

### 7. 🌐 Acesso à Página Web

No PC cliente, foi realizado o acesso ao site utilizando o endereço:

```text
www.aula.com
```

### 8. 📊 Análise de Tráfego

Utilização do **modo Simulation** do Cisco Packet Tracer para observar o fluxo dos seguintes protocolos:

* **DNS**
* **TCP**
* **HTTP**
* **ICMP**

### 9. 📚 Análise das Camadas

Observação do processo de encapsulamento dos dados e dos cabeçalhos presentes nas camadas:

* **Camada 4 — Transporte**
* **Camada 7 — Aplicação**

---

## 🖼️ Evidências da Prática

### Topologia da Rede

![Topologia da rede](./imagens/pratica2-topologia.png)

### Configuração e Testes

![Configuração e testes](./imagens/pratica2-testes.png)

---

## 🎯 Conclusão

A prática possibilitou a montagem de uma rede local funcional e a configuração dos serviços **HTTP e DNS** em um servidor no Cisco Packet Tracer.

Além disso, foi possível verificar a conectividade entre os dispositivos por meio do **ICMP**, testar a resolução de nomes utilizando o **DNS** e acompanhar o estabelecimento da comunicação **TCP** durante o acesso ao servidor HTTP.

A utilização do modo de simulação permitiu observar, na prática, o fluxo dos pacotes e o funcionamento dos protocolos nas diferentes camadas da rede, especialmente nas **camadas de Transporte (4) e Aplicação (7)**.
