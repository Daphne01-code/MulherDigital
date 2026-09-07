
# Modelagem de Rede Corporativa em 3 Camadas (Cisco)

> **Modulo 2:** Conceitos Basicos de Rede — Pratica 4 (Final)  
> **Orientacao:** Profa. Karen Oliveira Camargo  
> **Objetivo:** Implementacao e validacao do modelo hierarquico de tres camadas da Cisco utilizando o simulador Cisco Packet Tracer.

---

## Visao Geral do Projeto

Este laboratorio teve como objetivo montar a infraestrutura de rede corporativa para uma empresa do zero, estruturando o tráfego de dados de acordo com o modelo de design hierarquico recomendado pela Cisco (**Access, Distribution e Core**).

---

## Arquitetura e Modelo de 3 Camadas

A rede foi dividida em tres niveis funcionais para garantir escalabilidade, redundancia e alta performance:

| Camada | Equipamento Utilizado | Funcao na Infraestrutura |
| :--- | :--- | :--- |
| **1. Acesso (Access)** | Switch Cisco `2960` | Porta de entrada da rede local; conexao direta dos computadores de funcionarios e laboratorios. |
| **2. Distribuicao (Distribution)** | Switch Multilayer Cisco `3650` | Agregacao do trafego proveniente da camada de acesso, Roteamento Inter-VLAN e controle de politicas de tráfego. |
| **3. Nucleo (Core)** | Roteador Cisco `4331` | Backhaul/Autoestrada de alta velocidade focado no roteamento rapido de dados para redes externas/Internet. |

---

## O Que Foi Implementado

* **Configuracao via CLI (Command Line Interface):** Ativacao e configuracao dos ativos Cisco exclusivamente por meio de linha de comando.
* **Enderecamento IP:** Atribuicao de enderecos IP logicos para identificacao e comunicacao unica dos hosts na rede.
* **Validacao de Uplinks e Downlinks:** Checagem e estruturacao das conexoes fisicas e logicas entre os comutadores e o roteador principal.
* **Analise de Trafego (ICMP):** Execucao e rastreamento visual de pacotes ICMP em modo de simulacao para validacao de conectividade de ponta a ponta.

---

## Resultados Obtidos

* Topologia 100% operacional com convergencia de rede validada.
* Dominio pratico dos comandos fundamentais do Cisco IOS.
* Compreensao do comportamento do tráfego de dados ao longo das camadas de Acesso, Distribuicao e Core.

---
<img width="1280" height="724" alt="1786932360165" src="https://github.com/user-attachments/assets/f9c1dccf-0d92-43ae-ab04-c9302c8c0933" />

##  Tags
`Redes de Computadores` • `Cisco Packet Tracer` • `Modelo 3 Camadas` • `CLI Cisco` • `CCNA` • `Infraestrutura IT`
