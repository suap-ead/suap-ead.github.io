# Variáveis de ambiente

## db

POSTGRES_HOST=db
POSTGRES_PORT=5432
POSTGRES_DATABASE=postgres
POSTGRES_USER=sead_user
POSTGRES_PASSWORD=sead_pass
POSTGRES_DB_ID=sead_id

# suap_ead

DEBUG=True

GUNICORN_TIMEOUT=30
GUNICORN_NUM_WORKERS=3
GUNICORN_LOG_LEVEL=DEBUG

SUAP_EAD_ID_URL=/sead/id/
SUAP_EAD_ID_JWT_AUTHORIZE=/sead/id/jwt/authorize/
SUAP_EAD_ID_JWT_VALIDATE=http://id:8000/sead/id/jwt/validate/
SUAP_EAD_ID_JWT_LOGOUT=/sead/id/logout/
SUAP_EAD_ID_JWT_CLIENT_ID=_SUAP_EAD_ID_JWT_CLIENT_ID_
SUAP_EAD_ID_JWT_SECRET=_SUAP_EAD_ID_JWT_SECRET_

#DJANGO_SECURE_PROXY_SSL_HEADER=HTTP_X_FORWARDED_SERVER,example.com
DJANGO_SECURE_PROXY_SSL_HEADER=HTTP_X_FORWARDED_PROTO,https

DJANGO_SESSION_REDIS='{"host":"redis","port":6379,"db":0,"password":"redis_password","prefix":"session","socket_timeout":1,"retry_on_timeout":false}'
DJANGO_SESSION_ENGINE=redis_sessions.session


## id

DJANGO_DEBUG=True
URL_PATH_PREFIX=sead/id/
AUTHENTICATION_BACKENDS=django_python3_ldap.auth.LDAPBackend,django.contrib.auth.backends.ModelBackend


# id_ldap

LDAP_AUTH_URL=ldap://0.0.0.0
LDAP_AUTH_USE_TLS=False
LDAP_AUTH_SEARCH_BASE=dc=domainname,dc=local
LDAP_AUTH_OBJECT_CLASS=user
LDAP_AUTH_USER_FIELDS='{"key": "value"}'
LDAP_AUTH_USER_LOOKUP_FIELDS=username
LDAP_AUTH_CLEAN_USER_DATA=django_python3_ldap.utils.clean_user_data
LDAP_AUTH_SYNC_USER_RELATIONS=django_python3_ldap.utils.sync_user_relations
LDAP_AUTH_FORMAT_SEARCH_FILTERS=django_python3_ldap.utils.format_search_filters
LDAP_AUTH_FORMAT_USERNAME=django_python3_ldap.utils.format_username_active_directory
LDAP_AUTH_ACTIVE_DIRECTORY_DOMAIN=domainname
LDAP_AUTH_CONNECT_TIMEOUT=10
LDAP_AUTH_RECEIVE_TIMEOUT=10
LDAP_ACTIVE_VALUE=512


# dashboard

DJANGO_DEBUG=True
MY_APPS=dashboard
POSTGRES_DB=sead_dashboard
URL_PATH_PREFIX=sead/dashboard/
DJANGO_SECRET_KEY=changeme
DJANGO_LOGIN_URL=/sead/dashboard/jwt/login
DJANGO_LOGOUT_URL=/sead/dashboard/logout/
DJANGO_LOGIN_REDIRECT_URL=/sead/dashboard/
DJANGO_LOGOUT_REDIRECT_URL=/sead/dashboard/
DJANGO_AUTHENTICATION_BACKENDS=django.contrib.auth.backends.ModelBackend


# pre_matricula

DJANGO_DEBUG=True
URL_PATH_PREFIX=pre_matricula/
AUTHENTICATION_BACKENDS=django_python3_ldap.auth.LDAPBackend,django.contrib.auth.backends.ModelBackend
