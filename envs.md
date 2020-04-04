# Variáveis de ambiente

Aqui estão as variáveis de ambiente e seus valores padrões contidos em `./bin/confs_examples`.

## db

1. `POSTGRES_HOST`=db
1. `POSTGRES_PORT`=5432
1. `POSTGRES_DATABASE`=postgres
1. `POSTGRES_USER`=sead_user
1. `POSTGRES_PASSWORD`=sead_pass
1. `POSTGRES_DB_ID`=sead_id

## suap_ead

1. `DJANGO_DEBUG`=True
1. `GUNICORN_TIMEOUT`=30
1. `GUNICORN_NUM_WORKERS`=3
1. `GUNICORN_LOG_LEVEL`=DEBUG
1. `SUAP_EAD_ID_URL`=/sead/id/
1. `SUAP_EAD_ID_JWT_AUTHORIZE`=/sead/id/jwt/authorize/
1. `SUAP_EAD_ID_JWT_VALIDATE`=http://id:8000/sead/id/jwt/validate/
1. `SUAP_EAD_ID_JWT_LOGOUT`=/sead/id/logout/
1. `SUAP_EAD_ID_JWT_CLIENT_ID`=_SUAP_EAD_ID_JWT_CLIENT_ID_
1. `SUAP_EAD_ID_JWT_SECRET`=_SUAP_EAD_ID_JWT_SECRET_
1. `DJANGO_SECURE_PROXY_SSL_HEADER`=HTTP_X_FORWARDED_PROTO,https
1. `DJANGO_SESSION_REDIS`='{"host":"redis","port":6379,"db":0,"password":"redis_password","prefix":"session","socket_timeout":1,"retry_on_timeout":false}'
1. `DJANGO_SESSION_ENGINE`=redis_sessions.session


## id

1. `DJANGO_DEBUG`=True
1. `URL_PATH_PREFIX`=sead/id/
1. `AUTHENTICATION_BACKENDS`=django_python3_ldap.auth.LDAPBackend,django.contrib.auth.backends.ModelBackend


## id_ldap

1. `LDAP_AUTH_URL`=ldap://0.0.0.0
1. `LDAP_AUTH_USE_TLS`=False
1. `LDAP_AUTH_SEARCH_BASE`=dc=domainname,dc=local
1. `LDAP_AUTH_OBJECT_CLASS`=user
1. `LDAP_AUTH_USER_FIELDS`='{"key": "value"}'
1. `LDAP_AUTH_USER_LOOKUP_FIELDS`=username
1. `LDAP_AUTH_CLEAN_USER_DATA`=django_python3_ldap.utils.clean_user_data
1. `LDAP_AUTH_SYNC_USER_RELATIONS`=django_python3_ldap.utils.sync_user_relations
1. `LDAP_AUTH_FORMAT_SEARCH_FILTERS`=django_python3_ldap.utils.format_search_filters
1. `LDAP_AUTH_FORMAT_USERNAME`=django_python3_ldap.utils.format_username_active_directory
1. `LDAP_AUTH_ACTIVE_DIRECTORY_DOMAIN`=domainname
1. `LDAP_AUTH_CONNECT_TIMEOUT`=10
1. `LDAP_AUTH_RECEIVE_TIMEOUT`=10
1. `LDAP_ACTIVE_VALUE`=512


## dashboard

1. `DJANGO_DEBUG`=True
1. `MY_APPS`=dashboard
1. `POSTGRES_DB`=sead_dashboard
1. `URL_PATH_PREFIX`=sead/dashboard/
1. `DJANGO_SECRET_KEY`=changeme
1. `DJANGO_LOGIN_URL`=/sead/dashboard/jwt/login
1. `DJANGO_LOGOUT_URL`=/sead/dashboard/logout/
1. `DJANGO_LOGIN_REDIRECT_URL`=/sead/dashboard/
1. `DJANGO_LOGOUT_REDIRECT_URL`=/sead/dashboard/
1. `DJANGO_AUTHENTICATION_BACKENDS`=django.contrib.auth.backends.ModelBackend


## pre_matricula

1. `DJANGO_DEBUG`=True
1. `URL_PATH_PREFIX`=pre_matricula/
1. `POSTGRES_DB`=sead_pre_matricula
1. `AUTHENTICATION_BACKENDS`=django_python3_ldap.auth.LDAPBackend,django.contrib.auth.backends.ModelBackend
