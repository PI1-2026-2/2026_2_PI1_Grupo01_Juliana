# Política de Contribuição — PI1 Grupo 01

Este documento define regras simples para que todo o grupo consiga trabalhar no projeto de forma organizada, mesmo quem nunca utilizou Git ou GitHub.

## 1. Regra principal

**Ninguém deve trabalhar diretamente na branch `main`.**

Cada integrante deve criar uma branch para sua tarefa, fazer os commits nela e depois abrir um Pull Request (PR) para `main`.

Fluxo básico:

```text
main → criar branch → fazer alterações → commit → push → Pull Request → revisão → merge
```

## 2. Nome das branches

O nome deve indicar de forma simples o que será feito.

Formato recomendado:

```text
feature/nome-da-tarefa
fix/nome-do-problema
docs/nome-da-documentacao
```

Exemplos:

```text
feature/sensor-linha
feature/tela-inicial
fix/leitura-sensor
fix/erro-motor
/docs/readme
```

Evite nomes genéricos como `teste`, `coisa`, `mudancas` ou `branch-luiza`.

## 3. Commits

Um commit deve representar **uma alteração lógica**. Evite colocar várias tarefas diferentes no mesmo commit.

### Formato recomendado

```text
tipo: descrição curta da alteração
```

Tipos mais comuns:

- `feat:` — nova funcionalidade
- `fix:` — correção de erro
- `docs:` — documentação
- `refactor:` — reorganização do código sem mudar o comportamento
- `test:` — criação ou alteração de testes
- `chore:` — configuração, organização ou manutenção

### Exemplos

```text
feat: adiciona leitura do sensor esquerdo
fix: corrige controle do motor direito
docs: atualiza instruções de montagem
test: adiciona teste dos sensores
chore: organiza arquivos do firmware
```

### Boas práticas

- Escreva o commit de forma curta e clara.
- Use verbo no presente: `adiciona`, `corrige`, `cria`, `atualiza`.
- Não use mensagens como `alterações`, `coisas`, `teste`, `final` ou `agora vai`.
- Não faça um commit gigante com todas as alterações do projeto.
- Não é necessário fazer um commit a cada linha alterada; faça quando concluir uma pequena unidade de trabalho.

## 4. Pull Requests

Quando terminar uma tarefa:

1. Envie sua branch para o GitHub.
2. Abra um Pull Request para `main`.
3. Explique brevemente o que foi feito.
4. Se possível, peça para pelo menos uma pessoa do grupo revisar.
5. Só faça o merge depois da revisão.

Exemplo de descrição de PR:

```text
## O que foi feito?
- Adicionada leitura dos sensores de linha.
- Criado tratamento para perda da linha.

## Testes
- Testado com o sensor sobre a pista.
- Testado com perda temporária da linha.
```

## 5. Antes de começar uma tarefa

Antes de criar uma branch, atualize sua cópia da `main` para evitar trabalhar sobre uma versão antiga do projeto.

```bash
git switch main
git pull origin main
```

Depois crie sua branch:

```bash
git switch -c feature/minha-tarefa
```

## 6. Enviando seu trabalho

Depois de fazer as alterações:

```bash
git add .
git commit -m "feat: minha alteração"
git push -u origin feature/minha-tarefa
```

Depois, abra o Pull Request no GitHub.

## 7. Regra para quem está aprendendo Git

**Não tenha medo de perguntar.** Git pode parecer complicado no começo.

Se aparecer um erro ou você não souber qual comando utilizar, pare e peça ajuda antes de executar comandos que possam apagar ou sobrescrever trabalho de outras pessoas.

Comandos como `git reset --hard`, `git push --force` e exclusões de branches não devem ser utilizados sem orientação de alguém do grupo que saiba exatamente o que está fazendo.

## 8. Revisão e colaboração

O projeto é coletivo. Portanto:

- Não altere o trabalho de outra pessoa sem conversar com ela.
- Revise PRs com respeito e foco no projeto.
- Comentários devem explicar o problema e, quando possível, sugerir uma solução.
- Se houver conflito entre alterações, conversem antes de resolver.
- O objetivo da revisão é melhorar o projeto, não avaliar a pessoa.

## 9. Regra de ouro

> **Branch para trabalhar, commit para registrar, Pull Request para revisar e `main` para manter o projeto funcionando.**

Em caso de dúvida, peça ajuda. É melhor perguntar do que perder o trabalho de alguém.
