# 💡 reportLinuxUsersPython
Este projeto é parte do curso "Introduction to Python Development" da plataforma "A Cloud Guru". A finalidade é criar um CLI "hr" que nos permite realizar um relatório dos usuários do sistema linux com UID maiores que 1000 (usuário comuns). Com a opção de visualizar apenas o retorno (stdout) ou exportar para um arquivo, podendo ser em formato JSON ou CSV.

---
## hr
CLI que retorna usuários do SO linux e exportar em json ou csv.

---
## Uso
Ajuda do comando
```
$ hr --help
usage: hr [-h] [--path PATH] [--format {json,csv}]

options:
  -h, --help           show this help message and exit
  --path PATH          the path to the export file
  --format {json,csv}
```

Apenas retorna usuários:
```
$ hr 
[
    {
        "name": "davi",
        "id": 1000,
        "home": "/home/davi",
        "shell": "/usr/bin/zsh"
    },
    {
        "name": "carmo",
        "id": 1001,
        "home": "/home/carmo",
        "shell": "/usr/bin/zsh"
    }
]
```

Exporta resultado para JSON, pode ser CSV também:
```
$ hr --format=json --path=users.json
```

---
## Pré-requisitos
- Python
- SO linux

---
## Instalar da fonte

Para instalar o package depois de clonar o repositório:
```
$ pip install --user -e .
```

---
## Preparar para Desenvolvimento

Siga estes passos:

1. Garanta `pip` e `pipenv` estão instalados
2. Clone o repositório: `git clone git@github.com:davigdc/reportLinuxUsersPython`
3. `cd` para o diretório
4. Ative o virtualenv: `pipenv shell`
5. Instale as dependências: `pipenv install`

---