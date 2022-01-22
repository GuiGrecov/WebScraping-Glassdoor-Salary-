# WebScraping-Glassdoor-Salary

![image](https://user-images.githubusercontent.com/94385953/150644222-0aedc7c1-9855-45d4-941d-1199be58ad2b.png)
<br>
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
<br>
![image](https://user-images.githubusercontent.com/94385953/150644564-bad5cb8f-ecd9-4dbb-b340-0de49e7e690a.png)
<br>
Na imagem acima vemos que na maioria dos casos, vamos ter mais de uma página para conseguir fazer o scraping. Com isso vale criar uma segunda função que agrupe todos os dados em somente um arquivo. 



# 4. Limitações 

Como esse código participa de uma extração de dados que foram inseridos anonimamente, pode haver alguns erros nos valores de alguns salários. **RECOMENDAÇÕES:** Caso queira retirar alguns insight dos dados, vale retirar os outliers. Por se tratar de dados anônimos e queremos um "norte" de valor em salários para pagarmos dentro da nossa empresa.

# 5. Resultados

![image](https://user-images.githubusercontent.com/94385953/150644908-54c974db-d671-4c0a-96e7-53feced055e4.png)
<br>
Com esse nosso código seguindo nossas funções conseguimos gerar a tabela acima. Conseguimos agora salvar esse csv em formato excel e mandar de forma automática para o CEO da empresa em cada começo de semana ou em cada mês. 

**O RESULTADO SE ENCONTRA NESSA PÁGINA:** https://github.com/GuiGrecov/WebScraping-Glassdoor-Salary-/tree/main/datas

# 6. Arquiterura de Web Scraping
<br>
![image](https://user-images.githubusercontent.com/94385953/150645445-5704eb79-ea64-4ede-aae3-8e089071626a.png)
<br>
* **JOB 1:** Gerar um arquivo individual para cada página que o usuário analisou pertinente. Nessa etapa usamos a função: webscraping_glassdoor(). Para roadr essa função comentada anteriormente precisamos somente salvar essas URL's em variáveis - no Notebook utilizei variáveis com nomes "page1", "page2", "page3",...
*  **JOB 2:** Para conseguir fazer a limpeza de Dados utilizamos funções do tipo REGEX. Foi a saída mais fácil que encontrei para puxar os arquivo em um formato mais amigável para o usuário. 
* **JOB 3:** Nesta parte das tarefas fizemos uma função nomeada como juntar_df() a qual precisa receber uma "lista" com todas as variáveis selecionada na etapa anterior. *Exemplo: No job 1 e 2 eu selecionei duas páginas para fazer o Scraping - "page1" e "page2". Com isso nesta etapa preciso agrupar essas duas variáveis em uma lista e depois colocar essa lista na função juntar_df(), desta forma: juntar_df(page_total).*
* **JOB 4** Essa etapa é clásscia em qualquer trabalho de Web Scraping somente geramos um arquivo CSV ou um XLS com a tabela feita durante as outras etapas. 

# 7. Otimizações Futuras

* 1. Fazer uma agendamento no agendador do Windows, ou se for Linux utilizando uma biblioteca de agendar tarefas do Linux. 
* 2. Utilizar bibliotecas que contenha bot's que fazem o envio para alguns e-mails de forma automática. Para o CEO receber os arquivos de forma automática em determinado intervalo de tempo 
 
