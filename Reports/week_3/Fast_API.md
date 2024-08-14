
# Relatório de Estudos

**Nome do Estagiário:** Rafael Rodrigues  
**Data:** 12/08/2024

<div style="text-align: justify">

## Referências: 

[FastAPI docs](https://fastapi.tiangolo.com/tutorial/first-steps/)

[Como Criar API em Python Usando o FastAPI](https://youtu.be/R26iojTwUv8?si=Qu-FJ-9Iufh-dVXK)

[Criando API com FastAPI (PARTE 1)](https://www.youtube.com/watch?v=2MmmjUv_tRc)

[Criando API com FastAPI (PARTE 2)](https://www.youtube.com/watch?v=bGW0v8HHDow)

**Módulos/Etapas Feitas:**  
1. **Tutorial - User Guide**
## Primeiro passos 

Aqui eu aprendi um pouco sobre A FastAPI que é um framework criado em Python focando em ser rápida e eficiente. Ela cria uma documentação automática facilitando que outros desenvolvedores entendam o código, faz o gerenciamento de processos assíncronos.

Para iniciar minha API usando fastAPI, primeiro eu tenho que ter o python instalado no site [python.org](https://www.python.org/downloads/) 

Configurar as váriáveis de ambiente: 

clicar na area de trabalho com o direito do mouse -> propriedades -> propriedades avançadas -> variáveis de ambiente -> em user variáveis e system variáveis clicar em path e adicionar o caminho do arquivo que foi instalado o python no meu caso devo setar essas duas:
```C:\Users\rafa_\AppData\Local\Programs\Python\Python312\Scripts```

```C:\Users\rafa_\AppData\Local\Programs\Python\Python312```

Quando o comando ```pip install "fastapi[standard]" é utilizado para iniciar a fastAPI ele vem com alguma dependências padrão opicionais.

posso passar somente ```pip install fastapi```


Importando FastAPI:

```from fastapi import FastAPI```

app = FastAPI()


@app.get("/")
async def root():
    return {"message": "Hello World"}

cria uma instância da FastAPI:

from fastapi import FastAPI

```app = FastAPI()```

@app.get("/")
async def root():
    return {"message": "Hello World"}

Cria um **Path** que é o caminho para a página também chamado de endpoint ou rota.

**Operação**
- POST: para criar dados.
- GET: para ler dados.
- PUT: para atualizar dados.
- DELETE: para deletar dados.

Com o Protocolo HTTP eu posso me comunicar com cada caminho(path) usando um ou mais desses méthodos.

O comando ```fastapi dev main.py``` inicia minha api por conta da dependência instalada com o comando ```pip install "fastapi[standard]"``` do pacote **fastapi-cli** mas em modo de desenvolvimento. Não é obrigatório instalar essa dependência.

Mais usado é o Uvicorn com o comando:

```
uvicorn nome_do_arquivo:app --reload
```

- Quando digito o endereço onde fica minha api passando o /docs no final ela mostra uma documentação detalhada sobre o método onde podemos fazer testes.
também tem o /redocs que é uma alternativa para o /docs

### Esquema OpenAPI e JSON

OpenAPI define um esquema de API para minha API, incluindo definições dos dados enviados e recebidos por minha API usando o JSON Schema, que é o padrão para esquemas de dados JSON.

Exemplo de um esquema API em JSON SChema:

 http://127.0.0.1:8000/openapi.json

{"openapi":"3.1.0","info":{"title":"FastAPI","version":"0.1.0"},"paths":{"/":{"get":{"summary":"Root","operationId":"root__get","responses":{"200":{"description":"Successful Response","content":{"application/json":{"schema":{}}}}}}}}}

## comandos para criar e iniciar uma api 

- Deve ser criado um ambiente virtual para instalar dependências do próprio projeto 
``` 
python -m venv venv
```

- usa se o ```venv/Scripts/activate``` para rodar no linux.

- para ver as dependências instaladas podemos usar o comando ``` pip freeze ``` ou ```pip freeze >> requirements.txt```

se ele criar o arquivo ele pode ser deletado com o comando ```rmdir requirements.txt``` 
Ele vai instalar as dependências que estão no arquivo requirements.txt.

Posso usar esse arquivo requirements.txt para instalar dependências em outro terminal por exemplo eu abro o terminal novo, apago a pasta venv e digito ``` python -m venv venv ``` e depois digito: ```pip install -r requirements.txt```

## Resumo dos módulos 

12/08/24

Hoje eu iniciei meus estudos em FastAPI e entendi um pouco sobre o que ela é e seu funcionamento.
Aprendi também como configurar o python para usar seus principais comandos como pip install para instalar dependências python a partir do python package index (Pyp).

13/08/24

Hoje eu estudei um pouco mais sobre a documentação da api reforçando algumas coisas que eu já tinha visto como comandos para iniciar uma api, seus métodos, etc.
O comando ```pip install "fastapi[standard]"``` traz pacotes padrões um deles me permite rodar o comando ```fastapi dev nome-arquivo.py ``` que roda a api em ambiente de teste, não precisando do Uvicorn ser instalado.
comando ```python -m venv venv ``` cria um ambiente virtual onde posso instalar dependências somente para o projeto especifico, para entrar no ambiente **ENV** eu digito ```venv/Scripts/requirements``` e para ver as dependências instaladas uso o comando ```pip freeze``` ou o comando ```pip freeze >> requirements.txt``` para criar um arquivo com as dependências instaladas. 

14/08/24

Hoje estou finalizando meu relatório dessa semana aprendi como criar uma API com os métodos Get e Post na prática, vi um pouco das duas rotar e fiz o código junto com a video da aula.

## Links de Laboratórios (se houver)

- [Google Colab 1/Notion 1](URL_do_Lab_1)
- [Google Colab 2/Notion 2](URL_do_Lab_2)
- ...

**Recursos Utilizados:**  
- VS Code
- Terminal
- [Recurso 3]
- ...

**Principais comandos: (se aplicável)**  
- pip install fastapi
- fastapi dev main.py
- uvicorn nome_do_arquivo:app --reload
- python -m venv venv
- venv/Scripts/activate
- pip freeze ou pip freeze >> requirements.txt
- rmdir requirements.txt
- pip install -r requirements.txt
- ...

**Desafios Encontrados:**  
Hoje dia 14/08/24 eu tive um problema pois eu instalei as dependências da fastapi de forma global mas não é o recomendado e sim instalar em um ambiente virtual, para corrigir eu busquei os pacotes instalados e apaguei eles com o comando ```pip uninstall anyio httpcore httptools sniffio watchfiles websockets```


**Feedback e Ajustes:**  
Não tenho feedback a fazer.

**Próximos Passos:**  
Vou continuar meus estudos em fastapi.

</div>