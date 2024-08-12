# Relatório de Estudos

**Nome do Estagiário:** Rafael Rodrigues  
**Data:** 12/08/2024

## Referências: 

[FastAPI docs](https://fastapi.tiangolo.com/tutorial/first-steps/)

[Como Criar API em Python Usando o FastAPI](https://youtu.be/R26iojTwUv8?si=Qu-FJ-9Iufh-dVXK)

**Módulos/Etapas Feitas:**  
1. **Tutorial - User Guide**
### Primeiro passos 

Aqui eu aprendi um pouco sobre A FastAPI que é um framework criado em python focando em ser rápida e eficiente. Ela cria uma documentação automática facilitando que outros desenvolvedores entendam o código, faz o gerenciamento de processos assíncronos.

Para iniciar minha API usando fastAPI, primeiro eu tenho que ter o python instalado no site [python.org](https://www.python.org/downloads/) 

Configurar as váriáveis de ambiente: 

clicar na area de trabalho com o direito do mouse -> propriedades -> propriedades avançadas -> variáveis de ambiente -> em user variáveis e system variáveis clicar em path e adicionar o caminho do arquivo que foi instalado o python no meu caso devo setar essas duas:
```C:\Users\rafa_\AppData\Local\Programs\Python\Python312\Scripts```

```C:\Users\rafa_\AppData\Local\Programs\Python\Python312```


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




2. **[Módulo/Etapa 2]**
3. **[Módulo/Etapa 3]** 
4. ...

## Resumo dos módulos 

12/08/24

Hoje eu iniciei meus estudos em FastAPI e entendi um pouco sobre o que ela é e seu funcionamento.
Aprendi também como configurar o python para usar seus principais comandos como pip install para instalar dependências python a partir do python package index (Pyp).

## Links de Laboratórios (se houver)

- [Google Colab 1/Notion 1](URL_do_Lab_1)
- [Google Colab 2/Notion 2](URL_do_Lab_2)
- ...

**Recursos Utilizados:**  
- [Recurso 1]
- [Recurso 2]
- [Recurso 3]
- ...

**Principais comandos: (se aplicável)**  
- [Comando 1]
- [Comando 2]
- [Comando 3]
- ...

**Desafios Encontrados:**  
Descreva quaisquer desafios ou obstáculos que você encontrou durante a trilha de aprendizagem e como você os superou ou planeja superá-los.

**Feedback e Ajustes:**  
Descreva qualquer feedback que você recebeu e como você ajustou sua abordagem de estudo com base nesse feedback.

**Próximos Passos:**  
Descreva os próximos passos em sua trilha de aprendizagem. Quais são as próximas etapas ou módulos que você irá abordar?
