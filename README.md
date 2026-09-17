# Modelagem de Banco de Dados para Gestão de Informações da Ansarah
Projeto acadêmico de modelagem de Banco de Dados da empresa ANSARAH - UNICID

#Integrantes
-Ana Beatriz
-Luiz Gustavo Santos de Oliveira
-Samantha Paula dos Santos Silva

## 1. Introdução

Este trabalho apresenta a modelagem conceitual de um banco de dados para a Ansarah, empresa do segmento de moda e vestuário. O objetivo é representar as principais informações e processos da organização, organizando os dados de forma estruturada para apoiar uma futura implementação de banco de dados.

Os requisitos foram levantados por meio de pesquisa de campo, questionário e entrevista com Alessandra, uma das proprietárias e responsável pela administração financeira da organização.

O escopo deste trabalho contempla a modelagem conceitual, não abrangendo, nesta etapa, a implementação do banco de dados ou o desenvolvimento do sistema.

---

## 2. Caracterização da Organização

A Ansarah atua no comércio do segmento de moda e vestuário. Sua história teve início em 1932, na Rua 25 de Março, em São Paulo, inicialmente com a venda de meias. Ao longo do tempo, a empresa ampliou sua atuação para lingerie e outros tipos de vestuário.

Atualmente, a organização possui lojas físicas e loja virtual, além de centro logístico, atuando no varejo e no atacado em âmbito nacional. A organização possui aproximadamente 50 a 100 funcionários.

Entre os problemas identificados estão:

- Inserção manual de dados, principalmente no cadastro de produtos;
- Dificuldade para gerar relatórios personalizados;
- Problemas relacionados à recuperação de dados após restauração de backup;
- Necessidade de reinserção manual de informações que não estejam presentes na versão recuperada;
- Risco de retrabalho e perda ou desatualização de informações.

---

## 3. Evidências da Pesquisa

As evidências da pesquisa de campo estão **anexadas no repositório**, incluindo fotografias das lojas, registros de comunicação e respostas do questionário.

### 3.1 Fotos das lojas

- **Loja da 25 de Março:** foto anexada no repositório.
- **Loja do Brás:** foto anexada no repositório.

### 3.2 Localização das lojas

**Loja da 25 de Março:**  
https://maps.app.goo.gl/ja89dX2NqaD3WHnK6

**Loja do Brás:**  
https://maps.app.goo.gl/SKGrzBL6uDV7w4WL8

### 3.3 Site oficial

https://www.ansarah.com.br/

### 3.4 Consulta de CNPJ

> **Adicionar aqui o link completo utilizado pela equipe para a consulta do CNPJ da organização.**

### 3.5 Comunicação com a organização

Os registros da comunicação com Alessandra, incluindo **áudio, prints e questionário**, estão **anexados no repositório**.

---

## 4. Principais Processos de Negócio

Os principais processos identificados na organização foram:

- Cadastro e atualização de produtos;
- Controle de estoque e inventário;
- Cadastro e gerenciamento de clientes;
- Cadastro e gerenciamento de fornecedores e marcas;
- Registro de vendas no PDV e no site;
- Controle de preços e promoções;
- Registro e acompanhamento de pedidos online;
- Trocas, devoluções, cancelamentos e estornos;
- Geração de relatórios;
- Controle de usuários e permissões.

---

## 5. Requisitos Funcionais

| Código   | Requisito |
|----------|-----------|
| **RF01** | Cadastrar e atualizar produtos. |
| **RF02** | Cadastrar marcas e fornecedores. |
| **RF03** | Relacionar produtos a marcas e fornecedores. |
| **RF04** | Cadastrar clientes. |
| **RF05** | Consultar histórico de compras do cliente. |
| **RF06** | Registrar vendas e itens. |
| **RF07** | Registrar quantidade, preço, desconto, forma de pagamento, data e vendedor. |
| **RF08** | Controlar estoque e inventários. |
| **RF09** | Controlar variações de produtos conforme cadastro da organização. |
| **RF10** | Cadastrar e aplicar tabelas de preços. |
| **RF11** | Registrar pedidos online. |
| **RF12** | Acompanhar o status das etapas dos pedidos online. |
| **RF13** | Registrar trocas, devoluções e cancelamentos. |
| **RF14** | Registrar motivos e estornos. |
| **RF15** | Registrar pedidos de compra. |
| **RF16** | Gerar relatórios de faturamento, estoque, produtos, marcas e comparativos de vendas. |
| **RF17** | Controlar usuários e permissões. |
| **RF18** | Realizar e recuperar backups. |

---

## 6. Requisitos Não Funcionais

| Código | Requisito |
|---|---|
| **RNF01** | **Segurança:** proteger as informações contra acessos não autorizados. |
| **RNF02** | **Privacidade:** atender à LGPD. |
| **RNF03** | **Controle de acesso:** cada funcionário deve acessar somente as informações necessárias à sua função/departamento. |
| **RNF04** | **Backup:** realizar backups periódicos. |
| **RNF05** | **Recuperação de dados:** permitir restauração a partir de backups em casos de perda ou inconsistência. |
| **RNF06** | **Integridade:** reduzir duplicidades e informações inconsistentes ou desatualizadas. |
| **RNF07** | **Usabilidade:** facilitar a inserção e atualização de informações, especialmente de produtos. |
| **RNF08** | **Compatibilidade:** permitir acesso nos computadores e notebooks utilizados pela organização. |
| **RNF09** | **Desempenho:** manter consultas e relatórios adequados à rotina. |

---

## 7. Regras de Negócio

| Código | Regra |
|---|---|
| **RN01** | O cadastro de produtos no ERP utiliza informações fornecidas pelas fábricas. |
| **RN02** | Os produtos possuem referência, coleção, categoria, marca, cor e tamanho. |
| **RN03** | O estoque é controlado pelo ERP, integrado à loja física e ao e-commerce. |
| **RN04** | As vendas são registradas no sistema. |
| **RN05** | Os pedidos online possuem etapas como pagamento, separação, conferência, faturamento, envio, rastreamento, entrega, cancelamento e reembolso. |
| **RN06** | Trocas e devoluções exigem a conferência do produto antes da conclusão. |
| **RN07** | As informações dos clientes online devem ser protegidas conforme as regras de privacidade aplicáveis. |
| **RN08** | Os prazos de troca seguem o Código de Defesa do Consumidor. |
| **RN09** | Clientes B2C e B2B podem possuir diferentes prazos de pagamento, descontos e condições. |
| **RN10** | Alterações de preços e descontos dependem da aprovação da diretoria. |
| **RN11** | O acesso ao sistema segue as permissões definidas para cada departamento. |
| **RN12** | O tratamento dos dados pessoais dos clientes observa a LGPD. |

---

## 8. Modelo Entidade-Relacionamento

O modelo conceitual foi desenvolvido com base nos requisitos funcionais, requisitos não funcionais e regras de negócio levantados durante a pesquisa.

### 8.1 Entidades

As entidades identificadas no modelo são:

- Cliente
- Funcionário
- Departamento
- Produto
- Marca
- Fornecedor
- Cor
- Tamanho
- Estoque
- Venda
- Item_Venda
- Pedido_Online
- Item_Pedido
- Tabela_Preco
- Historico_Preco
- Troca_Devolucao
- Produto_SKU
- Pedido_Compra
- Item_Pedido_Compra

### 8.2 Relacionamentos principais

- Cliente realiza vendas e pedidos online;
- Funcionário pertence a departamento e registra vendas;
- Produto pertence a marca, possui variações e possui estoque;
- Venda possui itens;
- Produto compõe itens de venda;
- Pedido_Online pertence a cliente e possui itens;
- Produto compõe itens de pedido;
- Produto possui histórico de preços;
- Tabela_Preco possui registros;
- Pedido_Online pode possuir troca, devolução ou cancelamento;
- Produto_SKU possui estoque;
- Produto_SKU compõe itens de venda, pedidos e compras;
- Pedido_Compra possui itens;
- Fornecedor possui pedidos de compra.

### 8.3 DER

O **Diagrama Entidade-Relacionamento (DER)** está **anexado no repositório**.

> **Imagem do DER: anexada no repositório.**

---

## 9. Dicionário de Dados

O **Dicionário de Dados** está **anexado no repositório**.

Ele apresenta as entidades, atributos, chaves primárias (PK), chaves estrangeiras (FK) e demais informações definidas para o modelo.

> **Arquivo/Documento do Dicionário de Dados: anexado no repositório.**

---

## 10. Justificativa Técnica do Modelo

O modelo conceitual organiza as informações da organização, reduzindo a concentração e a duplicação de dados e preparando uma futura implementação do modelo relacional.

A entidade **Produto** é central no modelo. A entidade **Produto_SKU** representa as variações dos produtos, evitando a duplicação das informações gerais do produto. As entidades **Cor** e **Tamanho** são separadas para permitir reutilização.

A entidade **Estoque** está relacionada ao SKU. As entidades **Venda** e **Item_Venda** representam as vendas e seus itens, enquanto **Pedido_Online** e **Item_Pedido** representam os pedidos realizados pela loja virtual.

As entidades **Tabela_Preco** e **Historico_Preco** permitem representar o controle de preços.

As entidades **Fornecedor**, **Pedido_Compra** e **Item_Pedido_Compra** representam o processo de compras.

A entidade **Troca_Devolucao** registra ocorrências relacionadas a trocas, devoluções e cancelamentos.

As entidades **Funcionário** e **Departamento** representam a organização interna, enquanto **Cliente** está relacionado às vendas e aos pedidos.

O atributo `valor_total` da entidade **Venda** não foi incluído por ser calculável a partir da quantidade, preço unitário e desconto dos itens.

As chaves primárias identificam unicamente os registros e as chaves estrangeiras estabelecem os relacionamentos entre as entidades, servindo como base para uma futura implementação do banco de dados relacional.

---

## 11. Uso de Inteligência Artificial

### 11.1 Ferramenta utilizada

**ChatGPT**

### 11.2 Aplicação da IA

A inteligência artificial foi utilizada como apoio na elaboração do questionário e na organização e estruturação do conteúdo do trabalho.

### 11.3 Prompts utilizados

**Prompt 1:**

> Orientação para entrevistar uma pequena loja de roupas e elaborar perguntas sobre processos, dados, estoque, vendas, clientes, fornecedores, funcionários, relatórios, segurança e dificuldades do sistema.

**Prompt 2:**

> Orientação para organizar o conteúdo conforme a rota do professor, contemplando Introdução, Caracterização da Organização, Processos de Negócio, Requisitos Funcionais, Requisitos Não Funcionais, Regras de Negócio e Dicionário de Dados.

### 11.4 Participação da IA no trabalho

A IA auxiliou na elaboração das perguntas e na organização das informações, além de sugerir possíveis entidades, atributos e relacionamentos.

As sugestões foram analisadas pela equipe e algumas foram rejeitadas ou corrigidas quando não correspondiam à realidade da organização ou não haviam sido confirmadas pela pesquisa.

As informações sobre a empresa foram definidas a partir da entrevista com a representante da Ansarah, pesquisa de campo e fontes públicas utilizadas pela equipe.

A IA foi utilizada como **ferramenta de apoio**, e não como fonte definitiva das informações da empresa.

A versão final foi definida pelo grupo com base nos dados levantados e nas orientações da disciplina.

---

## 12. Conclusão

A pesquisa de campo permitiu identificar os principais processos relacionados a produtos e suas variações, estoque, clientes, funcionários e departamentos, vendas, fornecedores e marcas, preços, pedidos online, pedidos de compra, trocas e devoluções, relatórios e controle de acesso.

Entre as principais dificuldades identificadas estão a inserção manual de informações, especialmente no cadastro de produtos, a geração de relatórios personalizados e a correção ou recuperação de dados.

O modelo conceitual proposto organiza essas informações e representa os principais relacionamentos identificados.

O modelo ainda poderá ser validado e refinado pela equipe antes da elaboração do modelo lógico, da implementação em SQL e da criação das consultas.

---

## 13. Referências

- **ANSARAH.** Informações institucionais e comerciais.  
  https://www.ansarah.com.br/

- **ANSARAH.** Entrevista e questionário com representante da organização. 2026.

- **Google Maps.** Localização das lojas da Ansarah.  
  25 de Março: https://maps.app.goo.gl/ja89dX2NqaD3WHnK6  
  Brás: https://maps.app.goo.gl/SKGrzBL6uDV7w4WL8

- **CNPJ.BIZ.** Consulta de registro da organização.  
  > **(https://cnpj.biz/61419610000119)**

---

