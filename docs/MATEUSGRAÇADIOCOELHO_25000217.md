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

---

# 6. Documentação dos Casos de Uso
Para **cada caso de uso**, utilize o template abaixo:
---

## **UCXX — Nome do Caso de Uso**
**Ator(es):**  
**Descrição:**  
**Pré-condições:**  
**Pós-condições:**  

### Fluxo Principal
1.  
2.  
3.  
4.  

### Fluxos Alternativos / Exceções
- FA01 —  
- FA02 —  

### Relacionamentos
- **Include:** (listar quando aplicável)  
- **Extend:** (listar quando aplicável)  

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

---

> Repita essa estrutura para **todos os seus casos de uso** (mínimo 10).


