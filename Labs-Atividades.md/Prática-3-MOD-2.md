#  PRÁTICA 3: Simulação de Rede SOHO com Cisco Packet Tracer

> **Módulo 2:** Conceitos Básicos de Rede — Prática 3  
> *A teoria só se consolida quando colocamos a mão na massa!*

---

## Visão Geral do Projeto
Este projeto consiste na montagem e configuração **do zero** de uma infraestrutura de rede para um pequeno escritório/home office (**SOHO**), aplicando conceitos essenciais de conectividade, endereçamento IP e segurança sem fio através do **Cisco Packet Tracer**.
<img width="967" height="670" alt="image" src="https://github.com/user-attachments/assets/9310d075-5548-4ce6-a8f1-0466af50d5c2" />


---

##  Arquitetura da Rede

* **Conectividade Externa:** Emulação de Link de Internet via Nuvem e Cable Modem.
* **Core da Rede:** Roteador Wireless (`WRT300N`) atuando simultaneamente como:
  * Roteador / Switch
  * Ponto de Acesso (Wi-Fi)
  * Servidor DHCP
* **Dispositivos Finais:** PCs, Notebook, Smartphone e Impressora corporativa (conexões cabeadas e sem fio).

---

##  O Que Foi Implementado

| Etapa | Descrição |
| :--- | :--- |
| **Cabeamento Estruturado** | Conexões físicas com cabos diretos (*Copper Straight-Through*) e cabo coaxial no link de internet. |
| **Segurança Wireless** | Configuração de SSID dedicado e implementação do protocolo **WPA2 Personal** para proteção da rede sem fio. |
| **Upgrade de Hardware** | Customização física do Notebook no simulador: substituição da placa Ethernet por módulo Wi-Fi (`WPC300N`). |
| **Automação IP (DHCP)** | Configuração do DHCP no roteador para distribuição dinâmica de IPs (Faixa `192.168.0.X`). |
| **Validação de Conectividade** | Testes de comunicação de ponta a ponta via prompt de comando (`ping`). |

---

## Principais Aprendizados
* Entendimento prático sobre o comportamento real e fluxo dos pacotes de dados.
* Importância do controle de acesso e criptografia em redes wireless.
* Diagnóstico básico e resolução de problemas de conectividade (*Troubleshooting*).
<img width="1280" height="724" alt="1786932360165" src="https://github.com/user-attachments/assets/1b1cc11f-56ca-4bda-b342-1440c1d6b7d7" />

---

## Tags
`Redes de Computadores` • `Cisco Packet Tracer` • `Infraestrutura IT` • `SOHO` • `DHCP` • `WPA2`
