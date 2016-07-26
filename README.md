# estudos-maven
Estudo sobre gerenciamento de dependências em Java utilizando Maven disponibilizado pelo curso do Alura.

## Configuração do Maven
### Windows
Para utilização do Maven em sistemas operacionais **Windows** primeiramente devemos fazer o <a href="https://maven.apache.org/download.cgi">download</a> do arquivo **Binary zip archive**.
Após finalizar o donwload devemos configurar as variáveis de ambiente de nossa máquina para que seja possível executar comandos `mvn`.

## Sobre o Maven
* Repositório de plugins do Maven esta disponível atráves do link https://mvnrepository.com/.
* Todo pacote importado pelo Maven é direcionado para a pasta `.m2/repository` presente no diretório do usuário ativo.
* Toda configuração do Maven encontra-se presente no arquivo `pom.xml`, permitindo a adição quanto remoção de dependências (`<dependency></dependency>`), configuração de repositórios `<repositories></repositories>`, versionamento (`<version></version>`) e url (`<url></url>`) do projeto.
* Fases utilizadas para o build do projeto:
 * **`validade`**: verifica se todas as informações necessárias estão presentes no projeto.
 * **`compile`**: compila dependências.
 * **`test`**: executa teste do projeto.
 * **`package`**: geração de pacotes.
 * **`integration-test`**: executa testa de integração.
 * **`verify`**: verifica integridade do pacote gerado.
 * **`install`**: instala pacote no repositório local.
 * **`deploy`**: captura pacote local e faz deploy para seu destino.

## Comandos Maven
### Criando novo projeto
Comando: `mvn archetype:generate -DartifactId=[projectname] -DgroupId=[packagedefault] -DinteractiveMode=[projectconfig (true/false)] -DarchetypeArtfactId=[maventemplate]`
### Compilando projeto
Comando: `mvn compile`
### Verifica projeto
Comando: `mvn verify`
### Testando projeto
Comando: `mvn test`
### Gerar relatório de teste
* Comando: `mvn surefire-reports:reports` - relatório para simples conferência do build
* Comando: `mvn pmd:pdm` - relatório que detecta possíveis margens de bug
* Comando: `mvn pmd:check` - verifica se existe algum suposto bug e não permite dar build até sua correção

### Limpar execução de teste
Comando: `mvn clean`
### Ignorar execução de teste
Comando: `mvn -DskipTests=true package`
### Gerar arquivo *.jar
Comando: `mvn package`
### Executar comando offline
Comando: `mvn -o [comand]`
### Instala repositório local
Comando: `mvn install` - utilizado para instalar dependência de outros projetos locais no repositório do Maven
### Obter últimas versões das dependências presentes no Maven
* Comando: `mvn versions:display-dependency-updates` - verifica novas versões de dependências
* Comando: `mvn versions:use-latest-versions` - efetua download automático de novas versões (**não recomendado**)

###

