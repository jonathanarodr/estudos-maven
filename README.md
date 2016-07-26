# estudos-maven

# Repositório oculto do Maven
Todo pacote importado pelo Maven é direcionado para a pasta '.m2/repository' presente no diretório do usuário ativo.

# Comandos Maven
## Criando novo projeto
mvn archetype:generate -DartifactId=[projectname] -DgroupId=[packagedefault] -DinteractiveMode=[projectdefault (true/false)] -DarchetypeArtfactId=[maventemplate]

## Compilando projeto
mvn compile

## Testando projeto
mvn test

## Gerar relatório de teste
Comando: mvn surefire-reports:reports

## Limpar execução de teste
mvn clean

## Gerar arquivo jar
mvn package

## Executar comando offline
mvn -o [comand]
