# Webmotors
Challenge QA Jr.
webmotors.com
Elaboração de CENÁRIOS DE TESTE  
Front-end e backend do domínio webmotors.com em formato BDD (Behavior Driven Development)/ Gherkin + Teste manual de realização de Cadastro.

Seção 1 - Testes de front-end automatizados

Cenário: Encontrar os seus futuros veículos e consultar detalhes e preços do veículo. 
Implementado via SeleniumIDE para front-end

Procurando pela marca
Dado que possuo cadastro no site webmotors e estou na página de busca; 
Quando digito “Honda” na área de busca da main page;
Então sou direcionado para área de resultados da busca.

Filtrando pelo modelo
Dado que estou na página de resultados de busca para “Honda”;
Quando seleciono o modelo CRV na barra lateral de filtros de busca;
Então a área de resultados de busca apresenta as ofertas disponíveis.

Filtrando pela faixa de valores
Dado que escolhi marca e modelo do carro;
Quando escolho o intervalo de ano e preço;  
Então acesso as opções disponíveis de acordo com minhas opções.

Seção 2 - Testes de backend automatizados

Cenário: Encontrar os seus futuros veículos e consultar detalhes e preços do veículo. 
Implementado via Postman para backend. 
Nos testes automatizados do backend  foi possível testar:

 a listagem de marcas; 
 o filtro de modelos por marca e 
 filtro de versões por modelo. 

Não foi possível testar o filtro de  veículos disponíveis (e seus detalhes) de acordo com alguma marca, modelo ou versão. A única possibilidade, com o Swagger, é filtrar por paginação, sendo assim exibindo veículos de todas as marcas, modelos e versões com seus detalhes.  
Listando as marcas cadastradas
Dado que possuo uma base de dados com marcas cadastradas no site webmotors.com;  
Quando busco pelas marcas cadastradas;  
Então é retornado para mim a lista de marcas cadastrados com seus respectivos IDs.

Listando os modelos filtrando pela marca
Dado que possuo o ID de uma marca cadastrada no site webmotors; 
Quando busco os modelos utilizando o ID da marca como parâmetro/filtro; 
Então é retornado para mim a lista de modelos cadastrados apenas da respectiva marca.

Listando as versões filtrando pelo modelo
Dado que possuo o ID de um modelo cadastrado no site webmotors; 
Quando busco as versões utilizando o ID do modelo como parâmetro/filtro; 
Então é retornado para mim a lista de versões cadastradas apenas do respectivo modelo.

Listando os veículos disponíveis
Dado que possuo uma base de dados com veículos disponíveis cadastrados no site webmotors.com;  
Quando busco pelos veículos disponíveis;  
Então é retornado para mim a lista de veículos cadastrados com seus respectivos detalhes e valores.

Seção 1 - Testes Manuais
Cenário : Realizar o cadastro no domínio webmotors.com

Cadastro
Dado que não possuo cadastro, acesso a página para  “logar ou cadastrar”;
Quando acesso a página de cadastro deixo nome completo, email, senha e confirmação de senha   				
E concordo com Termos e Políticas e Uso e recebo e-mail de validação (que pode estar na caixa de spam) e confirmo;
Então sou direcionado para página principal recebendo mensagem de boas vindas.

Email não informado
Dado que não possuo cadastro, acesso a página para  “logar ou cadastrar”;
Quando submeto o meu cadastro sem o email;
Então não consigo concluir a operação de cadastro.

Senha não informada
Dado que não possuo cadastro, acesso a página para  “logar ou cadastrar”;
Quando submeto o meu cadastro sem a senha;
Então não consigo concluir a operação de cadastro.

Senha divergente
Dado que não possuo cadastro, acesso a página para  “logar ou cadastrar”;
Quando submeto meu cadastro com senha divergente;
Então não consigo concluir a operação de cadastro;

Nenhum campo preenchido
Dado que não possuo cadastro, acesso a página para  “logar ou cadastrar”;
Quando submeto meu cadastro sem preencher os campos;
Então não consigo concluir a operação de cadastro;

