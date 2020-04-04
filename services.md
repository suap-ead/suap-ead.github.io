# Services

- **proxy**(*nginx:1.17.8-alpine*) - É o proxy reverso das aplicações web, como todas elas vão rodar em portas diferentes, o proxy ter a responsabilidade de ouvir a porta 80 e a 443 e rotear para a porta correta de cada aplicação. As configurações ficam em `../confs/proxy:/etc/nginx/conf.d`.
- **db**(*postgres:12.1-alpine*) - Aqui ficam todos os bancos PostgreSQL das aplicações web. A porta será aberta por padrão em 
$POSTGRES_EXTERNAL_PORT, ou seja, 5432. As configurações ficam em `../confs/db.env`.
- **redis**(*redis:5.0-alpine*) - Usado para manter as sessões das aplicações web em memória. Não abre porta. Não tem variável de ambiente. Não necessita de volumes.
- **id**(*ifrn/suap_ead_base:1.5.11*) - Serviço de provisionamento, autenticação e do perfil do usuário. As configurações ficam em `../confs/db.env`, `../confs/suap_ead.env`, `../confs/id.env` e `../confs/id_ldap.env`. O volume `../libs/:/libs/` é montado para podermos dinamicamente alterar as bibliotecas sem a necessidade de subir uma nova versão para o PyPI.
- **dashboard**(*ifrn/suap_ead_base:1.5.11*) - Ainda não tem nada em especial, mas será o dashboard que consolida dados de diversos serviços. As configurações ficam em `../confs/db.env`, `../confs/suap_ead.env`, `../confs/dashboard.env`. O volume `../libs/:/libs/` é montado para podermos dinamicamente alterar as bibliotecas sem a necessidade de subir uma nova versão para o PyPI.
- **pre_matricula**(*ifrn/suap_ead_base:1.5.11*) - Sistema de solicitação de matrícula. As configurações ficam em `../confs/db.env`, `../confs/suap_ead.env`, `../confs/pre_matricula.env`. O volume `../libs/:/libs/` é montado para podermos dinamicamente alterar as bibliotecas sem a necessidade de subir uma nova versão para o PyPI.
