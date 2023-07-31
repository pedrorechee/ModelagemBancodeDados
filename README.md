# Modelagem e Desenvolvimento de um Banco de Dados

# 🤔Etapas:
- 1-Entendimento do Problema 
- 2-Levantar os Requisitos
- 3-Modelo Conceitual
            
            Definir Entidades,Atributos,atributo indentificador,tipos de Relacionamentos
            Diagrama DER
            
4-Modelo Lógico

            Converter minhas entidades em tabelas
            Converter meus atributos em colunas
            Converter meu atributo indentificador em Primary Key 
            Definir Cardinalidades
            Definir Integridade de Restrições
            Realizar o processo de Normalização
            
- 5-Normalização
- 6-Implementar meu modelo Físico

# ⚙ Desenvolvimento 
 ## Etapa 1 e 2
- 1-Teremos alguns premios: Melhor atriz,melhor ator,melhor filme e melhor diretor
- 2-Podemos cadastrar neste banco de forma ilimitada:Diretores,atrizes,atores e os filmes
- 3-Todos os que foram cadastrados tem q estar associados a alguma disputa de algum premio  
- 4-Cada ator pode participar de 1 ou varios filmes
- 5-Um ator pode ser um diretor mas deve ser cadastrado de forma diferente
- 6-Cada diretor ator e atriz tem um código de indentificação diferente
- 7-Preciso de informações de localidade,nome completo ,nacionalidade,gênero daquele diretor,ator ou atriz
- 8-Cada Filme pode estar relacionada a um dos 4 premios definidos anteriomente em um ano 
e eu não posso ter um filme ganhando o mesmo premio em mais de um ano 
- 9-Cada filme só pode estar relacionado a apenas um diretor 

 ## Etapa 3 
Modelo Conceitual
 - Entidades-Diretor,Ator/Atriz,Filmes,Premio
 - Atributos(1)-id_diretor(atributo indentificador),nome,cidade,pais
 - Atributos(2)-id_ator_atriz(atributo indentificador),nome,cidade,pais,genero
 - Atributos(3)-id_filme(atributo indentificador),titulo,id_diretor
 - Atributos(4)-id_premio(atributo indentificador),descricao_premio 

 - Relacionamentos

        Cada diretor dirige um filme
        Cada ator participa de um filme 
        Cada Filme recebe um premio

- Cardinalidade Respectivamente
   -   (1 - *)
   -   (* - *)
   -   (* - *)
 
 ## Etapa 4
  Modelo Lógico
 - Criar tabelas
 - Colunas
 - Chaves
 - Relacionamentos,
 - Definir integridade de restriçoes como as *constrains*

  ## Etapa 5
   Normalização
   
   - Vamos dividir uma nova tabela para não termos a cardinalidade *-*
      em um relacionamento terciário de 1-*
      
   - Nova tabela-Participação
      cod_filme,cod_ator
      
   - Nova tabela-Premiação
      id_filme,id_premio

   ## Etapa 6
   Modelo Físico
   - Deixarei o script em SQL aqui mesmo neste repositório com o nome: "Meuprojeto"









