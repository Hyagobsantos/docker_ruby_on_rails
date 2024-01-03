# Documentação

## Configuração Inicial

Dê permissão de escrita para o script de aplicação:

```bash
sudo chmod +x ./script/app
```

#### 1. Execute o script de ajuda para visualizar as opções disponíveis:

```bash
./script/app help
```

#### 2. Execute o script para configurar o projeto:

```bash
./script/app setup
```

#### 3. Aguarde até que os arquivos sejam criados.

## Configuração do Banco de Dados

#### 1. No arquivo config/database.yml, ajuste as configurações para o PostgreSQL:

```yaml
default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password: password
  pool: 5

development:
  <<: *default
  database: myapp_development

test:
  <<: *default
  database: myapp_test
```

## Inicialização do Projeto

#### 1. Execute o script para iniciar o projeto:

```bash
./script/app start
```

#### 2. Execute o script para iniciar o projeto:

```bash
docker compose run web rake db:create

```

#### 3. Abra o navegador e acesse a rota:

http://localhost:3000

#### 4. Para acessar o bash do container:

```bash
./script/app bash
```

## Criação de Scaffold Básico

#### 1. Crie um scaffold básico para o modelo User:

```ruby
rails generate scaffold User name:string age:integer
```

#### 2. Execute a migration para aplicar as alterações ao banco de dados:

```runy
rails db:migrate
```

#### 3. Acesse a rota para testar o scaffold:

http://localhost:3000/users

> Agora, você configurou, inicializou e criou um scaffold básico no seu projeto Rails. Siga as etapas conforme necessário para o desenvolvimento do seu aplicativo.
