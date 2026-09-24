# Modelagem de Banco de Dados para Gestão de Informações da Ansarah
Projeto acadêmico de modelagem de Banco de Dados da empresa ANSARAH - UNICID

#Integrantes
- **Ana Beatriz Mendes Gonçalves**
- **Luiz Gustavo Santos de Oliveira**
- **Samantha Paula dos Santos Silva**

## 1. Introdução

Este trabalho apresenta a modelagem conceitual de um sistema de gestão de informações para a Ansarah, organização que atua no comércio de roupas de academia, roupas íntimas e produtos relacionados ao segmento de moda.
</br></br>
O trabalho tem como objetivo desenvolver um modelo conceitual de dados que represente as principais informações e processos da organização, contribuindo para uma melhor organização e gerenciamento dos dados utilizados em suas atividades. O levantamento de requisitos foi realizado por meio de pesquisa de campo, utilizando um questionário com perguntas direcionadas à organização. As informações foram obtidas por meio de entrevista com Alessandra, uma das proprietárias da Ansarah e responsável pela administração do setor financeiro, sendo utilizadas como base para a compreensão dos processos, informações, dificuldades e regras de funcionamento da organização.
</br></br>
O projeto tem como delimitação a modelagem conceitual das informações e dos processos levantados junto à organização, não abrangendo, nesta etapa, a implementação do banco de dados ou o desenvolvimento do sistema. O modelo será construído com base nos processos e nas necessidades identificadas durante o levantamento de requisitos.


---

## 2. Caracterização da Organização

**Nome e natureza da organização:** A Ansarah é uma empresa comercial, pertencente ao segmento de moda e vestuário. Sua história começou em 1932, na Rua 25 de Março, em São Paulo, inicialmente com a comercialização de meias. Ao longo dos anos, a empresa expandiu sua atuação para moda íntima, lingerie e outros tipos de vestuário, comercializando atualmente diversos produtos por meio de lojas físicas e loja virtual. 
</br></br>
**Contexto e porte:** A Ansarah é uma empresa com fins lucrativos, com uma operação consolidada no segmento de moda e vestuário. Possui entre 50 e 100 funcionários, loja física, loja virtual e centro de logística, realizando vendas no varejo e no atacado para todo o país.
</br></br>
**Problemas e necessidades identificados:** Os principais problemas identificados estão relacionados à inserção manual das informações no sistema, especialmente no cadastro de produtos, à dificuldade de criação de relatórios personalizados e à recuperação das informações após a perda ou restauração de um backup. Nesses casos, é necessário retornar a um backup anterior e realizar novamente, de forma manual, a inserção das informações que não estavam presentes na versão recuperada, o que pode gerar retrabalho e aumentar o risco de perda ou desatualização dos dados. Dessa forma, identifica-se a necessidade de otimizar a inserção e atualização das informações no sistema, facilitar a obtenção de informações para apoio à tomada de decisão e melhorar os mecanismos relacionados à recuperação dos dados. 
</br></br>
**Justificativa da escolha:** a Ansarah foi escolhida porque o grupo possui acesso à organização por meio de contato com seu responsável. Uma das integrantes do grupo possui vínculo familiar com uma funcionária da empresa, o que possibilitou o contato e a realização da pesquisa de campo. Além disso, a organização possui diversos processos de negócio adequados à aplicação dos conceitos de banco de dados.
</br></br>
**Evidências da organização:** Para comprovar a existência da organização e o acesso do grupo para a realização da pesquisa de campo, foram reunidas informações e registros relacionados à Ansarah. Como evidências, serão apresentados: 

---

## 3. Evidências da Pesquisa
<br>
Para comprovar a existência da organização e o acesso do grupo para a realização da pesquisa de campo, foram reunidas informações e registros relacionados à Ansarah.

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

> **https://cnpj.biz/61419610000119**

### 3.5 Comunicação com a organização

Os registros da comunicação com Alessandra (uma das proprietárias da organização e responsável pelo setor financeiro) incluindo **áudio, prints e questionário**, estão **anexados no repositório**.

---

## 4. Principais Processos de Negócio

Principais processos mapeados:

•	Cadastro e atualização de produtos; 
•	Cadastro e controle das variações de produtos por cor e tamanho; 
•	Controle de estoque e inventário; 
•	Cadastro de clientes; 
•	Cadastro e relacionamento com fornecedores e marcas; 
•	Registro de vendas no Ponto de Venda (PDV) e no site; 
•	Controle de preços e promoções; 
•	Processamento e acompanhamento de pedidos online; 
•	Trocas, devoluções, cancelamentos e estornos; 
•	Registro e acompanhamento de pedidos de reposição; 
•	Geração de relatórios; 
•	Controle de usuários e permissões de acesso.
<br><br>

### 4.1 DESCRIÇÃO DOS PRINCIPAIS PROCESSOS

Cadastro de produtos: os produtos são cadastrados manualmente no sistema de gestão empresarial utilizando informações fornecidas pelas fábricas, como código, descrição, referência, coleção, subcoleção, grupo, categoria, tipo, informações fiscais e demais características do produto.
<br><br>
Controle de estoque: as quantidades dos produtos são registradas e acompanhadas no sistema. A organização utiliza o sistema para verificar disponibilidade, identificar produtos com estoque baixo ou sem estoque e acompanhar produtos com baixo giro.
<br><br>
Cadastro de clientes: os dados dos clientes são cadastrados no sistema, incluindo informações de identificação e contato. No comércio eletrônico, essas informações devem receber tratamento adequado em relação à privacidade.
<br><br>
Registro de vendas: as vendas realizadas no Ponto de Venda e no site são registradas no sistema. Cada venda possui informações como data, canal, desconto, forma de pagamento, funcionário responsável e seus respectivos itens.
<br><br>
Processamento de pedidos online: os pedidos realizados pelo site passam por etapas de aprovação do pagamento, separação, conferência/bipagem, faturamento, envio, rastreamento e entrega. Também podem ocorrer cancelamentos e reembolsos.
<br><br>
Controle de preços: a organização utiliza diferentes preços conforme o canal de venda e o tipo de cliente. Alterações de preços e descontos dependem de autorização da diretoria.
<br><br>
Trocas e devoluções: as solicitações são registradas e o produto devolvido passa por conferência antes da conclusão da operação. Quando necessário, é realizado o estorno.
<br><br>
Reposição de produtos: são registrados pedidos de reposição junto aos fornecedores, contendo os produtos/variações solicitados, suas quantidades, preços e informações relacionadas à entrega.

<br><br>

---

## 5. Requisitos do Sistema
Os requisitos do sistema foram organizados em *Requisitos Funcionais (RF)* e *Requisitos Não Funcionais (RNF) *. Os Requisitos Funcionais representam as funcionalidades e operações que o sistema deve realizar, enquanto os Requisitos Não Funcionais representam características, restrições e condições relacionadas ao funcionamento do sistema, como segurança, desempenho, disponibilidade e recuperação dos dados.


*Requisitos Funcionais*

 






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



---

## 11. Uso de Inteligência Artificial





---

## 12. Conclusão



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

