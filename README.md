# 📖 README — DER e MER do Sistema de Gestão Agrícola.
## 📌 Sobre o Projeto
Este projeto tem como objetivo estruturar o banco de dados para um sistema de gestão agrícola, permitindo o controle de fazendas, talhões, cultivos, sensores de monitoramento, aplicações de insumos e suas respectivas leituras.

## 📊DER
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

## 📄 MER
O MER é a versão formalizada e estruturada do DER, normalmente escrito em um formato declarativo que descreve a estrutura lógica do banco de dados.

**SQL**
```sql
Table Fazenda {
  id_fazenda int [pk]
  nome varchar
  localizacao varchar
}

Table Talhao {
  id_talhao int [pk]
  id_fazenda int [ref: > Fazenda.id_fazenda]
  nome varchar
  area_ha decimal
}

Table Cultura {
  id_cultura int [pk]
  nome varchar
}

Table Plantio {
  id_plantio int [pk]
  id_fazenda int [ref: > Fazenda.id_fazenda]
  id_cultura int [ref: > Cultura.id_cultura]
  data_plantio date
  data_colheita date
}

Table Sensores {
  id_sensor int [pk]
  tipo varchar
  unidade_medida varchar
}

Table Leitura {
  id_leitura int [pk]
  id_sensor int [ref: > Sensores.id_sensor]
  id_plantio int [ref: > Plantio.id_plantio]
  data_hora datetime
  valor decimal
}

Table AplicacaoInsumo {
  id_aplicacao int [pk]
  id_plantio int [ref: > Plantio.id_plantio]
  data_hora datetime
}

Table Insumo {
  id_insumo int [pk]
  nome varchar
  tipo varchar
}

Table ItemAplicado {
  id_item int [pk]
  id_aplicacao int [ref: > AplicacaoInsumo.id_aplicacao]
  id_insumo int [ref: > Insumo.id_insumo]
  quantidade decimal
  unidade varchar
}

```

## 🎨 GITHUB
https://github.com/Raquerd/Cap1_-_Um_mapa_do_tesouro
