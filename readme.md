# Wordpress - docker

## Desenvolvimento

1. Copie o arquivo `uploads.ini.modelo` para `uploads.ini` e substitua as seguintes variáveis:
  * `%UPLOAD_MAX_FILE_SIZE%`: Tamanho máximo para realizar upload de arquivos
  * `%POST_MAX_SIZE%`: Tamanho máximo para post

2. Copie o arquivo `env.modelo` para `.env` e substitua as seguintes variáveis:
  * `%APP_PORT%`: Porta na qual vai ser acessível sua aplicação. Ex: localhost:8080
  * `%APP_DEBUG`: Indica se vai mostrar erros. **1** para sim e **0** para não
  * `%BD_NAME%`: Nome do banco de dados
  * `%BD_USER%`: Nome do usuário do banco de dados
  * `%BD_PASS%`: Senha do usuário do banco de dados
  * `%BD_PASS_ROOT%`: Senha do usuário root do banco de dados
  * `%BD_PORT%`: Porta de acesso do banco de dados
  * `%BD_DIR_LIB%`: Local onde fica os arquivos
  * `%CONTAINER_WORDPRESS_NAME%`: Nome do container do wordpress
  * `%CONTAINER_BD_NAME%`: Nome do container do banco de dados

3. Execute
  ```
  docker-compose up -d
  ```