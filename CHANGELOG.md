2020-06-02 - Role: edxapp
2020-06-02   - Add a new `edxapp_sandbox_python_version` variable that deterimens the python version of the edxapp sandbox
2020-06-02   used for instructor python code.  This will default to `python3.5` but can be reverted to `python2.7` if necessary.
2020-06-02 
2020-05-06 - Role: all
2020-05-06   - Split the COMMON_SANDBOX_BUILD variable with its two components: SANDBOX_CONFIG and CONFIGURE_JWTS.
2020-05-06 
2020-05-06   - Disable install of private requirements for docker devstack.
2020-05-05 - Role: edxapp
2020-05-05   - enable paver autocomplete in docker devstack
2020-05-05 
2020-04-24     Must be set if user credentials are in the connection string, or use `""` if no user credentials required.
2020-04-21 - Role: forum
2020-04-21   - Added `FORUM_MONGO_AUTH_MECH` to allow the authentication mechanism to be configurable.
2020-04-21     Defaults to `":scram"`, which is supported by Mongo>=3.0, because `":mongodb_cr"` is removed in Mongo>=4.0.
2020-04-21     Use `":mongodb_cr"` for mongo 2.6.
2020-04-21 
2020-04-15     - ENTERPRISE_CATALOG_WORKERS_ENABLE_NEWRELIC_DISTRIBUTED_TRACING
2020-04-15     - ENTERPRISE_CATALOG_NEWRELIC_WORKERS_APPNAME
2020-04-15     - REGISTRAR_WORKERS_ENABLE_NEWRELIC_DISTRIBUTED_TRACING
2020-04-15     - REGISTRAR_NEWRELIC_WORKERS_APPNAME
2020-04-14 - Docker: edxapp
2020-04-14 
2020-04-14 - Roles: edx_django_service, registrar, enterprise_catalog
2020-04-14   - Moved celery worker supervisor config files/scripts into edx_django_service
2020-04-14   - Removed the following variables
2020-04-14     - ENTERPRISE_CATALOG_WORKER_DEFAULT_STOPWAITSECS
2020-04-14     - ENTERPRISE_CATALOG_CELERY_HEARTBEAT_ENABLED
2020-04-14     - REGISTRAR_WORKER_DEFAULT_STOPWAITSECS
2020-04-14     - REGISTRAR_CELERY_HEARTBEAT_ENABLED
2020-04-14 
2020-03-31 - Role: edxapp
2020-03-31   - Added Stanford-developed Image Modal XBlock.
2020-03-31 
2020-03-23 - Role: edxapp
2020-03-23   - Added Stanford-developed SQL Grader XBlock.
2020-03-23 
2020-03-04 # Changelog
2020-03-04 All notable changes to this project will be documented in this file.
2020-03-04 Add any new changes to the top(right below this line).
2020-03-04 
2020-03-04 - Role: mount_ebs
2020-03-04   - Added check for disk size, size is now a required parameter in variables volumes and MONGO_VOLUMES
2020-03-04   - This is to prevent mounting the wrong volumes when AWS swaps the order
2020-03-04 
2020-03-04 - Role: all
2020-03-04   - Removed OPENID settings
2020-03-04 
2020-03-04 - Role: all
2020-03-04   - Removed all settings with OIDC in name
2020-03-04 
2020-02-26 - Role: edxapp
2020-02-26   - Added `ENTERPRISE_LEARNER_PORTAL_HOSTNAME` env var for lms.
2020-02-26 
2020-02-25 - Role: all
2020-02-25   - Removed the unused task timing callback plugin.
2020-02-24 - Role: ecommerce
2020-02-24   - Added `ENTERPRISE_LEARNER_PORTAL_HOSTNAME` env var for ecommerce.
2020-02-24 
2020-01-31 - Role: edxapp
2020-01-31   - Added Stanford-developed Free Text Response XBlock.
2020-01-31 
2020-01-31 - Role: edxapp
2020-01-31   - Added Stanford-developed Submit-and-Compare XBlock.
2020-01-31 
2020-01-29 - Role: edxapp
2020-01-29   - Added Stanford-developed Qualtrics and In-Video Quiz XBlocks.
2020-01-29 
2020-01-29 - Open edX
2020-01-29   - Don't use AWS_GATHER_FACTS, it was only for tagging which we don't need.
2020-01-29 
2020-01-24 - Open edX
2020-01-24   - The wrong version of xqueue was being installed, fixed.
2020-01-24 
2020-01-24 
2020-01-24   `EDXAPP_RETIREMENT_SERVICE_USER_NAME` to generic_env_config to allow user retirement to be configurable.
2020-01-21 - Role: enterprise_catalog
2020-01-21   - Added infrstructure to start up and deploy celery workers
2020-01-21 
2020-01-07 - Role: insights
2020-01-07   - install libssl-dev, needed for mysqlclient
2020-01-03 - Role: insights
2020-01-03   - add DOT config (deprecate DOP)
2020-01-03 
2019-12-26 - Role: edxapp
2019-12-26   - Added Celery worker `prefetch_optimization` option to allow switching from 'default' to 'fair' (only write to available worker processes)
2019-12-26 
2019-12-20 - Open edX
2019-12-20   - native.sh needed to uninstall pyyaml to proceed
2019-12-20 
2019-12-09 - Role: enterprise_catalog
2019-12-09   - Create role
2019-12-09 
2019-12-04 - Role: blockstore
2019-12-04   - Increased upload limit to 10M
2019-12-04 
2019-11-12 - Role: ecommerce
2019-11-12   - Fixed paypal payment processor default configuration
2019-11-12 
2019-08-30 - Role: edxapp
2019-08-30   - Added `ENABLE_PUBLISHER` for indicating that the publisher frontend service is in use
2019-08-30 
2019-08-30 - Role: discovery
2019-08-30   - Added `ENABLE_PUBLISHER` for indicating that the publisher frontend service is in use
2019-08-30 
2019-08-02 - Role: edxapp
2019-08-02   - Added `ENABLE_ENROLLMENT_RESET` feature flag for masters integration sandboxes
2019-08-02 
2019-08-01 - Role: conductor
2019-08-01   - New role added to configure the conductor service
2019-08-01 
2019-08-01   - Set CORS_ORIGIN_WHITELIST.
2019-07-22 - Role: jwt_signature
2019-07-22   - Added role to inject JWT signing keys into application config, used from edxapp, worker, and registrar.
2019-07-22 
2019-07-15 - Playbook: masters_sandbox_update
2019-07-15   - Create edx partner
2019-07-15 
2019-07-12 - Role: registrar
2019-07-12   - Set CSRF_TRUSTED_ORIGINS.
2019-07-12 
2019-07-12 - Role: registrar
2019-07-12 
2019-07-11 - Role: discovery
2019-07-11   - Override DISCOVERY_MYSQL_REPLICA_HOST to `edx.devstack.mysql` in docker.
2019-07-11 
2019-07-10 - Playbook: masters_sandbox
2019-07-10   - Include call to create_api_access_request
2019-07-10 
2019-07-09 - Role: discovery
2019-07-09   - Add mysql replica settings to env config.
2019-07-09 
2019-07-05 - Playbook: program_manager
2019-07-05   - Added playbook to setup program-manager micro-frontend application on sandboxes
2019-07-05 
2019-07-05 - Role: program_manager
2019-07-05   - Created the program-manager role for micro-frontend application to be setup
2019-07-05 
2019-06-24 - Role: common_vars
2019-06-24   - Default `COMMON_JWT_PUBLIC_SIGNING_JWK_SET` to `''`
2019-06-24     instead of `!!null`. Because of how this setting is handled,
2019-06-24     `!!null` ends up rendering as the literal string `None` instead
2019-06-24     of the value `null`, which causes JSON decoding to fail
2019-06-24     wherever the default value is used (as `'None'` is not valid JSON).
2019-06-24     By setting the default to a Falsy value like the
2019-06-24     empty string, edx-drf-extensions does not attempt to JSON-
2019-06-24     decode it.
2019-06-24 
2019-06-20 - Playbook: masters_sandbox
2019-06-20   - Added playbook to setup user and api access
2019-06-20 
2019-06-19 - Role: registrar
2019-06-19   - Changed `REGISTRAR_CELERY_ALWAYS_EAGER` default to `false`.
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Added `REGISTRAR_CELERY_ALWAYS_EAGER` with default `True`.
2019-06-19   - Injected above settings as environment variable for Registrar.
2019-06-19 
2019-06-19 - Role: supervisor
2019-06-19   - Add registrar to `pre_supervisor_checks.py`
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Added `registrar-workers.conf.j2`
2019-06-19   - Add task to generate `registrar-workers.conf` from `registrar-workers.conf.j2`
2019-06-19   - Added `REGISTRAR_WORKERS_ENABLE_NEWRELIC_DISTRIBUTED_TRACING`
2019-06-19   - Added `REGISTRAR_WORKER_DEFAULT_STOPWAITSECS`
2019-06-19   - Added `REGISTRAR_CELERY_HEARTBEAT_ENABLED`
2019-06-19   - Added `REGISTRAR_NEWRELIC_WORKERS_APPNAME`
2019-06-19   - Added `REGISTRAR_CELERY_WORKERS`
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Added `REGISTRAR_CELERY_BROKER_TRANSPORT`.
2019-06-19   - Added `REGISTRAR_CELERY_BROKER_USER`.
2019-06-19   - Added `REGISTRAR_CELERY_BROKER_PASSWORD`.
2019-06-19   - Added `REGISTRAR_CELERY_BROKER_HOSTNAME`.
2019-06-19   - Added `REGISTRAR_CELERY_BROKER_VHOST`.
2019-06-19   - Injected all above settings as environment variables for Registrar.
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Added `REGISTRAR_API_ROOT`
2019-06-19   - Modified `REGISTRAR_MEDIA_URL`.
2019-06-19 
2019-06-19 - Role: edx_django_service
2019-06-19   - Added new overridable variable `edx_django_service_api_root`
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Replaced `REGISTRAR_MEDIA_ROOT`.
2019-06-19   - Added `REGISTRAR_MEDIA_STORAGE_BACKEND`.
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Replaced `REGISTRAR_LMS_URL_ROOT` with `REGISTRAR_LMS_BASE_URL`.
2019-06-19   - Replaced `REGISTRAR_DISCOVERY_API_URL` with `REGISTRAR_DISCOVERY_BASE_URL`.
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Added `REGISTRAR_SEGMENT_KEY` for segment.io event tracking.
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Added `REGISTRAR_SOCIAL_AUTH_EDX_OAUTH2_KEY` for oauth2.
2019-06-19   - Added `REGISTRAR_SOCIAL_AUTH_EDX_OAUTH2_SECRET` for oauth2.
2019-06-19   - Added `REGISTRAR_BACKEND_SERVICE_EDX_OAUTH2_KEY` for backend auth.
2019-06-19   - Added `REGISTRAR_BACKEND_SERVICE_EDX_OAUTH2_SECRET` for backend auth.
2019-06-19   - Added `REGISTRAR_SERVICE_USER_EMAIL` to have a registrar service user on LMS
2019-06-19   - Added `REGISTRAR_SERVICE_USER_NAME` to have a registrar service user on LMS
2019-06-19 
2019-06-19 - Role: registrar
2019-06-19   - Create role
2019-06-19 
2019-06-12 - Role: oauth_client_setup
2019-06-12   - Ensure that created DOT applications have corresponding ApplicationAccess records with user_id scope.
2019-06-12 
2019-06-12 - Role: edx_notes_api
2019-06-12   - Added `EDX_NOTES_API_HOSTNAME` to set a hostname for the edx-notes-api IDA.
2019-06-12 
2019-06-12 - Open edX
2019-06-12   - Added `SANDBOX_ENABLE_NOTES` to enable/disable setting up the edx-notes-api IDA.
2019-06-12 
2019-06-05 - Role: registrar
2019-06-05   - Change default celery queue to `registrar.default`, explicitly set default exchange and routing key.
2019-06-05 
2019-05-24 - Role: xserver
2019-05-24   - Remove xserver from sandbox builds.
2019-05-24 
2019-05-24 - Role: registrar
2019-05-24   - Add registrar to sandbox builds.
2019-05-24 
2019-05-10 - Role: edxapp
2019-05-10   - Added ENTERPRISE_MARKETING_FOOTER_QUERY_PARAMS to allow for edx specific query params to be added for business marketing footer.
2019-05-10 
2019-05-09 - Role: designer
2019-05-08   - Create role
2019-05-08 
2019-04-16 - Role: edxapp
2019-04-16   - Removed the OfficeMix XBlock (the service that it uses has been dead for months).
2019-04-16 
2019-03-28 - Role: edxapp
2019-03-28   - Added 'SYSTEM_WIDE_ROLE_CLASSES' for use of edx-rbac roles in the jwt in the lms
2019-03-28 
2019-02-20 - Open edX
2019-02-20   - Renamed edx_sandbox.yml to openedx_native.yml
2019-02-20 
2019-02-20 - Role: nginx
2019-02-20   - Added CORS Access-Control-Allow-Origin for static assets.
2019-02-20   - Replaced wildcard Access-Control-Allow-Origin header for fonts. Make sure you set EDXAPP_CORS_ORIGIN_WHITELIST to include all your domains.
2019-02-20 
2019-02-14 - Role: ecomworker
2019-02-14   - Added `assignment_email` default template value in `SAILTHRU` config to send offer assignment emails.
2019-02-14 
2019-02-14   - Added CORS_ORIGIN_WHITELIST and CORS_URLS_REGEX to allow selective CORS whitelisting of origins/urls.
2019-02-14 
2019-02-14   - Remove unused JWT_SECRET_KEYS.
2019-02-14   - Transformed the JWT_ISSUERS to match the format expected by edx-drf-extensions jwt_decode_handler.
2019-02-11 
2019-02-05 - Role: ecommerce
2019-02-05 - common_vars
2019-02-05   - Added new overridable variable `COMMON_LMS_BASE_URL`.
2019-02-05 
2019-01-18 - Role: discovery
2019-01-18   - Added `DISCOVERY_CORS_ORIGIN_WHITELIST` to allow CORS whitelisting of origins.
2019-01-18 
2019-01-14 - Role: nginx
2019-01-14   - Modified robots.txt.j2 to accept the Allow rule.
2019-01-14   - Modified robots.txt.j2 to accept either a single string or a list of strings for agent, disallow, and allow.
2019-01-14 
2019-01-09 - abbey.py
2019-01-09   - Removed abbey.py
2019-01-09 
2019-01-03   - Render auth and env config to a single yml file
2019-01-02 - Role: edxapp
2019-01-02   - Renamed proctoring backend setting to work with edx-proctoring 1.5.0
2019-01-02 
2018-11-20 - Role: edxapp
2018-11-20   - Remove low priority queue, use default instead.
2018-11-20 
2018-11-14 - Role: ecommerce
2018-11-14 
2018-11-14 
2018-11-14 
2018-11-07 - Role: ecommerce
2018-11-05 - Role: edxapp
2018-11-05   - Added `ENTERPRISE_CUSTOMER_SUCCESS_EMAIL` to lms_env_config for configuring emails to the customer success team.
2018-10-31 - Role: edx_django_service
2018-10-31   - Added new overridable variable `edx_django_service_gunicorn_max_requests`
2018-10-31 - Role: ecommerce
2018-10-31   - Set default max_requests to 3000.(eg. restart gunicorn process every 3000 requests.)
2018-10-31 
2018-10-03 - Role: edx_notes_api
2018-10-03   - Added `JWT_AUTH` to edx-notes-api that is used in other IDAs.
2018-10-03 
2018-10-01 - Role: edxapp
2018-10-01   - Removed `PASSWORD_MIN_LENGTH`, `PASSWORD_MAX_LENGTH`, and `PASSWORD_COMPLEXITY` in favor of specifying these in `AUTH_PASSWORD_VALIDATORS`.
2018-10-01 
2018-10-01 - Role: edxapp
2018-10-01   - Added `AUTH_PASSWORD_VALIDATORS` to utilize Django's password validation. Base validators included in configuration are UserAttributeSimilarity to test the password against the username and email using the default similarity threshold of 0.7 (1.0 fails exact matches only), MinimumLength to test password minimum length, and MaximumLength to test password maximum length.
2018-10-01 
2018-09-29 - Role: edxapp
2018-09-29   - Added `EDXAPP_LOGIN_REDIRECT_WHITELIST` which provides a whitelist of domains to which the login/logout pages will redirect.
2018-09-29 
2018-09-17 
2018-09-17 - Role: edxapp
2018-09-17   - `EDXAPP_EDXAPP_SECRET_KEY` no longer has a default value
2018-09-17 
2018-08-30 - Role: edxapp
2018-08-30   - `EDXAPP_CACHE_BACKEND` added to allow overriding Django's memcache backend
2018-08-30 
2018-08-28 - Role: prospectus
2018-08-28   - New role added to configure the prospectus service
2018-08-28 
2018-08-14 - Removed the obsolete install_stack.sh file (the last reference to fullstack)
2018-08-14 
2018-08-07 - Role: analytics_api
2018-08-07   - Added `basic_auth_exempted_paths` configuration for enterprise api endpoints
2018-08-07 
2018-08-06 - Role: edx_django_service
2018-08-06   - Added optional `edx_django_service_allow_cors_headers` boolean option to pass CORS headers (`Access-Control-Allow-Origin` and `Access-Control-Allow-Methods`) on non basic-auth
2018-08-06   calls to support `/api` endpoints for analytics_api.
2018-08-06 
2018-08-03 - Role: edxapp
2018-08-03   - `EDXAPP_X_FRAME_OPTIONS` added in studio to prevent clickjacking.
2018-08-03 
2018-08-02 - Role: analytics_api
2018-08-02   - Added `ANALYTICS_API_CORS_ORIGIN_WHITELIST` to allow CORS whitelisting of origins.
2018-08-02 
2018-07-31 - Role: nginx
2018-07-31   - Added `NGINX_EDXAPP_PROXY_INTERCEPT_ERRORS` to be able to use custom static error pages for error responses from the LMS.
2018-07-31   - Added `NGINX_SERVER_HTML_FILES_TEMPLATE` to make the error file template configurable.
2018-07-31   - Added `NGINX_SERVER_STATIC_FILES` to allow copying static contents to the server static folder. Can be used to deploy static contents for the error pages for example.
2018-07-31 
2018-07-31 - Role: edxapp
2018-07-31   - Added `EDXAPP_X_FRAME_OPTIONS` to prevent click jacking in LMS.
2018-07-31 
2018-07-11   - sandbox.sh has been renamed native.sh to better indicate what it does.
2018-07-10 - git_clone:
2018-07-10   - The working tree is explicitly checked for modified files, to prevent mysterious failures.
2018-07-10 
2018-07-05 - Installation
2018-07-05   - OPENEDX_RELEASE is now required, to prevent accidental installation of master.
2018-07-05 
2018-06-21 - XQueue
2018-06-21   - Expose CLOUDWATCH_QUEUE_COUNT_METRIC which is defined XQueue's settings.py for further dictionary structure
2018-06-21 
2018-06-12 - Role: edxapp
2018-06-12   - Create EDXAPP_CMS_GUNICORN_TIMEOUT and EDXAPP_LMS_STATIC_URL_BASE to allow overriding of the gunicorn timeout
2018-06-12 
2018-06-11 - nginx:
2018-06-11   - remove nginx_cfg - an internal variable that was really only used for the edx-release nginx site, which served version.{html,json} off of a nonstandard port.  The file it served was never populated.
2018-06-11 
2018-06-07 - Structure: edx-east
2018-06-07   - Deprecated the edx-east folder, playbooks now live in the top level directory instead of edx-east/playbooks. A symbolic link was added for now, but should not be relied upon.
2018-06-07 
2018-06-07   - EDXAPP_LMS_STATIC_URL_BASE and EDXAPP_CMS_STATIC_URL_BASE allow a per-application setting of the static URL.  You can stil use EDXAPP_STATIC_URL_BASE for now but we may retire that as we continue to separate LMS and CMS.
2018-06-06 - Role: edxapp
2018-06-06   - EDXAPP_NGINX_SKIP_ENABLE_SITES added to allow you to not sync in the lms or cms nginx configuration.  Instead you can enable them during deployment.
2018-06-06   - EDXAPP_NGINX_DEFAULT_SITES added to allow you to mark both lms and cms as defaults, best paired with picking which site to enable during deployment.
2018-06-06 
2018-05-11   - XQUEUE_SETTINGS now prefers production.py over aws_settings.py
2018-05-09 - Role: credentials
2018-05-09   - Set `LANGUAGE_COOKIE_NAME` so that Credentials will use the global language cookie.
2018-05-09 
2018-05-08 - Role: edxapp
2018-05-08   - Added `PASSWORD_POLICY_COMPLIANCE_ROLLOUT_CONFIG` to make configurable whether password complexity is checked on login and how such complexity is rolled out to users.
2018-05-08 
2018-05-03 - Role: XQueue
2018-05-03   - Convert to a yaml config (instead of xqueue.auth.json and xqueue.env.json we get xqueue.yml and it lives by default in /edx/etc/xqueue.yml like standard IDAs)
2018-05-03   - Add XQUEUE_DEFAULT_FILE_STORAGE so that you can specify S3 or Swift in your config
2018-05-03 
2018-04-25 - Role: edxapp
2018-04-25   - Added `RETIREMENT_STATES` to generic_env_config to support making the retirement workflow configurable.
2018-04-25 
2018-04-19 - Removed Vagrantfiles for devstack and fullstack, and supporting files.
2018-04-19 
2018-04-19 - Role: xqueue
2018-04-19   - Added XQUEUE_SUBMISSION_PROCESSING_DELAY and XQUEUE_CONSUMER_DELAY to xqueue env so they can be passed along to the app.
2018-04-19 
2018-04-13 - Role: edxapp
2018-04-13   - Added GOOGLE_SITE_VERIFICATION_ID to move a previously hardcoded value into configuration.
2018-04-13   - Changed `EDXAPP_RETIRED_USERNAME_FMT` to `EDXAPP_RETIRED_USERNAME_PREFIX`. Changed/split `EDXAPP_RETIRED_EMAIL_FMT` to be `EDXAPP_RETIRED_EMAIL_PREFIX` and `EDXAPP_RETIRED_EMAIL_DOMAIN`.
2018-04-13 
2018-04-13     XQUEUE_RABBITMQ_USER XQUEUE_RABBITMQ_PASS XQUEUE_RABBITMQ_VHOST XQUEUE_RABBITMQ_HOSTNAME
2018-04-13 
2018-04-13   - Added `EDXAPP_RETIRED_USERNAME_FMT`, `EDXAPP_RETIRED_EMAIL_FMT`, `EDXAPP_RETIRED_USER_SALTS`, and
2018-04-12   - Retired XQUEUE_WORKERS_PER_QUEUE
2018-04-11 - Role: edxapp
2018-04-11   - Moved `PASSWORD_MIN_LENGTH`, `PASSWORD_MAX_LENGTH`, and `PASSWORD_COMPLEXITY` to generic_env_config to allow CMS and LMS to share these configurations
2018-04-11 
2018-04-09   - Added XQUEUE_CONSUMER_NEWRELIC_APPNAME which is added to the supervisor start of xqueue_consumer
2018-04-09     if you have New Relic enabled.
2018-04-04 - Role xqueue
2018-04-04   - Removed RabbitMQ in earlier changes in XQueue itself, we don't need any of the configuration
2018-04-04     XQUEUE_RABBITMQ_PORT XQUEUE_RABBITMQ_TLS
2018-04-02   - Added NEWRELIC_APPNAME and NEWRELIC_LICENSE_KEY to the configuration files consumed by XQueue.
2018-04-02     Useful for external utilities that are reporting NR metrics.
2018-04-02 - Role: edxapp
2018-04-02 
2018-03-28 - Role: xqueue
2018-03-28   - Added XQUEUE_MYSQL_CONN_MAX_AGE so that you can have xqueue use django's persistent DB connections
2018-03-22 - Role edx_django_service
2018-03-22   - Added maintenance page under the flag EDX_DJANGO_SERVICE_ENABLE_S3_MAINTENANCE.
2018-03-22   - Added the s3_maintenance.j2 file to point to the s3 maintenance page.
2018-03-22 
2018-03-22 
2018-03-20 - Role: splunkforwarder
2018-03-20   - Updated the role so the splunkforwarder can be installed on Amazon Linux OS environment, which is a RHEL variant
2018-03-20 
2018-03-20 - Role: server_utils
2018-03-20   - Update to only do things for debian varient environment
2018-03-20 
2018-03-08 - Role: edxapp
2018-03-08   - Added empty `EDXAPP_PASSWORD_COMPLEXITY` setting to ease overriding complexity.
2018-03-08 
2018-02-27   - The manage_users management command is only run when disable_edx_services is false (previously this play would try
2018-02-27     to update databases while building images, where services are generally disabled).
2018-02-22 - Role: xqueue
2018-02-22   - Remove S3_BUCKET and S3_PATH_PREFIX - they were deprecated prior to ginkgo
2018-02-22   - Remove SERVICE_VARIANT - it was copied from edxapp but never truly used (except to complicate things)
2018-02-22 
2018-02-09   - Added `CERTS_QUEUE_POLL_FREQUENCY` to make configurable the certificate agent's queue polling frequency.
2018-02-06 - Role: certs
2018-02-06 
2018-02-02 - Role: xqueue
2018-02-02   - Added `XQUEUE_SESSION_ENGINE` to allow a configurable xqueue session engine.
2018-02-02   - Added `XQUEUE_CACHES` to allow a configurable xqueue cache.
2018-02-02 
2018-02-02 
2018-01-31 - Role: devpi
2018-01-31   - New role added to configure a devpi service as a pass-through cache for PyPI.
2018-01-31 
2018-01-31 - Role: devpi_consumer
2018-01-31   - Added role to configure Python containers to use devpi for Docker Devstack
2018-01-31 
2018-01-26 - Role: edxapp
2018-01-26   - Added `ENTERPRISE_REPORTING_SECRET` to CMS auth settings to allow edx-enterprise migrations to run.
2018-01-26 
2018-01-25 - Role: edxapp
2018-01-25   - Added `EDXAPP_FERNET_KEYS` to allow for use of django-fernet-keys in LMS.
2018-01-04 - Role: nginx
2018-01-04   - Added `NGINX_EDXAPP_DEFAULT_SITE_THEME` to allow to completely
2018-01-04   override `favicon.ico` file when Comprehensive Theme is enabled.
2018-01-04 
2017-12-14 - Role: edxapp
2017-12-14   - Added `EDX_PLATFORM_REVISION` (set from `edx_platform_version`). This is for
2017-12-14   edx-platform debugging purposes, and replaces calling dealer.git at startup.
2017-12-14 
2017-12-07 - Role: edxapp
2017-12-07   - Added `EDXAPP_BRANCH_IO_KEY` to configure branch.io journey app banners.
2017-12-07 
2017-12-06 - Role: veda_pipeline_worker
2017-12-06   - New role to run all (`deliver, ingest, youtubecallback`) [video pipeline workers](https://github.com/edx/edx-video-pipeline/blob/master/bin/)
2017-12-06 
2017-12-06 - Role: ecomworker
2017-12-06   - Added `ECOMMERCE_WORKER_BROKER_TRANSPORT` with a default value of 'ampq' to be backwards compatible with rabbit.  Set to 'redis' if you wish to use redis instead of rabbit as a queue for ecommerce worker.
2017-12-06 
2017-12-05   - Added `ECOMMERCE_BROKER_TRANSPORT` with a default value of 'ampq' to be backwards compatible with rabbit.  Set to 'redis' if you wish to use redis instead of rabbit as a queue for ecommerce.
2017-12-04 - Role: ecommerce
2017-12-04 
2017-12-01 - Role: credentials
2017-12-01   - This role is now dependent on the edx_django_service role. Settings are all the same, but nearly all of the tasks are performed by the edx_django_service role.
2017-12-01 
2017-11-29 - Role: veda_delivery_worker
2017-11-29   - New role added to run [video delivery worker](https://github.com/edx/edx-video-pipeline/blob/master/bin/deliver)
2017-11-29 
2017-11-23   - Added `EDXAPP_DEFAULT_COURSE_VISIBILITY_IN_CATALOG` setting (defaults to `both`).
2017-11-23 
2017-11-23   - Added `EDXAPP_DEFAULT_MOBILE_AVAILABLE` setting (defaults to `false`).
2017-11-23 
2017-11-21 - Role: veda_ffmpeg
2017-11-21   - New role added to compile ffmpeg for video pipeline. It will be used as a dependency for video pipeline roles.
2017-11-21 
2017-11-15 - Role: nginx
2017-11-15   - Modified `lms.j2` , `cms.j2` , `credentials.j2` , `edx_notes_api.j2` and `insights.j2` to enable HTTP Strict Transport Security
2017-11-15   - Added `NGINX_HSTS_MAX_AGE` to make HSTS header `max_age` value configurable and used in templates
2017-11-14 - Role: edxapp
2017-11-14   - Added `EDXAPP_MONGO_REPLICA_SET`, which is required to use
2017-11-14 
2017-11-14 
2017-11-13 
2017-11-13 - Role: edxapp
2017-11-13   - Added `EDXAPP_ZENDESK_OAUTH_ACCESS_TOKEN` for making requests to Zendesk through front-end.
2017-11-09 - Role: edxapp
2017-11-09   - Added `EDXAPP_LMS_INTERNAL_ROOT_URL` setting (defaults to `EDXAPP_LMS_ROOT_URL`).
2017-11-09 
2017-11-07 - Role: edxapp
2017-11-07   - Added `EDXAPP_CELERY_BROKER_TRANSPORT` and renamed `EDXAPP_RABBIT_HOSTNAME`
2017-11-07     to `EDXAPP_CELERY_BROKER_HOSTNAME`. This is to support non-amqp brokers,
2017-11-07     specifically redis. If `EDXAPP_CELERY_BROKER_HOSTNAME` is unset it will use
2017-11-07     the value of `EDXAPP_RABBIT_HOSTNAME`, however it is recommended to update
2017-11-07     your configuration to set `EDXAPP_CELERY_BROKER_TRANSPORT` explicitly.
2017-11-07 
2017-11-03 - Role: server_utils
2017-11-03   - Install "vim", not "vim-tiny".
2017-11-03 
2017-11-03 - Role: edxapp
2017-11-03   - Added GOOGLE_ANALYTICS_TRACKING_ID setting for inserting GA tracking into emails generated via ACE.
2017-11-03 
2017-10-30 - Role: edxapp
2017-10-30   - Added `EDXAPP_REINDEX_ALL_COURSES` to rebuild the course index on deploy. Disabled by default.
2017-10-30 
2017-10-26 - Role: ecommerce
2017-10-26   - This role is now dependent on the edx_django_service role. Settings are all the same, but nearly all of the tasks are performed by the edx_django_service role.
2017-10-26 
2017-10-24 - Role: notifier
2017-10-24   - Added notifier back to continuous integration.
2017-10-24 
2017-10-20     pymongo.MongoReplicaSetClient in PyMongo 2.9.1.  This should be set to the
2017-10-20     name of your replica set.
2017-10-20     This setting causes the `EDXAPP_*_READ_PREFERENCE` settings below to be used.
2017-10-20   - Added `EDXAPP_MONGO_CMS_READ_PREFERENCE` with a default value of `PRIMARY`.
2017-10-20   - Added `EDXAPP_MONGO_LMS_READ_PREFERENCE` with a default value of
2017-10-20     `SECONDARY_PREFERED` to distribute the read workload across the replica set
2017-10-20     for replicated docstores and contentstores.
2017-10-20   - Added `EDXAPP_LMS_SPLIT_DOC_STORE_READ_PREFERENCE` with a default value of
2017-10-20     `EDXAPP_MONGO_LMS_READ_PREFERENCE`.
2017-10-20   - Added `EDXAPP_LMS_DRAFT_DOC_STORE_CONFIG` with a default value of
2017-10-20     `EDXAPP_MONGO_CMS_READ_PREFERENCE`, to enforce consistency between
2017-10-20     Studio and the LMS Preview modes.
2017-10-20   - Removed `EDXAPP_CONTENTSTORE_ADDITIONAL_OPTS`, since there is no notion of
2017-10-20     common options to the content store anymore.
2017-10-19 - Role: veda_web_frontend
2017-10-19   - New role added for [edx-video-pipeline](https://github.com/edx/edx-video-pipeline)
2017-10-19 
2017-10-07 - Role: discovery
2017-10-07   - Added `DISCOVERY_REPOS` to allow configuring discovery repository details.
2017-10-07 
2017-10-07 - Role: edx_django_service
2017-10-07   - Made the keys `edx_django_service_git_protocol`, `edx_django_service_git_domain`, and `edx_django_service_git_path` of `edx_django_service_repos` all individually configurable.
2017-10-07 
2017-10-05 
2017-10-05 - Role: whitelabel
2017-10-05   - Added `WHITELABEL_THEME_DIR` to point to the location of whitelabel themes.
2017-10-05   - Added `WHITELABEL_ADMIN_USER` to specify an admin user.
2017-10-05   - Added `WHITELABEL_DNS` for DNS settings of themes.
2017-10-05   - Added `WHITELABEL_ORG` for whitelabel organization settings.
2017-09-26 - Role: edxapp
2017-09-26   - Added `EDXAPP_EXTRA_MIDDLEWARE_CLASSES` for configuring additional middleware logic.
2017-09-26 
2017-09-25 - Role: discovery
2017-09-25   - Updated LANGUAGE_CODE to generic english. Added configuration for multilingual language package django-parler.
2017-09-25 
2017-09-14 - Role: edxapp
2017-09-14   - Added `EDXAPP_SCORM_PKG_STORAGE_DIR`, with default value as it was in the server template.
2017-09-14   - Added `EDXAPP_SCORM_PLAYER_LOCAL_STORAGE_ROOT`, with default value as it was in the server template.
2017-09-14 
2017-09-14 - Role: edxapp
2017-09-14   - Added `ENTERPRISE_SUPPORT_URL` variable used by the LMS.
2017-09-14 
2017-09-13 - Role: discovery
2017-09-13   - Added `OPENEXCHANGERATES_API_KEY` for retrieving currency exchange rates.
2017-09-13 
2017-09-12   - Added `EDXAPP_PLATFORM_DESCRIPTION` used to describe the specific Open edX platform.
2017-09-11 - Role: edxapp
2017-09-11   - Added `EDXAPP_ENTERPRISE_TAGLINE` for customized header taglines for different enterprises.
2017-09-11 
2017-09-05 - Role: edxapp
2017-09-05   - Added OAUTH_DELETE_EXPIRED to enable automatic deletion of edx-django-oauth2-provider grants, access tokens, and refresh tokens as they are consumed. This will not do a bulk delete of existing rows.
2017-09-05 
2017-08-23 - Role: mongo_3_2
2017-08-23   - Added role for mongo 3.2, not yet in use.
2017-08-23   - Removed MONGO_CLUSTERED variable. In this role mongo replication is always configured, even if there is only one node.
2017-08-23 
2017-08-16   - Removed unused `EDXAPP_BOOK_URL` setting
2017-08-08 
2017-08-08 - Role: credentials
2017-08-08   - Replaced `CREDENTIALS_OAUTH_URL_ROOT` with `COMMON_OAUTH_URL_ROOT` from `common_vars`
2017-08-08   - Replaced `CREDENTIALS_OIDC_LOGOUT_URL` with `COMMON_OAUTH_LOGOUT_URL` from `common_vars`
2017-08-08   - Replaced `CREDENTIALS_JWT_AUDIENCE` with `COMMON_JWT_AUDIENCE` from `common_vars`
2017-08-08   - Replaced `CREDENTIALS_JWT_ISSUER` with `COMMON_JWT_ISSUER` from `common_vars`
2017-08-08   - Replaced `CREDENTIALS_JWT_SECRET_KEY` with `COMMON_JWT_SECRET_KEY` from `common_vars`
2017-08-08   - Replaced `CREDENTIALS_SOCIAL_AUTH_EDX_OIDC_ISSUER` with `COMMON_JWT_ISSUER` from `common_vars`
2017-08-08 
2017-08-08 - Role: ecommerce
2017-08-08   - Replaced `ECOMMERCE_OAUTH_URL_ROOT` with `COMMON_OAUTH_URL_ROOT` from `common_vars`
2017-08-08   - Replaced `ECOMMERCE_OIDC_LOGOUT_URL` with `COMMON_OAUTH_LOGOUT_URL` from `common_vars`
2017-08-08   - Replaced `ECOMMERCE_JWT_SECRET_KEY` with `COMMON_JWT_SECRET_KEY` from `common_vars`
2017-08-08   - Replaced `ECOMMERCE_SOCIAL_AUTH_EDX_OIDC_ISSUER` with `COMMON_JWT_ISSUER` from `common_vars`
2017-08-04 - Role: edxapp
2017-08-04   - Added `PASSWORD_MIN_LENGTH` for password minimum length validation on reset page.
2017-08-04   - Added `PASSWORD_MAX_LENGTH` for password maximum length validation on reset page.
2017-08-03 
2017-08-03 - Role: edxapp
2017-08-03   - Added `EDXAPP_VIDEO_TRANSCRIPTS_SETTINGS` to configure S3-backed video transcripts.
2017-07-28 - Role: edxapp
2017-07-28   - Added creation of enterprise_worker user to provisioning. This user is used by the edx-enterprise package when making API requests to Open edX IDAs.
2017-07-28 
2017-07-25 - Role: neo4j
2017-07-25   - Increase heap and page caches sizes for neo4j
2017-07-25 
2017-07-21 
2017-07-21 - Role: edxapp
2017-07-21   - Remove EDXAPP_ANALYTICS_API_KEY, EDXAPP_ANALYTICS_SERVER_URL, EDXAPP_ANALYTICS_DATA_TOKEN, EDXAPP_ANALYTICS_DATA_URL since they are old and
2017-07-21   no longer consumed.
2017-07-21 
2017-07-18 
2017-07-18 - Role: insights
2017-07-18   - Moved `THEME_SCSS` from `INSIGHTS_CONFIG` to `insights_environment`
2017-07-14 - Role: forum
2017-07-14   - Added `FORUM_REBUILD_INDEX` to rebuild the ElasticSearch index from the database, when enabled.  Default: `False`.
2017-07-14 
2017-07-14 
2017-07-14 - Role: insights
2017-07-14   - Removed `bower install` task
2017-07-14   - Replaced r.js build task with webpack build task
2017-07-13   - Removed `./manage.py compress` task
2017-07-13 
2017-07-13 - Role: analytics_api
2017-07-13   - Added a number of `ANALYTICS_API_DEFAULT_*` and `ANALYTICS_API_REPORTS_*` variables to allow more selective specification of database parameters (rather than
2017-07-13       overriding the whole structure).
2017-07-06   - Removed authentication requirement for neo4j
2017-06-30 
2017-06-30 - Role: insights
2017-06-30   - Added `INSIGHTS_DOMAIN` to configure the domain Insights is deployed on
2017-06-30   - Added `INSIGHTS_CLOUDFRONT_DOMAIN` to configure the domain static files can be served from
2017-06-30   - Added `INSIGHTS_CORS_ORIGIN_WHITELIST_EXTRA` to configure allowing CORS on domains other than the `INSIGHTS_DOMAIN`
2017-06-28 - Role: edxapp
2017-06-28   - Let `confirm_email` in `EDXAPP_REGISTRATION_EXTRA_FIELDS` default to `"hidden"`.
2017-06-28   - Let `terms_of_service` in `EDXAPP_REGISTRATION_EXTRA_FIELDS` default to `"hidden"`.
2017-06-28 
2017-06-28 
2017-06-27 - Role: ecommerce
2017-06-27   - Added ECOMMERCE_LANGUAGE_COOKIE_NAME which is the name of the cookie the ecommerce django app looks at for determining the language preference.
2017-06-26 - Role: neo4j
2017-06-26   - Enabled splunk forwarding for neo4j logs.
2017-06-26   - Increased maximum amount of open files to 40000, as suggested by neo4j.
2017-06-26   - Updated the java build that neo4j uses to run.
2017-06-26 
2017-06-22 
2017-06-22 - Role: edxapp
2017-06-22   - Added `EDXAPP_BASE_COOKIE_DOMAIN` for sharing cookies across edx domains.
2017-06-21 - Role: edxapp
2017-06-21   - Set the default value for EDXAPP_POLICY_CHANGE_GRADES_ROUTING_KEY to
2017-06-21  'edx.lms.core.default'.
2017-06-21 
2017-06-21 - Role: edxapp
2017-06-21   - Set the default value for EDXAPP_BULK_EMAIL_ROUTING_KEY_SMALL_JOBS to
2017-06-21  'edx.lms.core.low'.
2017-06-21 
2017-06-16 - Role: neo4j
2017-06-16   - Updated neo4j to 3.2.2
2017-06-16 
2017-06-15 - Role: jenkins_master
2017-06-15   - Update pinned use of JDK7 in Jenkins installs to default JDK version from role `oraclejdk`.
2017-06-15 
2017-06-12 - Role: elasticsearch
2017-06-12   - Replaced `elasticsearch_apt_key` and `elastic_search_apt_keyserver` with `elasticsearch_apt_key_url`
2017-06-12   - Updated elasticsearch version to 1.5.0
2017-06-12 
2017-06-08 - Role: edxapp
2017-06-08   - Set the EDXAPP_IMPORT_EXPORT_BUCKET setting to an empty string
2017-06-08 
2017-06-07 - Role: edxapp
2017-06-07   - Updated default value of the EDXAPP_ENTERPRISE_COURSE_ENROLLMENT_AUDIT_MODES setting to ["audit", "honor"]
2017-06-07 
2017-06-07 - Role: edx_notes_api
2017-06-07   - Removed EDX_NOTES_API_ELASTICSEARCH_HOST.
2017-06-07   - Removed EDX_NOTES_API_ELASTICSEARCH_PORT.
2017-06-07   - EDX_NOTES_API_ELASTICSEARCH_URL.
2017-06-07 
2017-06-07 
2017-06-07 - Role: insights
2017-06-07   - Removed `SUPPORT_EMAIL` setting from `INSIGHTS_CONFIG`, as it is was replaced by `SUPPORT_URL`.
2017-06-05 
2017-06-05 - Role: insights
2017-06-05   - Removed `INSIGHTS_FEEDBACK_EMAIL` which is no longer used, as it was deemed redundant with `INSIGHTS_SUPPORT_EMAIL`.
2017-06-01 - Role: nginx
2017-06-01   - Modified `server-template.j2` to be more accessible and configurable.
2017-06-01   - The template should contain the `lang` attribute in the HTML tag.
2017-06-01   - If the image loaded has some meaning, as a logo, it should have the `alt` attribute.
2017-06-01   - After the header 1 (h1) there is no relevant text content, so next it can not be
2017-06-01     another header (h2). It was changed to be a paragraph with the header 2 CSS style.
2017-06-01   - Added `NGINX_SERVER_ERROR_IMG_ALT` with default value as it was in the server template
2017-06-01   - Added `NGINX_SERVER_ERROR_LANG` with default value `en`
2017-06-01   - Added `NGINX_SERVER_ERROR_STYLE_H1` with default value as it was in the server template
2017-06-01   - Added `NGINX_SERVER_ERROR_STYLE_P_H2` with default value as it was in the server template
2017-06-01   - Added `NGINX_SERVER_ERROR_STYLE_P` with default value as it was in the server template
2017-06-01   - Added `NGINX_SERVER_ERROR_STYLE_DIV` with default value as it was in the server template
2017-06-01 
2017-05-31 - Role: edxapp
2017-05-31   - Install development.txt in Vagrant and Docker devstacks
2017-05-31 
2017-05-26 - Role: edxapp
2017-05-26   - Added the EDXAPP_ACTIVATION_EMAIL_SUPPORT_LINK URL with default value `''`.
2017-05-26   - Added the EDXAPP_PASSWORD_RESET_SUPPORT_LINK URL with default value `''`.
2017-05-26 
2017-05-23 - Role: edxapp
2017-05-23   - Added the EDXAPP_SHOW_HEADER_LANGUAGE_SELECTOR feature flag with default value [false]
2017-05-23   - Added the EDXAPP_SHOW_FOOTER_LANGUAGE_SELECTOR feature flag with default value [false]
2017-05-23 
2017-05-23 - Role: edxapp
2017-05-23   - Added the EDXAPP_ENTERPRISE_COURSE_ENROLLMENT_AUDIT_MODES setting with default value ["audit"]
2017-05-23 
2017-05-15 - Role: nginx
2017-05-15   - Added `NGINX_EDXAPP_CMS_APP_EXTRA`, which makes it possible to add custom settings to the site configuration for Studio.
2017-05-15   - Added `NGINX_EDXAPP_LMS_APP_EXTRA`, which makes it possible to add custom settings to the site configuration for the LMS.
2017-05-15 
2017-05-04 
2017-05-04 - Role: edxapp
2017-05-04   - Added `EDXAPP_VIDEO_IMAGE_SETTINGS` to configure S3-backed video images.
2017-04-24 - Role: edxapp
2017-04-24   - DOC_LINK_BASE settings have been removed, replaced by HELP_TOKENS_BOOKS
2017-04-24 
2017-04-24 - Role: edxapp
2017-04-24   - Add the EDXAPP_LANGUAGE_COOKIE setting
2017-04-24 
2017-04-12   - Added a new EDXAPP_MYSQL_CONN_MAX_AGE, default to 0.  Adjust it to change how long a connection is kept open
2017-04-12   for reuse before it is closed.
2017-04-11 - Role: rabbitmq
2017-04-11   - Upgraded to 3.6.9
2017-04-11   - Switched to a PPA rather than a .deb hosted in S3
2017-04-11   - Note that you generally cannot upgrade RabbitMQ live in place https://www.rabbitmq.com/clustering.html
2017-04-11     this is particularly true coming from 3.2 to 3.6.  We are using the shovel plugin to move tasks across clusters
2017-04-11     but their documentation covers different scenarios.
2017-03-31 - Role: edxapp
2017-03-31   - Set preload_app to False in gunicorn config for LMS and Studio.
2017-03-13 
2017-03-13 - Role: edxapp
2017-03-13   - Added `EDXAPP_BLOCK_STRUCTURES_SETTINGS` to configure S3-backed Course Block Structures.
2017-03-07 - Role: analytics_api
2017-03-07   - Added `ANALYTICS_API_AGGREGATE_PAGE_SIZE`, default value 10.  Adjust this parameter to increase the number of
2017-03-07     aggregate search results returned by the Analytics API, i.e. in course_metadata: enrollment_modes, cohorts, and
2017-03-07     segments.
2017-02-27 - Role: xqueue
2017-02-27   - Changed `XQUEUE_RABBITMQ_TLS` default from `true` to `false`.
2017-02-27   - Added `XQUEUE_RABBITMQ_TLS` to allow configuring xqueue to use TLS when connecting to the AMQP broker.
2017-02-27   - Added `XQUEUE_RABBITMQ_VHOST` to allow configuring the xqueue RabbitMQ host.
2017-02-27   - Added `XQUEUE_RABBITMQ_PORT` to allow configuring the RabbitMQ port.
2017-02-27   - Added `EDXAPP_CELERY_BROKER_USE_SSL` to allow configuring celery to use TLS.
2017-02-24 - Role: programs
2017-02-24   - This role has been removed as this service is no longer supported. The role is still available on the [Ficus branch](https://github.com/edx/configuration/releases/tag/open-release%2Fficus.1).
2017-02-16 - Role: mongo_2_6
2017-02-16   - Added `MONGO_AUTH` to turn authentication on/off. Auth is now enabled by default, and was previously disabled by default.
2017-02-16 
2017-02-16   - Added `MONGO_AUTH` to turn authentication on/off. Auth is now enabled by default, and was previously disabled by default.
2017-02-14 - Role: notifier
2017-02-14   - Added `NOTIFIER_DATABASE_ENGINE`, `NOTIFIER_DATABASE_NAME`, `NOTIFIER_DATABASE_USER`, `NOTIFIER_DATABASE_PASSWORD`, `NOTIFIER_DATABASE_HOST`, and `NOTIFIER_DATABASE_PORT` to be able to configure the `notifier` service to use a database engine other than sqlite. Defaults to local sqlite.
2017-02-14   - Deprecated: `NOTIFIER_DB_DIR`: Please use `NOTIFIER_DATABASE_NAME` instead.
2017-02-14 
2017-02-02   - Support parsing the replset JSON in 3.2 and 3.0
2017-02-02 
2017-02-02 - Role: ecommerce
2017-02-02   - Removed `SEGMENT_KEY` which is no longer used.  Segment key is now defined in DB configuration. (https://github.com/edx/ecommerce/pull/1121)
2017-02-01 
2017-02-01 - Role: ecommerce
2017-02-01   - Added `ECOMMERCE_ENTERPRISE_URL` for the `enterprise` API endpoint exposed by a new service `edx-enterprise` (currently hosted by `LMS`), which defaults to the existing setting `ECOMMERCE_LMS_URL_ROOT`.
2017-01-12 - Role: credentials
2017-01-12   - Added `CREDENTIALS_EXTRA_APPS` to enable the inclusion of additional Django apps in the Credentials Service.
2017-01-10   - Added `COMMON_EDXAPP_SETTINGS`. Default: `aws`
2016-11-18 
2016-11-18 - Role: mongo_3_0
2016-11-18   - Changed MONGO_STORAGE_ENGINE to default to wiredTiger which is the default in 3.2 and 3.4 and what edX suggests be used even on 3.0.
2016-11-18     If you have a mmapv1 3.0 install, override MONGO_STORAGE_ENGINE to be mmapv1 which was the old default.
2016-11-03 
2016-11-03 - Role: xqueue
2016-11-03 
2016-11-03 - Role: edxapp
2016-10-27 
2016-10-27 - Role: security
2016-10-27   - Changed SECURITY_UPGRADE_ON_ANSIBLE to only apply security updates.  If you want to retain the behavior of running safe-upgrade,
2016-10-27     you should switch to using SAFE_UPGRADE_ON_ANSIBLE.
2016-10-24 
2016-10-24 - Role: discovery
2016-10-24   - Added `PUBLISHER_FROM_EMAIL` for sending emails to publisher app users.
2016-10-18 
2016-10-18 - Role: edxapp
2016-10-18   - Added `EXPIRING_SOON_WINDOW` to show message to learners if their verification is expiring soon.
2016-10-11 
2016-10-11 - Role: edxapp
2016-10-11   - Added COMPREHENSIVE_THEME_LOCALE_PATHS to support internationalization of strings originating from custom themes.
2016-06-30 - Role: discovery
2016-06-30   - Course Discovery JWT configuration now takes a list of issuers instead of a single issuer.  This change is not backward compatible with older versions of course discovery.
2016-06-30 
2016-06-22 - Role: hadoop_common
2016-06-22   - Enable log retention by default to assist with debugging. Now YARN will retain stdout and stderr logs produced by map reduce tasks for 24 hours. They can be retrieved by running "yarn logs -applicationId YOUR_APPLICATION_ID".
2016-06-22 
2016-06-08 
2016-06-08 - Role: Edxapp
2016-06-08   - `EDXAPP_COMPREHENSIVE_THEME_DIR` is deprecated and is maintained for backward compatibility, `EDXAPP_COMPREHENSIVE_THEME_DIRS`
2016-06-08     should be used instead which is a list of directories. `EDXAPP_COMPREHENSIVE_THEME_DIR` if present will have priority over `EDXAPP_COMPREHENSIVE_THEME_DIRS`
2016-06-08   - `COMPREHENSIVE_THEME_DIR` is deprecated and is maintained for backward compatibility, `COMPREHENSIVE_THEME_DIRS` should be used
2016-06-08     instead which is a list of directories. `COMPREHENSIVE_THEME_DIR` if present will have priority over `COMPREHENSIVE_THEME_DIRS`
2016-05-23 
2016-05-23 - Role: ecommerce
2016-05-23   - Renamed `ECOMMERCE_COMPREHENSIVE_THEME_DIR` to `ECOMMERCE_COMPREHENSIVE_THEME_DIRS`, `ECOMMERCE_COMPREHENSIVE_THEME_DIRS`
2016-05-23     is now a list of directories. Change is backward incompatible.
2016-05-23   - Renamed `COMPREHENSIVE_THEME_DIR` to `COMPREHENSIVE_THEME_DIRS`, `COMPREHENSIVE_THEME_DIRS` is now a list of directories.
2016-05-23     Change is backward incompatible.
2016-01-25 - Role: common
2016-01-25   - Renamed `COMMON_AWS_SYNC` to `COMMON_OBJECT_STORE_LOG_SYNC`
2016-01-25   - Renamed `COMMON_AWS_SYNC_BUCKET` to `COMMON_OBJECT_STORE_LOG_SYNC_BUCKET`
2016-01-25   - Renamed `COMMON_AWS_S3_SYNC_SCRIPT` to `COMMON_OBJECT_STORE_LOG_SYNC_SCRIPT`
2016-01-25   - Added `COMMON_OBJECT_STORE_LOG_SYNC_PREFIX`. Default: `logs/tracking/`
2016-01-25 - Role: aws
2016-01-25   - Removed `AWS_S3_LOGS`
2016-01-25   - Added `vhost` role as dependency
2016-01-25 - Role: edxapp
2016-01-25   - Added `EDXAPP_SWIFT_USERNAME`
2016-01-25   - Added `EDXAPP_SWIFT_KEY`
2016-01-25   - Added `EDXAPP_SWIFT_TENANT_ID`
2016-01-25   - Added `EDXAPP_SWIFT_TENANT_NAME`
2016-01-25   - Added `EDXAPP_SWIFT_AUTH_URL`
2016-01-25   - Added `EDXAPP_SWIFT_AUTH_VERSION`
2016-01-25   - Added `EDXAPP_SWIFT_REGION_NAME`
2016-01-25   - Added `EDXAPP_SWIFT_USE_TEMP_URLS`
2016-01-25   - Added `EDXAPP_SWIFT_TEMP_URL_KEY`
2016-01-25   - Added `EDXAPP_SWIFT_TEMP_URL_DURATION`
2016-01-25   - Added `EDXAPP_SETTINGS` to allow using a settings file other than `aws.py`. Default: `aws`
2016-01-25   - Renamed `ENABLE_S3_GRADE_DOWNLOADS` to `ENABLE_GRADE_DOWNLOADS`
2016-01-25   - Replaced `EDXAPP_GRADE_STORAGE_TYPE`, `EDXAPP_GRADE_BUCKET` and `EDXAPP_GRADE_ROOT_PATH` with `EDXAPP_GRADE_STORAGE_CLASS` and `EDXAPP_GRADE_STORAGE_KWARGS`
2016-01-25 - Role: openstack
2016-01-25   - Added role
2016-01-25 - Role: vhost
2016-01-25   - Added as dependency for aws and openstack roles. Handles common functionality for setting up VM hosts
2016-01-25 - Role: xqueue
2016-01-25   - Added `XQUEUE_SETTINGS` to specify which settings file to use. Default: `aws_settings`
2016-01-25   - Renamed `XQUEUE_S3_BUCKET` to `XQUEUE_UPLOAD_BUCKET`
2016-01-25   - Renamed `XQUEUE_S3_PATH_PREFIX` to `XQUEUE_UPLOAD_PATH_PREFIX`
2016-01-25 
2015-12-15 - Role: edxapp
2015-12-15   - Removed SUBDOMAIN_BRANDING and SUBDOMAIN_COURSE_LISTINGS variables
2015-12-15 
2015-12-03 - Role: ora
2015-12-03   - Remove the ora1 role as support for it was deprecated in Cypress.
2015-12-03   - Removed dependencies on ora throughout the playbooks / vagrantfiles.
2015-11-12 - Role: edxapp
2015-11-12   - Removed XmlModuleStore from the default list of modulestores for the LMS.
2015-11-12   - EDXAPP_XML_MAPPINGS variable no longer exists by default and is not used by the edxapp role.
2015-11-12 
2015-11-03 - Role: ecommerce
2015-11-03   - Removed ECOMMERCE_ORDER_NUMBER_PREFIX variable
2015-11-03 
2015-09-28 - Role: edxapp
2015-09-28   - All of the following changes are BACKWARDS-INCOMPATABLE:
2015-09-28     - Renamed two top level variables SEGMENT_IO_LMS_KEY and SEGMENT_IO_KEY to SEGMENT_KEY in {lms|cms].auth.json.
2015-09-28     - Renamed two top level variables in roles/edxapp/defaults/main.yml.  EDXAPP_SEGMENT_IO_LMS_KEY and EDXAPP_SEGMENT_IO_KEY are now EDXAPP_LMS_SEGMENT_KEY and EDXAPP_CMS_SEGMENT_KEY respectively
2015-09-28     - REMOVED two top level variables SEGMENT_IO_LMS and SEGMENT_IO from {lms|cms].auth.json. We will use the existence of the SEGMENT_KEY to to serve the same function that these boolean variables served.
2015-09-28     - REMOVED two top level variables EDXAPP_SEGMENT_IO_LMS and EDXAPP_SEGMENT_IO from roles/edxapp/defaults/main.yml.
2015-09-28 
2015-08-17 - Updated ansible fork to be based on ansible 1.9.3rc1 instead of 1.9.1
2015-08-17   - Ansible Changelog: https://github.com/ansible/ansible/blob/stable-1.9/CHANGELOG.md
2015-08-17 
2015-06-17 - Role: rabbitmq
2015-06-17   - Removed the RABBITMQ_CLUSTERED var and related tooling. The goal of the var was to be able to setup a cluster in the aws environment without having to know all the IPs of the cluster before hand.  It relied on the `hostvars` ansible varible to work correctly which it no longer does in 1.9.  This may get fixed in the future but for now, the "magic" setup doesn't work.
2015-06-17   - Changed `rabbitmq_clustered_hosts` to RABBITMQ_CLUSTERED_HOSTS.
2015-06-17 
2015-05-27 - Role: edxapp
2015-05-27   - Removed deprecated variables EDXAPP_PLATFORM_TWITTER_URL, EDXAPP_PLATFORM_MEETUP_URL, EDXAPP_PLATFORM_LINKEDIN_URL, and EDXAPP_PLATFORM_GOOGLE_PLUS_URL in favor of EDXAPP_SOCIAL_MEDIA_FOOTER_URLS.  These variables haven't been used in edx-platform since March 17, 2015 (when https://github.com/edx/edx-platform/pull/7383 was merged).  This change is backwards incompatible with versions of edx-platform from before March 17, 2015.
2015-05-27   - Added EDXAPP_MOBILE_STORE_URLS and EDXAPP_FOOTER_ORGANIZATION_IMAGE variables, used in https://github.com/edx/edx-platform/pull/8175 (v3 version of the edx.org footer).
2015-05-27 
2015-05-27 
2015-05-27   - We now remove the default syslog.d conf file (50-default.conf) this will
2015-05-27   - Added EDXAPP_LMS_AUTH_EXTRA and EDXAPP_CMS_AUTH_EXTRA for passing unique AUTH_EXTRA configurations to the LMS and CMS.
2015-05-11 - Updated ansible fork with small bug fix.
2015-05-11   - https://github.com/ansible/ansible/pull/10957
2015-05-11 
2015-05-07 - Role: edxapp
2015-05-07   - Removed post.txt from the list of files that will have its github urls replaced with git mirror urls.
2015-05-07 
2015-04-29 - Role: edxapp
2015-04-29   - The edxapp role no longer uses checksums to bypass pip installs.
2015-04-29     - pip install will always run for all known requirements files.
2015-04-29 
2015-04-29 - Role: edx-ansible
2015-04-12   - `/edx/bin/update` no longer runs the ansible command with `--tags deploy`
2015-04-12 
2015-03-23 - Role: edxapp
2015-03-23   - Added newrelic monitoring capabilities to edxapp workers. Note that this is a BACKWARDS-INCOMPATABLE CHANGE, as it introduces a new key, `monitor`, to each item in `EDXAPP_CELERY_WORKERS` in `defaults/main.yml`, and plays including this role will fail if that key is not set.
2015-03-23 
2015-03-05 - Role: analytics_api, xqwatcher, insights, minos, edx_notes_api
2015-03-05   - Expanded `edx_service` role to do git checkout and ec2 tagging
2015-03-05   - Refactored roles that depend on `edx_service` to use the new interface: `minos`, `analytics_api`, `insights`, and `xqwatcher`
2015-03-05   - Refactored name from `analytics-api` to `analytics_api`
2015-03-05   - Changed location of minos' config file from `/edx/etc/minos/minos.yml` to `/edx/etc/minos.yml`
2015-03-05   - Added new `edx_notes_api` role for forthcoming notes api
2015-03-05   - This is a __BACKWARDS INCOMPATABLE__ change and will require additional migrations when upgrading an existing server. While we recommend building from scratch, running the following command _might_ work:
2015-03-05       rm -rf /edx/etc/minos
2015-02-06       ```
2015-02-06       rm -rf /edx/app/analytics-api /edx/app/ /edx/app/nginx/sites-available/analytics-api.j2 /edx/app/supervisor/conf.d.available/analytics_api.conf
2015-02-06       ```
2015-02-06 
2015-02-02 - Role: edxapp
2015-02-02   - Enabled combined login registration feature by default
2015-02-02 
2014-12-29 - Role: notifier
2014-12-29   - Refactored `NOTIFIER_HOME` and `NOTIFIER_USER` to `notifier_app_dir` and `notifier_user` to match other roles. This shouldn't change anything since users should've only been overriding COMMON_HOME.
2014-12-29 
2014-12-10 - Role: gitreload
2014-12-10   - New role added for running
2014-12-10     [gitreload](https://github.com/mitodl/gitreload) that can be used
2014-12-10     for importing courses via github/gitlab Web hooks, or more
2014-12-10     generally updating any git repository that is already checked out
2014-12-10     on disk via a hook.
2014-12-10 
2014-12-01 - Role: analytics-api, edxapp, ora, xqueue, xserver
2014-12-01   - Switched gunicorn from using an entirely command argument based
2014-12-01     configuration to usign python configuration files. Variables for
2014-12-01     extra configuration in the configuration file template, and
2014-12-01     command line argument overrides are available.
2014-12-01 
2014-11-13 - Role: analytics-api, insights
2014-11-13   - Using Django 1.7 migrate command.
2014-11-13 
2014-10-15 - Role: edxapp
2014-10-15   - A new var was added to make it easy ot invalidate the default
2014-10-15     memcache store to make it easier to invalidate sessions. Updating
2014-10-15     the edxapp env.json files will result in all users getting logged
2014-10-15     out.  This is a one time penalty as long as the value of `EDXAPP_DEFAULT_CACHE_VERSION`
2014-10-15     is not explicitly changed.
2014-10-15 
2014-09-18 - Role: nginx
2014-09-18   - New html templates for server errors added.
2014-09-18     Defaults for a ratelimiting static page and server error static page.
2014-09-18     CMS/LMS are set to use them by default, wording can be changed in the
2014-09-18     Nginx default vars.
2014-09-18 
2014-09-15 - Role: edxapp
2014-09-15   - We now have an all caps variable override for celery workers
2014-08-28 
2014-08-28 - Role: Edxapp
2014-08-28     Both variables default to EDXAPP_AUTH_EXTRA for backward compatibility
2014-08-22 
2014-08-22 - Role: Mongo
2014-08-22   - Fixed case of variable used in if block that breaks cluster configuration
2014-08-22     by changing mongo_clustered to MONGO_CLUSTERED.
2014-08-20 - Role: common
2014-08-20   break people who have hand edited that file.
2014-08-20 
2014-08-15 - Role: edxapp
2014-08-15   - Updated the module store settings to match the new settings format.
2014-08-15 
2014-08-05 - Update, possible breaking change: the edxapp role vars edxapp_lms_env and edxapp_cms_env have
2014-08-05   been changed to EDXAPP_LMS_ENV and EDXAPP_CMS_ENV to indicate, via our convention,
2014-08-05   that overridding them is expected.  The default values remain the same.
2014-08-05 
2014-06-26 - Role: analytics-api
2014-06-26   - Added a new role for the analytics-api Django app.  Currently a private repo
2014-06-26 
2014-06-26 - Logrotation now happens hourly by default for all logs.
2014-06-26 
2014-06-26   - Basic auth will be turned on by default
2014-06-26 - Update `CMS_HOSTNAME` default to allow any hostname that starts with `studio` along with `prod-studio` or `stage-studio`.
2014-06-11 - Role: xqwatcher, xqueue, nginx, edxapp, common
2014-06-11   - Moving nginx basic authorization flag and credentials to the common role
2014-06-11 
2014-06-02 - Role: Edxapp
2014-06-02   - Turn on code sandboxing by default and allow the jailed code to be able to write
2014-06-02     files to the tmp directory created for it by codejail.
2014-06-02 
2014-05-28 - Role: Edxapp
2014-05-28   - The repo.txt requirements file is no longer being processed in anyway.  This file was removed from edxplatform
2014-05-28     via pull #3487(https://github.com/edx/edx-platform/pull/3487)
2014-05-28 
2014-05-19 
2014-05-19 - Start a change log to keep track of backwards incompatible changes and deprecations.
