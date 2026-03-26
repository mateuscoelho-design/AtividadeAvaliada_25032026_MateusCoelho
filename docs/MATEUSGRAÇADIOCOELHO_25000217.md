# Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante**

Aluno: *25000217*
RA: *25000217*
Data: *25/03/2026*

---

# 1. Definição do MVP
Descreva aqui **qual parte do sistema** foi incluída no seu MVP.  
Explique claramente: Meu MVP cobre o processo de venda da farmácia, desde a identificação ou cadastro do cliente até a finalização da venda e emissão do comprovante, incluindo a verificação de estoque.

*O que está **dentro** do MVP?*
- Cadastro e identificação de clientes
- Consulta de produtos
- Verificação de estoque
- Registro de venda
- Venda à vista e a prazo
- Atualização automática do estoque após a venda
- Emissão de comprovante
- Registro em contas a receber (no caso de venda a prazo)

*O que está **fora** do MVP*
- Cadastro e controle de fornecedores
- Processo de compras
- Contas a pagar
- Relatórios e indicadores
- Controle de usuários e permissões
- Transferência de estoque entre unidades

*Por que você fez essas escolhas*  
Escolhi focar na parte de vendas porque é a função principal da farmácia e a mais usada no dia a dia. Assim, o sistema já consegue funcionar de forma básica, atendendo clientes e registrando vendas. As outras partes ficaram de fora porque não são essenciais para o funcionamento inicial e deixariam o sistema mais complexo.

---

# 2. Regras de Negócio (mínimo: 5)
Liste e descreva **cada RN** de forma clara.

**RN01 —Venda só pode ser realizada se houver estoque disponível** 
- O sistema deve verificar se a quantidade do produto existe no estoque antes de permitir a venda.

**RN02 —Estoque deve ser atualizado automaticamente após a venda**
- Sempre que uma venda for concluída, a quantidade do produto no estoque deve ser reduzida automaticamente.

**RN03 —Cliente pode ser cadastrado no momento da venda**  
- Caso o cliente não esteja cadastrado, o atendente pode fazer um cadastro rápido durante o atendimento.

**RN04 —Vendas podem ser à vista ou a prazo**
- O sistema deve permitir os dois tipos de pagamento no momento da venda.

**RN05 —Vendas a prazo devem gerar conta a receber**
- Quando a venda for a prazo, o sistema deve criar automaticamente um registro em contas a receber.

**RN06 —Não é permitido vender produtos inexistentes**
- O sistema só deve permitir a venda de produtos que estejam cadastrados.

**RN07 —Toda venda deve gerar um comprovante**
- Após finalizar a venda, o sistema deve emitir um comprovante com os dados da compra.

---

# 3. Requisitos Funcionais (mínimo: 8)
Liste os requisitos funcionais do seu MVP.

**RF01 —Cadastrar cliente**
- O sistema deve permitir cadastrar novos clientes.

**RF02 —Identificar cliente**
- O sistema deve permitir buscar e identificar clientes já cadastrados.

**RF03 —Consultar produtos**
- O sistema deve permitir pesquisar produtos pelo nome, código ou fabricante.

**RF04 —Verificar estoque**
- O sistema deve mostrar a quantidade disponível de cada produto.

**RF05 —Registrar venda**
- O sistema deve permitir registrar uma venda com um ou mais produtos.

**RF06 —Selecionar forma de pagamento**
- O sistema deve permitir escolher entre pagamento à vista ou a prazo.

**RF07 —Atualizar estoque automaticamente**
- O sistema deve atualizar o estoque após a finalização da venda.

**RF08 —Gerar comprovante de venda**
- O sistema deve emitir um comprovante com os dados da venda.

**RF09 —Registrar conta a receber**
- O sistema deve gerar automaticamente uma conta a receber quando a venda for a prazo.

---

# 🛡 4. Requisitos Não Funcionais (mínimo: 4)
Liste os RNFs do sistema conforme seu MVP.

**RNF01 —Tempo de resposta rápido**
- O sistema deve responder às ações do usuário em poucos segundos, para não atrasar o atendimento.
  
**RNF02 —Facilidade de uso**
- O sistema deve ser simples e fácil de usar, já que será utilizado por atendentes no dia a dia.

**RNF03 —Disponibilidade do sistema**
- O sistema deve estar disponível durante o horário de funcionamento da farmácia.

**RNF04 —Segurança de dados**
- O sistema deve proteger as informações de clientes e vendas contra acessos não autorizados.

**RNF05 —Confiabilidade**
- O sistema deve registrar corretamente todas as vendas sem perder dados.

---

# 5. Casos de Uso (mínimo: 10)
### Inserir **diagrama de casos de uso geral**, demonstrando claramente:
- os 10 casos
- relação entre eles e atores
- pelo menos 3 includes
- pelo menos 3 extends

---

- UC01 — Identificar cliente
- UC02 — Cadastrar cliente
- UC03 — Consultar produto
- UC04 — Verificar estoque
- UC05 — Registrar venda
- UC06 — Adicionar item à venda
- UC07 — Finalizar venda
- UC08 — Emitir comprovante
- UC09 — Realizar venda a prazo
- UC10 — Registrar conta a receber

<img width="2116" height="585" alt="image" src="https://github.com/user-attachments/assets/e7ecea9a-fb5c-4007-a657-ea7328b67ae3" />

---

# 6. Documentação dos Casos de Uso
Para **cada caso de uso**, utilize o template abaixo:
---

## **UC01 — Identificar cliente**
**Ator(es): Atendente**  
**Descrição: Permite localizar um cliente já cadastrado.**  
**Pré-condições: Cliente pode ou não estar cadastrado.**  
**Pós-condições: Cliente identificado no sistema.**  

### Fluxo Principal
1.  Atendente informa o nome ou CPF do cliente
2.  Sistema busca o cliente
3.  Sistema exibe os dados do cliente
4.  Atendente confirma o cliente

### Fluxos Alternativos / Exceções
- FA01 — Cliente não encontrado → sugerir cadastro
- FA02 — Dados inválidos → solicitar novamente

### Relacionamentos
- **Include: —** 
- **Extend: Cadastrar cliente**

<img width="242" height="312" alt="image" src="https://github.com/user-attachments/assets/1fca04c4-fafe-4d57-a138-edf324736579" />

---

## **UC02 — Cadastrar cliente**
**Ator(es): Atendente**  
**Descrição: Permite cadastrar um novo cliente.**  
**Pré-condições: Cliente não cadastrado.**  
**Pós-condições: Cliente registrado no sistema.**  

### Fluxo Principal
1.  Atendente informa dados do cliente
2.  Sistema valida os dados
3.  Sistema salva o cliente
4.  Sistema confirma cadastro

### Fluxos Alternativos / Exceções
- FA01 — Dados inválidos → solicitar correção
- FA02 — Cliente já existe → cancelar cadastro

### Relacionamentos
- **Include: —** 
- **Extend: —**

<img width="236" height="312" alt="image" src="https://github.com/user-attachments/assets/1375c80b-036e-46cd-8717-939e7da517e8" />

---

## **UC03 — Consultar produto**
**Ator(es): Atendente**  
**Descrição: Permite buscar produtos.**  
**Pré-condições: Produto cadastrado.**  
**Pós-condições: Produto exibido.**  

### Fluxo Principal
1.  Atendente informa nome ou código
2.  Sistema busca produto
3.  Sistema exibe resultado
4.  Atendente seleciona produto

### Fluxos Alternativos / Exceções
- FA01 — Produto não encontrado
- FA02 — Erro na busca

### Relacionamentos
- **Include: —** 
- **Extend: —**

<img width="244" height="257" alt="image" src="https://github.com/user-attachments/assets/09cfaef8-8f92-4f08-a947-a9b5b1742b7a" />

---

## **UC04 — Verificar estoque**
**Ator(es): Atendente**  
**Descrição: Mostra a quantidade disponível do produto.**  
**Pré-condições: Produto selecionado.**  
**Pós-condições: Estoque exibido.**  

### Fluxo Principal
1.  Sistema consulta estoque
2.  Sistema mostra quantidade
3.  Atendente verifica
4.  Continua venda

### Fluxos Alternativos / Exceções
- FA01 — Produto sem estoque
- FA02 — Erro no sistema

### Relacionamentos
- **Include: —** 
- **Extend: —**

<img width="249" height="257" alt="image" src="https://github.com/user-attachments/assets/dbc19841-9433-43d0-94b8-69312d2ee46b" />

---

## **UC05 — Registrar venda**
**Ator(es): Atendente**  
**Descrição: Inicia o processo de venda.**  
**Pré-condições: Sistema ativo.**  
**Pós-condições: Venda criada.**  

### Fluxo Principal
1.  Atendente inicia venda
2.  Sistema abre venda
3.  Atendente adiciona itens
4.  Continua processo

### Fluxos Alternativos / Exceções
- FA01 — Erro ao iniciar
- FA02 — Cancelamento

### Relacionamentos
- **Include: Adicionar item, Finalizar venda** 
- **Extend: —**

<img width="132" height="248" alt="image" src="https://github.com/user-attachments/assets/3b5b605b-a98a-4712-b3b7-1e49880413fe" />

---

## **UC06 — Adicionar item à venda**
**Ator(es): Atendente**  
**Descrição: Adiciona produtos à venda.**  
**Pré-condições: Venda iniciada.**  
**Pós-condições: Item adicionado.**  

### Fluxo Principal
1.  Buscar produto
2.  Verificar estoque
3.  Informar quantidade
4.  Adicionar item

### Fluxos Alternativos / Exceções
- FA01 — Sem estoque
- FA02 — Produto inválido

### Relacionamentos
- **Include: Consultar produto, Verificar estoque** 
- **Extend: —**

<img width="191" height="312" alt="image" src="https://github.com/user-attachments/assets/489c50ef-cef3-4762-9846-014c9b54c132" />

---

## **UC07 — Finalizar venda**
**Ator(es): Atendente**  
**Descrição: Finaliza a venda.**  
**Pré-condições: Venda com itens.**  
**Pós-condições: Venda concluída.**  

### Fluxo Principal
1.  Confirmar venda
2.  Escolher pagamento
3.  Finalizar
4.  Atualizar estoque

### Fluxos Alternativos / Exceções
- FA01 — Cancelamento
- FA02 — Erro pagamento

### Relacionamentos
- **Include: Emitir comprovante** 
- **Extend: Venda a prazo**

<img width="167" height="248" alt="image" src="https://github.com/user-attachments/assets/bd52c271-3c28-478a-a41a-03763da2293c" />

---

## **UC08 — Emitir comprovante**
**Ator(es): Sistema**  
**Descrição: Gera comprovante da venda.**  
**Pré-condições: Venda finalizada.**  
**Pós-condições: Comprovante emitido.**  

### Fluxo Principal
1.  Gerar dados
2.  Criar comprovante
3.  Exibir ou imprimir
4.  Finalizar

### Fluxos Alternativos / Exceções
- FA01 — Erro na geração
- FA02 — Impressora falha

### Relacionamentos
- **Include: —** 
- **Extend: —**

<img width="147" height="193" alt="image" src="https://github.com/user-attachments/assets/71ba67d8-8dc8-4f96-915d-85b9f2d9832a" />

---

## **UC09 — Realizar venda a prazo**
**Ator(es): Atendente, Cliente**  
**Descrição: Permite vender a prazo.**  
**Pré-condições: Cliente identificado.**  
**Pós-condições: Venda registrada a prazo.**  

### Fluxo Principal
1.  Selecionar pagamento a prazo
2.  Definir vencimento
3.  Confirmar
4.  Finalizar venda

### Fluxos Alternativos / Exceções
- FA01 — Cliente não autorizado
- FA02 — Dados inválidos

### Relacionamentos
- **Include: Registrar conta a receber** 
- **Extend: Registrar venda**

<img width="144" height="248" alt="image" src="https://github.com/user-attachments/assets/f344ccb6-73f7-4085-b7d6-ccf853b9dcc6" />

---

## **UC10 — Registrar conta a receber**
**Ator(es): Sistema**  
**Descrição: Registra valor a receber.**  
**Pré-condições: Venda a prazo.**  
**Pós-condições: Conta registrada.**  

### Fluxo Principal
1.  Gerar registro
2.  Definir valor
3.  Definir vencimento
4.  Salvar

### Fluxos Alternativos / Exceções
- FA01 — Erro ao salvar
- FA02 — Dados inválidos

### Relacionamentos
- **Include: —** 
- **Extend: —**

<img width="126" height="193" alt="image" src="https://github.com/user-attachments/assets/7fe8fcfc-ca52-42af-813f-8ae5dd0b5206" />
