# README - Exercicios de Docker

Repositorio com exercicios praticos de Docker organizados por etapas de aprendizado, começando pelos primeiros containers, passando por um site em container e chegando a exemplos com banco de dados.

## Objetivo

Este projeto foi criado para reunir exercicios de Docker com foco em pratica. A proposta e aprender os conceitos de forma progressiva, criando imagens, executando containers, copiando arquivos e trabalhando com aplicacoes simples e banco de dados.

## Estrutura do projeto

```text
.
├── 01 - Primeiros containers
│   ├── 0.imagem python
│   │   └── Dockerfile
│   ├── 1.direto
│   │   └── Dockerfile
│   ├── 2.CMD
│   │   └── Dockerfile
│   └── 3.copy
│       ├── Dockerfile
│       └── ola.py
├── 02 - Site em um container
│   └── 1.html_puro
│       ├── Dockerfile
│       └── index.html
├── 03 - banco de dados
│   ├── 1.postgres_dockerfile_sem_senha
│   │   └── Dockerfile
│   └── 2.posgre_com_senha_dockerfile
├── estrutura.txt
└── README.md
```

## Organizacao dos exercicios

### 01 - Primeiros containers
Conjunto de exercicios introdutorios para entender a criacao de imagens Docker e o comportamento basico de containers.

- `0.imagem python`: exemplo inicial usando imagem base Python.
- `1.direto`: exercicio com instrucoes diretas no Dockerfile.
- `2.CMD`: pratica com o comando `CMD`.
- `3.copy`: exemplo de copia de arquivos para dentro do container com uso do arquivo `ola.py`.

### 02 - Site em um container
Exercicio voltado para empacotar uma pagina HTML simples em um container.

- `1.html_puro`: contem um `Dockerfile` e um `index.html` para testar a publicacao de um site estatico.

### 03 - Banco de dados
Exercicios com foco em banco de dados usando PostgreSQL em Docker.

- `1.postgres_dockerfile_sem_senha`: exemplo inicial de configuracao.
- `2.posgre_com_senha_dockerfile`: variacao com configuracao de senha.

## Como usar

Clone o repositorio:

```bash
git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_REPOSITORIO>
```

Acesse a pasta do exercicio desejado e execute o build da imagem:

```bash
docker build -t nome-da-imagem .
```

Depois, execute o container:

```bash
docker run --rm nome-da-imagem
```

Nos exercicios que envolvem site ou banco de dados, pode ser necessario mapear portas ou definir variaveis de ambiente.

Exemplo com porta:

```bash
docker run -p 8080:80 nome-da-imagem
```

Exemplo com variavel de ambiente:

```bash
docker run -e POSTGRES_PASSWORD=minhasenha nome-da-imagem
```

## O que e praticado aqui

- Criacao de imagens com `Dockerfile`
- Uso de imagem base
- Execucao de comandos no build
- Uso de `CMD`
- Copia de arquivos com `COPY`
- Containerizacao de pagina HTML simples
- Primeiros testes com banco de dados em container

## Requisitos

Para executar os exercicios, e recomendado ter instalado:

- Docker Desktop ou Docker Engine
- Git
- VS Code (opcional, mas util para editar e testar)

## Observacoes

Os exercicios estao organizados de forma simples para facilitar o estudo. A ideia e manter o repositorio como material de apoio, consulta rapida e base para novos testes com Docker.