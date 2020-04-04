# Volumes

## De configuração

### proxy:
- "../confs/proxy:/etc/nginx/conf.d"



## De dados

### db:
- "../volumes/pgdata:/var/lib/postgresql/data"



## De código

### db:
- "./db/initdb_scripts:/docker-entrypoint-initdb.d"

### id
- '../apps/id:/apps/app'
- '../libs/:/libs/'

### dashboard:
- '../apps/dashboard:/apps/app'
- '../libs/:/libs/'

### pre_matricula:
- '../apps/pre_matricula:/apps/app'
- '../libs/:/libs/'
