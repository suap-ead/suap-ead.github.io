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


# Variáveis no template_settings

## Development
1. `DJANGO_DEBUG`=True

## Apps
1. `MY_APPS`=''
1. `SUAP_EAD_LIBS`=suap_ead
1. `DEV_APPS`=debug_toolbar,django_extensions if DEBUG else ''
1. `THIRD_APPS`=rest_framework_swagger,rest_framework
1. `DJANGO_APPS`=django.contrib.admin,django.contrib.auth,django.contrib.contenttypes,django.contrib.sessions,django.contrib.messages,django.contrib.staticfiles'

## Middleware
1. `DJANGO_MIDDLEWARE`=django.middleware.security.SecurityMiddleware,django.contrib.sessions.middleware.SessionMiddleware,django.middleware.common.CommonMiddleware,django.middleware.csrf.CsrfViewMiddleware,django.contrib.auth.middleware.AuthenticationMiddleware,django.contrib.messages.middleware.MessageMiddleware,django.middleware.clickjacking.XFrameOptionsMiddleware
if DEBUG:
1. `MIDDLEWARE`=debug_toolbar.middleware.DebugToolbarMiddleware

## Database
1. `POSTGRES_ENGINE`=django.db.backends.postgresql_psycopg2
1. `POSTGRES_HOST`=db
1. `POSTGRES_PORT`=5432
1. `POSTGRES_DB`=None
1. `POSTGRES_USER`=postgres
1. `POSTGRES_PASSWORD`=postgres


# Routing
1. `DJANGO_WSGI_APPLICATION`=suap_ead.wsgi.application
1. `DJANGO_ALLOWED_HOSTS`='*' if DEBUG else ''
1. `DJANGO_ROOT_URLCONF`=urls
1. `URL_PATH_PREFIX`=sead/id/
1. `DJANGO_STATIC_URL`="/" + URL_PATH_PREFIX + 'static/'
1. `STATIC_ROOT`="/static/" + URL_PATH_PREFIX

# Localization
1. `DJANGO_USE_I18N`=pt-br
1. `DJANGO_USE_I18N`=UTC
1. `DJANGO_USE_I18N`=True
1. `DJANGO_USE_L10N`=True
1. `DJANGO_USE_TZ`=True

# Session
1. `DJANGO_SESSION_COOKIE_AGE`=1209600
1. `DJANGO_SESSION_COOKIE_DOMAIN`=None
1. `SDJANGO_ESSION_COOKIE_HTTPONLY`=True
1. `DJANGO_SESSION_COOKIE_NAME`='%s_sessionid' % session_slug
1. `DJANGO_SESSION_COOKIE_PATH"`=/
1. `DJANGO_SESSION_COOKIE_SAMESITE`=Lax
1. `DJANGO_SESSION_COOKIE_SECURE`=False
1. `DJANGO_SESSION_ENGINE`=redis_sessions.session
1. `DJANGO_SESSION_EXPIRE_AT_BROWSER_CLOSE`=False
1. `DJANGO_SESSION_FILE_PATH`=None
1. `DJANGO_SESSION_SAVE_EVERY_REQUEST`=False
1. `DJANGO_SESSION_SERIALIZER`=django.contrib.sessions.serializers.JSONSerializer
1. `DJANGO_SESSION_REDIS_HOST`=redis
1. `DJANGO_SESSION_REDIS_PORT`=6379
1. `DJANGO_SESSION_REDIS_DB`=0
1. `DJANGO_SESSION_REDIS_PASSWORD`=redis_password
1. `DJANGO_SESSION_REDIS_PREFIX`='%s_session' % session_slug
1. `DJANGO_SESSION_REDIS_SOCKET_TIMEOUT`=0.1
1. `DJANGO_SESSION_REDIS_RETRY_ON_TIMEOUT`=False

# Auth and Security
1. `SUAP_EAD_ID_JWT_AUTHORIZE`=/ead/id/jwt/authorize/
1. `SUAP_EAD_ID_JWT_VALIDATE`=http://id:8000/ead/id/jwt/validate/
1. `SUAP_EAD_ID_JWT_LOGOUT`=http://id:8000/ead/id/logout/
1. `SUAP_EAD_ID_JWT_CLIENT_ID`=_SUAP_EAD_ID_JWT_CLIENT_ID_
1. `SUAP_EAD_ID_JWT_SECRET`=_SUAP_EAD_ID_JWT_SECRET_
1. `SUAP_EAD_UTILS_AUTH_JWT_BACKEND`=suap_ead.backends.PreExistentUserJwtBackend
1. `DJANGO_SECRET_KEY`=changeme
1. `DJANGO_LOGIN_URL`=URL_PATH_PREFIX + 'jwt/login'
1. `DJANGO_LOGOUT_URL`=URL_PATH_PREFIX + 'logout/'
1. `DJANGO_LOGIN_REDIRECT_URL`=URL_PATH_PREFIX
1. `DJANGO_LOGOUT_REDIRECT_URL`=URL_PATH_PREFIX
1. `DJANGO_AUTH_USER_MODEL`=auth.User
1. `DJANGO_AUTHENTICATION_BACKENDS`=django.contrib.auth.backends.ModelBackend

# LDAP (if USE_LDAP==True)
1. `LDAP_AUTH_URL`=''
1. `LDAP_AUTH_USE_TLS`=False
1. `LDAP_AUTH_SEARCH_BASE`=None
1. `LDAP_AUTH_OBJECT_CLASS`=user
1. `LDAP_AUTH_USER_FIELDS`=None
1. `LDAP_AUTH_USER_LOOKUP_FIELDS`=username
1. `LDAP_AUTH_CLEAN_USER_DATA`=None
1. `LDAP_AUTH_SYNC_USER_RELATIONS`=None
1. `LDAP_AUTH_FORMAT_SEARCH_FILTERS`=None
1. `LDAP_AUTH_ACTIVE_DIRECTORY_DOMAIN`=None
1. `LDAP_AUTH_CONNECT_TIMEOUT`=10
1. `LDAP_AUTH_RECEIVE_TIMEOUT`=10
1. `LDAP_AUTH_FORMAT_USERNAME`=django_python3_ldap.format_username_active_directory
1. `LDAP_ACTIVE_VALUE`=512
1. `DJANGO_AUTHENTICATION_BACKENDS`=django_python3_ldap.auth.LDAPBackend
