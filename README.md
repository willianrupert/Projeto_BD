# ecommerce-db-grupo-5 (2026.1)

**Projeto acadêmico de Banco de Dados com foco em modelagem relacional, SQL e PL/SQL para um cenário de e-commerce.**

**Disciplina:** Banco de Dados - UFPE CIn  
**Turma:** 2026.1  
**Equipe:** Amanda Trinity, Maria Eduarda, Maria Luísa, Matheus Braglia, Mirella Laura, Willian Neves

---

## Visão Geral

Este repositório reúne o banco relacional de um sistema de e-commerce, com scripts de criação, povoamento, consultas analíticas e relatórios finais. O projeto foi construído para demonstrar domínio prático de SQL, integridade referencial, normalização e consultas orientadas a negócio — exatamente o tipo de base útil para quem quer mostrar maturidade técnica em uma vaga que pede SQL.

---

## O Que Este Projeto Demonstra

- Modelagem relacional com tabelas, chaves primárias e estrangeiras bem definidas.
- Uso de `SEQUENCE` para geração automática de identificadores.
- Validações de domínio com `CHECK` e restrições consistentes.
- Normalização até a 3ª Forma Normal, reduzindo redundância e inconsistências.
- Relacionamentos associativos e históricos para preservar contexto de negócio.
- Consultas com `JOIN`, agregações, subconsultas, `GROUP BY`, `HAVING`, `UNION`, `INTERSECT`, `MINUS` e `VIEW`.
- Blocos PL/SQL com `FUNCTION`, `DECLARE`, `LOOP`, `WHILE`, `CASE`, `RECORD`, `TABLE` e tratamento de exceções.

---

## Destaques Técnicos

### Histórico temporal de cargos

O relacionamento entre Funcionário e Cargo foi modelado como histórico temporal em `HistoricoCargos`, permitindo registrar admissões, saídas e múltiplas ocupações do mesmo cargo ao longo do tempo sem perder rastreabilidade.

### Integridade e normalização

- **1FN:** endereços atomizados e telefones separados em tabelas próprias.
- **2FN:** tabelas associativas como `ItemPedido` e `Pertence` dependem totalmente de suas chaves compostas.
- **3FN:** atributos derivados foram evitados para reduzir redundância e anomalias de atualização.

### Consultas com valor de negócio

Os scripts incluem relatórios que respondem perguntas reais, como produtos mais vendidos, ticket médio por meio de pagamento, tempo médio de entrega, histórico de preços e uso de promoções.

---

## Estrutura do Repositório

```
ecommerce-db-grupo-5/
├── README.md
├── docs/
│   ├── AV1 GRUPO 5.pdf
│   ├── AV2-Grupo-5.pdf
│   └── walkthrough_oracle_livesql.md
└── sql/
    ├── 01_criacao.sql
    ├── 02_povoamento.sql
    ├── 03_consultas_checklist.sql
    └── 04_relatorios_finais.sql
```

---

## Principais Arquivos

- [sql/01_criacao.sql](sql/01_criacao.sql): cria o schema, constraints e sequences.
- [sql/02_povoamento.sql](sql/02_povoamento.sql): insere os dados base para testes e consultas.
- [sql/03_consultas_checklist.sql](sql/03_consultas_checklist.sql): reúne consultas SQL e blocos PL/SQL cobrindo o checklist da disciplina.
- [sql/04_relatorios_finais.sql](sql/04_relatorios_finais.sql): consolida respostas de negócio e relatórios gerenciais.
- [docs/walkthrough_oracle_livesql.md](docs/walkthrough_oracle_livesql.md): guia rápido para executar tudo no Oracle Live SQL.

---

## Como Executar

Execute os scripts nesta ordem para garantir a criação correta das tabelas e referências:

1. Execute `01_criacao.sql` para preparar o esquema.
2. Execute `02_povoamento.sql` para carregar os dados.
3. Execute `03_consultas_checklist.sql` para validar os requisitos técnicos.
4. Execute `04_relatorios_finais.sql` para explorar os relatórios finais.

Se quiser seguir passo a passo no Oracle Live SQL, veja o guia em [docs/walkthrough_oracle_livesql.md](docs/walkthrough_oracle_livesql.md).

---

## Checklist de Capacidades

- [x] DDL com tabelas, chaves e constraints.
- [x] DML com dados consistentes para testes.
- [x] `PRIMARY KEY` e `FOREIGN KEY` implementadas.
- [x] `SEQUENCE` para geração de identificadores.
- [x] `CHECK` para validação de domínio.
- [x] Consultas com `SELECT`, `JOIN`, `GROUP BY` e `HAVING`.
- [x] Blocos PL/SQL com estruturas de controle, coleções e funções.
- [x] Organização clara para execução em Oracle Live SQL.

---