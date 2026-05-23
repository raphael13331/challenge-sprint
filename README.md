# 🌿 VegTrack — Registro de Ocorrências de Vegetação em Rodovias

> Solução mobile para operadores de campo no monitoramento e registro de ocorrências de vegetação nas rodovias concedidas da Motiva (CCR).

---

## 👥 Integrantes

| Nome | RM |
|---|---|
| Leonardo Luster Gomes | RM564448 |
| Raphael Talarico | RM565219 |
| Nelson Troccoli | RM562815 |
| Kauã da Silva | RM564625 |

---
## Sobre o Projeto

Este projeto consiste no desenvolvimento de um aplicativo mobile no contexto do Challenge CCR Motiva, com o objetivo de aprimorar o processo de monitoramento e gestão da vegetação nas rodovias concedidas.

Atualmente, esse processo é realizado de forma manual e descentralizada, o que dificulta o controle das ocorrências, a padronização das informações e a tomada de decisão por parte dos gestores. A proposta do projeto é digitalizar esse fluxo, tornando-o mais eficiente, rastreável e confiável.
---
## 🚨 Problema Escolhido

As frentes de conservação da Motiva enfrentam dificuldades no registro padronizado de ocorrências de vegetação ao longo das rodovias concedidas. O processo atual é fragmentado: operadores de campo utilizam anotações manuais, comunicações por rádio/WhatsApp e registros em papel, o que gera:

- **Falta de rastreabilidade** das ocorrências (onde, quando, quem registrou)
- **Perda de informações** no repasse entre campo e supervisão
- **Dificuldade de atendimento** às exigências regulatórias da ARTESP e ANTT
- **Atraso na tomada de decisão** dos supervisores e gestores
- **Ausência de histórico georreferenciado** para planejamento de intervenções

---

## 👤 Persona Principal

**Carlos Eduardo, 34 anos — Operador de Campo**

- Trabalha em frentes de conservação de rodovias há 6 anos
- Realiza inspeções diárias ao longo de trechos da rodovia
- Tem ensino médio completo; uso moderado de smartphone (Android)
- Maior frustração: ter que ligar para o supervisor para reportar cada ocorrência e depois ainda preencher um formulário em papel
- Necessidade: um app simples, rápido e que funcione mesmo com sinal instável de internet

---
#### Necessidades

* Registrar ocorrências de forma rápida e prática
* Utilizar uma ferramenta simples no dispositivo móvel
* Garantir armazenamento correto das informações
* Reduzir retrabalho e erros

---

## 💡 Proposta de Solução

**VegTrack** é um aplicativo mobile (Android/iOS) voltado ao operador de campo que permite:

1. **Registrar ocorrências de vegetação** com foto, localização GPS automática e classificação do tipo de problema (vegetação alta, árvore caída, espécie invasora, dano estrutural por raízes, etc.)
2. **Preencher um checklist padronizado** por trecho inspecionado, garantindo conformidade com as exigências da ARTESP/ANTT
3. **Sincronizar os registros** com a supervisão em tempo real (ou em modo offline com sync posterior)
4. **Consultar o histórico** de ocorrências do seu trecho de responsabilidade

O foco é na **simplicidade e agilidade do fluxo de campo**: o operador abre o app, bate a foto, classifica, confirma a localização e envia — em menos de 30 segundos.

---
### Requisitos Funcionais (RF)

* RF01: Permitir autenticação do usuário
* RF02: Permitir o cadastro de novos registros
* RF03: Permitir a captura de fotos pelo dispositivo
* RF04: Registrar automaticamente a localização do usuário
* RF05: Permitir a classificação do tipo de vegetação ou problema
* RF06: Armazenar os registros realizados
* RF07: Exibir o histórico de registros
* RF08: Permitir a visualização dos registros em mapa
 ---

## 🎨 Protótipo Navegável (Figma)

🔗 **[Acessar Protótipo no Figma](https://www.figma.com/proto/DnZ2DDJSj2KItkNOfpQXNP/Sem-t%C3%ADtulo?node-id=5-6&starting-point-node-id=3%3A2)**

> O protótipo cobre os fluxos principais: Login → Registro de Ocorrência (foto + classificação + GPS) → Histórico de Registros.

---
