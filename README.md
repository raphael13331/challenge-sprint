#  VegTrack — Registro de Ocorrências de Vegetação em Rodovias

> Solução mobile para operadores de campo no monitoramento e registro de ocorrências de vegetação nas rodovias concedidas da Motiva (CCR).

---

##  Integrantes

* Leonardo Luster Gomes
* Raphael Talarico
* Nelson Troccoli
* Kauã da Silva

---

##  Problema Escolhido

As frentes de conservação da Motiva enfrentam dificuldades no registro padronizado de ocorrências de vegetação ao longo das rodovias concedidas. O processo atual é fragmentado: operadores de campo utilizam anotações manuais, comunicações por rádio/WhatsApp e registros em papel, o que gera:

- **Falta de rastreabilidade** das ocorrências (onde, quando, quem registrou)
- **Perda de informações** no repasse entre campo e supervisão
- **Dificuldade de atendimento** às exigências regulatórias da ARTESP e ANTT
- **Atraso na tomada de decisão** dos supervisores e gestores
- **Ausência de histórico georreferenciado** para planejamento de intervenções

---

##  Persona Principal

**Carlos Eduardo, 34 anos — Operador de Campo**

- Trabalha em frentes de conservação de rodovias há 6 anos
- Realiza inspeções diárias ao longo de trechos da rodovia
- Tem ensino médio completo; uso moderado de smartphone (Android)
- Maior frustração: ter que ligar para o supervisor para reportar cada ocorrência e depois ainda preencher um formulário em papel
- Necessidade: um app simples, rápido e que funcione mesmo com sinal instável de internet

---

##  Proposta de Solução

**VegTrack** é um aplicativo mobile (Android/iOS) voltado ao operador de campo que permite:

1. **Registrar ocorrências de vegetação** com foto, localização GPS automática e classificação do tipo de problema (vegetação alta, árvore caída, espécie invasora, dano estrutural por raízes, etc.)
2. **Preencher um checklist padronizado** por trecho inspecionado, garantindo conformidade com as exigências da ARTESP/ANTT
3. **Sincronizar os registros** com a supervisão em tempo real (ou em modo offline com sync posterior)
4. **Consultar o histórico** de ocorrências do seu trecho de responsabilidade

O foco é na **simplicidade e agilidade do fluxo de campo**: o operador abre o app, bate a foto, classifica, confirma a localização e envia — em menos de 30 segundos.

---

## Stack Tecnológica e Justificativa

| Tecnologia | Papel | Justificativa |
|---|---|---|
| **React Native** | Framework mobile | Cross-platform (Android/iOS) com único codebase; ampla comunidade e suporte corporativo (Meta) |
| **Expo (SDK 51+)** | Toolchain e runtime | Abstrai configurações nativas complexas; APIs prontas para câmera, GPS e notificações; facilita build e distribuição |
| **Expo Camera** | Captura de foto | API nativa de câmera integrada ao Expo; suporte a metadados EXIF com timestamp |
| **Expo Location** | Geolocalização | Acesso ao GPS do dispositivo; suporte a modo foreground e offline; retorna coordenadas com precisão adequada para uso em rodovias |
| **React Navigation v6** | Navegação entre telas | Biblioteca padrão do ecossistema React Native; suporte a Stack, Tab e Drawer navigation |
| **AsyncStorage** | Persistência local | Armazenamento local de registros para funcionamento offline; leve e sem dependências nativas extras |
| **React Query (TanStack)** | Gerenciamento de estado assíncrono | Controle de cache, sincronização e retry automático — essencial para cenários com conectividade intermitente |
| **Axios** | Cliente HTTP | Requisições à API backend com suporte a interceptors e timeout configurável |
| **Node.js + Express** | Backend API (mock/MVP) | API REST leve para receber e armazenar registros; fácil de prototipar e escalar |
| **Firebase Firestore** | Banco de dados em nuvem | Sincronização em tempo real, suporte offline nativo, sem necessidade de infraestrutura própria no MVP |
| **Firebase Storage** | Armazenamento de fotos | Upload de imagens com URLs públicas; integrado ao Firestore |

### Por que React Native + Expo?

A Motiva opera em múltiplas concessões com frota de dispositivos variada (Android predominante, mas com alguns iOS em níveis de supervisão). O React Native com Expo permite entregar um único app para ambas as plataformas, reduzindo custo de manutenção. O Expo ainda facilita atualizações OTA (over-the-air), críticas em contextos onde o operador não pode parar para atualizar o app manualmente.

---

##  Documento de Requisitos

Ver arquivo [`REQUISITOS.md`](./REQUISITOS.md)

---

##  Protótipo Navegável (Figma)

🔗 **[Acessar Protótipo no Figma](#)** ← *(substituir pelo link real após publicação)*

> O protótipo cobre os fluxos principais: Login → Dashboard do Operador → Nova Ocorrência (foto + classificação + GPS) → Confirmação → Histórico de Registros.

---



*Sprint 1 — Challenge CCR Motiva | FIAP 2025*
