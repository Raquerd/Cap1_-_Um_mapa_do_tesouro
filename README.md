# 📖 README — DER e MER do Sistema de Gestão Agrícola.
## 📌 Sobre o Projeto
Este projeto tem como objetivo estruturar o banco de dados para um sistema de gestão agrícola, permitindo o controle de fazendas, talhões, cultivos, sensores de monitoramento, aplicações de insumos e suas respectivas leituras.

## 📊 O que é DER (Diagrama Entidade-Relacionamento)?
O DER é uma representação gráfica que descreve as tabelas do sistema e seus relacionamentos. Ele facilita a visualização da estrutura do banco de dados antes da implementação, permitindo identificar:
- Tabelas
- Campos
- Os relacionamentos entre tabelas

**Tabelas presentes em nosso DER:**
- Fazenda
- Talhão
- Cultura
- Plantio
- Sensor
- Leitura
- Aplicação de Insumo
- Insumo
- Item Aplicado

## 📄 O que é MER (Modelo Entidade-Relacional)?
O Modelo Entidade-Relacional (MER) é a versão formalizada e estruturada do DER, normalmente escrito em um formato declarativo que descreve a estrutura lógica do banco de dados.

No MER, são definidos:

As tabelas com suas chaves primárias (pk) e chaves estrangeiras (ref)

Os tipos de dados para cada campo

Os relacionamentos de integridade entre as tabelas

Exemplo de trecho do nosso MER:

**SQL**
```sql
Table Fazenda {
  id_fazenda int [pk]
  nome varchar
  localizacao varchar
}
```
## 📈 Resumo
Nosso sistema de gestão agrícola possui:

Fazendas, que possuem Talhões

Cultura, que define o tipo de plantio

Plantios, que ocorrem nas fazendas, com uma cultura específica e datas de início e colheita

Sensores, que realizam leituras vinculadas aos plantios

Insumos, aplicados nos plantios via aplicações

Itens aplicados, que detalham quais insumos e quantidades foram usados em cada aplicação

## 🎨 GITHUB
https://github.com/Raquerd/Cap1_-_Um_mapa_do_tesouro
