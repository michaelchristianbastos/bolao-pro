# 🗄️ Banco de Dados - Bolão Pro

## Objetivo

Este documento descreve a estrutura inicial do banco de dados do Bolão Pro.

---

# Tabela: USUARIOS

Representa todas as pessoas cadastradas no sistema.

Campos:

- id
- nome
- telefone
- email
- cpf
- pix
- data_nascimento
- foto
- senha
- status
- data_cadastro
- ultimo_acesso

---

# Tabela: CAMPEONATOS

Representa os campeonatos disponíveis.

Campos:

- id
- nome
- temporada
- tipo
- data_inicio
- data_fim
- status

---

# Tabela: BOLOES

Representa cada bolão criado pelos administradores.

Campos:

- id
- nome
- campeonato_id
- temporada
- rodada_inicio
- rodada_fim
- tipo_classificacao
- valor_inscricao
- codigo_convite
- status
- data_criacao

---

# Tabela: PARTICIPANTES

Liga um usuário a um bolão.

Campos:

- id
- usuario_id
- bolao_id
- data_entrada
- status

---

# Tabela: RODADAS

Representa as rodadas oficiais do campeonato.

Campos:

- id
- campeonato_id
- numero
- data_inicio
- data_fim

---

# Tabela: JOGOS

Representa todas as partidas do campeonato.

Campos:

- id
- rodada_id
- mandante
- visitante
- data
- hora
- placar_mandante
- placar_visitante
- status
- processado

---

# Tabela: RODADAS_BOLAO

Representa as rodadas criadas dentro de cada bolão.

Campos:

- id
- bolao_id
- nome
- data_inicio
- data_fim
- status

---

# Tabela: RODADAS_BOLAO_JOGOS

Relaciona quais jogos pertencem a cada rodada do bolão.

Campos:

- id
- rodada_bolao_id
- jogo_id
