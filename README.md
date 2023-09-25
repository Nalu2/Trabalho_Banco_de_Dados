# Trabalho_Banco_de_Dados

Neste trabalho, veremos algumas funções normalmente usadas na plataforma pgAdmin para criar e manipular bancos de dados. para isso foi proposta uma pequena atividade com 11 questoes sobre uma tabela com varias informações (pais,regiao,cidade,nome,telefone).

1. Selecione todos os dados dos países da tabela_paises

Na primeira questão usaremos apenas esta linha de codigo on selecionamos todos os itens presentes na coluna
```sql
select * from tabela_paises
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/cdfd2ec6-298e-4877-ac90-e16e27f67733)

2. Selecione todas as cidades cujo país seja brazil
Na segunda questão, teremos apenas a adição do "where" ultilizado para especificar ainda mais de onde você quer os dados.
```sql
select cidade from tabela_paises where pais = 'Brazil'
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/34f020e0-a912-42f8-a0c9-e133319e03e5)

3. Selecione todas as cidades cuja região(estado) é ceará;
na terceira questão, faremos a mesma coisa porem com "regiao"
```sql
select cidade from tabela_paises where regiao = 'Ceará'
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/5fd1907b-bfa2-41c8-99da-a640d2db2e2b)

4. Utilize a função count para saber quantas regiões(estados) existem na China,
utilize também o group by;

```sql
select regiao, count (regiao) from tabela_paises where pais = 'China'group by regiao
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/251c6162-0252-40b7-b69f-39a2cd71f61f)

5. Quais regiões, diferentes, existem no Canadá?

```sql
select regiao from tabela_paises where pais = 'Canada' group by regiao
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/6abe1970-b1b0-45ab-9c29-3c875a4f8d86)

6. Quantos países diferentes existem na tabela 'tabela_paises';
```sql
select distinct pais from tabela_paises order by pais;
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/829ae5b2-ea86-406f-a2a0-ac6ad6c01dc3)

7. Quantas cidades diferentes existem no brazil;

```sql
select pais, count(regiao) from tabela_paises group by pais
```
![image](https://github.com/Nalu2/Trabalho_Banco_de_Dados/assets/88158868/369abfbf-77bf-4700-ae7c-87ca616038b4)

















