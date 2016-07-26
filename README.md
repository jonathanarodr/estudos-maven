# estudos-maven
Estudo sobre gerenciamento de dependências em Java utilizando Maven disponibilizado pelo curso da Alura.

## Sobre o Maven 
### Repositório oculto do Maven
* Todo pacote importado pelo Maven é direcionado para a pasta `.m2/repository` presente no diretório do usuário ativo.
* Toda configuração do Maven encontra-se presente no arquivo `pom.xml`, permitindo a adição quanto remoção de dependências (`<dependency></dependency>`), configuração de repositórios `<repositories></repositories>`, versionamento (`<version></version>`) e url (`<url></url>`) do projeto.

## Comandos Maven
### Criando novo projeto
Comando: `mvn archetype:generate -DartifactId=[projectname] -DgroupId=[packagedefault] -DinteractiveMode=[projectdefault (true/false)] -DarchetypeArtfactId=[## maventemplate ##]`
### Compilando projeto
Comando: `mvn compile`
### Testando projeto
Comando: `mvn test`
### Gerar relatório de teste
Comando: `mvn surefire-reports:reports`
### Limpar execução de teste
Comando: `mvn clean`
### Gerar arquivo *.jar
Comando: `mvn package`
### Executar comando offline
Comando: `mvn -o [comand]`
