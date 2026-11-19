# Análise da Produção Ambulatorial do SUS – Ijuí/RS (3º Trimestre de 2026)

Projeto prático desenvolvido para a entrega T3, utilizando dados públicos do SIASUS (DATASUS) referentes aos atendimentos ambulatoriais realizados no município de Ijuí/RS (IBGE `431020`).

## Arquitetura e Arquivos do Projeto

* **`04-gera-dimtempo-mysql.sql`**: Criação e carga dinâmica da dimensão temporal (`DIMTEMPO`) no MySQL.
* **`view_pa_ijui.sql`**: Criação da view `pa_ijui` no schema `sus`, consolidando a tabela fato `pars` com as dimensões de estabelecimentos (`cadgerrs`), procedimentos (`tb_sigtaw`), ocupações (`cbo`), diagnósticos (`s_cid`) e municípios (`tb_municip`).
* **`analise_siasus_ijui.ipynb`**: Extração dos dados via Python (`mysql-connector-python`), tratamento e análise exploratória com `pandas`.

## Resumo dos Dados Consolidados
* **Município de Atendimento:** Ijuí - RS (`431020`)
* **Recorte Temporal:** Junho, Julho e Agosto de 2026
* **Volume Total:** 75.192 registros ambulatoriais