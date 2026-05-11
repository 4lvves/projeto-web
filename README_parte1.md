# Parte 1 - Desenvolvimento Front-End

## Tarefa 1.1 - Proposta de Aplicação

A aplicação desenvolvida é uma plataforma de acompanhamento de treinos para corrida.
O sistema permite visualizar corredores cadastrados e os treinos associados a cada atleta.

O objetivo da aplicação é auxiliar treinadores e corredores amadores no acompanhamento
de rotinas de treino, intensidade e metas de corrida.

Os principais usuários da plataforma são:
- Corredores amadores
- Assessorias esportivas
- Treinadores de corrida

As duas entidades principais da aplicação são:
- Corredor
- Treino

---

# Tarefa 1.2 - Modelagem dos Dados Mockados

## Entidade: Corredor

### Estrutura JSON

```json
{
  "id": 1,
  "nome": "Mariana Costa",
  "idade": 29,
  "nivel": "Intermediário",
  "meta": "10km",
  "ativo": true
}
```

### Campos

- id: identificador único do corredor
- nome: nome completo do corredor
- idade: idade do corredor
- nivel: nível de experiência
- meta: objetivo principal de corrida
- ativo: status de atividade do corredor

---

## Entidade: Treino

### Estrutura JSON

```json
{
  "id": 1,
  "titulo": "Treino Intervalado",
  "distancia": 8,
  "intensidade": "Alta",
  "duracao": 50,
  "tipo": "Velocidade"
}
```

### Campos

- id: identificador do treino
- titulo: nome do treino
- distancia: distância em quilômetros
- intensidade: nível de intensidade do treino
- duracao: duração em minutos
- tipo: categoria do treino

---

# Registros Mockados

Os registros mockados foram implementados no arquivo:

frontend/src/data/mockData.js

Foram criados:
- 4 corredores
- 4 treinos

Todos os dados estão contextualizados ao domínio de corrida.

---

# Tarefa 1.3 - Implementação da Interface em React

## Componentes Criados

### RunnerCard

Responsável por exibir os dados individuais de um corredor.

Consome:
- nome
- idade
- nivel
- meta
- ativo

---

### WorkoutCard

Responsável por exibir informações de um treino.

Consome:
- titulo
- distancia
- intensidade
- duracao
- tipo

---

### WorkoutList

Renderiza a listagem dos treinos em formato de cards.

---

### WorkoutForm

Formulário para cadastro de treino.

O formulário possui:
- campo de texto
- campo select
- botão de submissão
- feedback visual após envio

---

## Gerenciamento de Estado

Foi utilizado o hook useState para:
- filtrar treinos por intensidade
- controlar os dados do formulário
- exibir mensagem de sucesso após submissão

---

## Biblioteca CSS Utilizada

Foi utilizado Tailwind CSS para estilização da interface.

A escolha foi feita devido:
- rapidez na prototipação
- simplicidade de integração com React
- facilidade para criar layouts responsivos
- redução da necessidade de arquivos CSS separados
