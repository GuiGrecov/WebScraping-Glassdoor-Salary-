# WebScraping-Glassdoor-Salary

![image](https://user-images.githubusercontent.com/94385953/150644222-0aedc7c1-9855-45d4-941d-1199be58ad2b.png)

**AVISO:** O CEO citado em problema de negócio não existe. Esse webscraping foi feito apenas para demonstrar uma possibilidade de Webscraping em People Analytics!

# 1. Sobre o Glassdoor

Glassdoor é um site americano no qual funcionários atuais e ex-funcionários avaliam empresas anonimamente. O Glassdoor também permite que os usuários enviem e visualizem salários anonimamente, bem como pesquisem e se candidatem a empregos em sua plataforma.

# 2. Problema de Negócio 

O CEO precisa saber quanto as empresas estão pagando para dois cargos: People Analytics e Data Science. O CEO já conta com uma pesquisa salarial feito por uma consultoria, porém gostaria de fazer esse bate nos valores. Para conseguir comparar a agressividade com as outras empresas. 


# 3. Questão de Negócios 
1 - Criar uma função em Python capaz de pegar qualquer URL e conseguir extrair: 
* Cargo 
* Função 
* Salário: alguns casos teremos mínimos e máximos, em outros casos vamos somente ter um valor. 
* Empresa


2 - Criar uma segunda função capaz de agrupar as outras páginas em um dataseet e depois juntar em um maior: 
![image](https://user-images.githubusercontent.com/94385953/150644564-bad5cb8f-ecd9-4dbb-b340-0de49e7e690a.png)
Na imagem acima vemos que na maioria dos casos, vamos ter mais de uma página para conseguir fazer o scraping. Com isso vale criar uma segunda função que agrupe todos os dados em somente um arquivo. 



# 4. Limitações 

Como esse código participa de uma extração de dados que foram inseridos anonimamente, pode haver alguns erros nos valores de alguns salários. **RECOMENDAÇÕES:** Caso queira retirar alguns insight dos dados, vale retirar os outliers. Por se tratar de dados anônimos e queremos um "norte" de valor em salários para pagarmos dentro da nossa empresa.

# 5. Resultados

![image](https://user-images.githubusercontent.com/94385953/150644908-54c974db-d671-4c0a-96e7-53feced055e4.png)

Com esse nosso código seguindo nossas funções conseguimos gerar a tabela acima. Conseguimos agora salvar esse csv em formato excel e mandar de forma automática para o CEO da empresa em cada começo de semana ou em cada mês. 


