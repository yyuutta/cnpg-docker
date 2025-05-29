# ベースイメージとしてPostgreSQLを使用
FROM ghcr.io/cloudnative-pg/postgresql:15.8
#FROM ghcr.io/cloudnative-pg/postgresql:16.3

User root

# PostGISのインストール
RUN set -xe; \
        apt-get update; \
        apt-get install -y --no-install-recommends \
                "postgresql-15-postgis-3" ; \
#                "postgresql-16-postgis-3" ; \
        rm -fr /tmp/* ; \
        rm -rf /var/lib/apt/lists/*;

# pg_hint_plan
RUN set -xe; \
        apt-get update; \
        apt-get install -y --no-install-recommends \
                "postgresql-15-pg-hint-plan" ; \
#                "postgresql-16-pg-hint-plan" ; \
        rm -fr /tmp/* ; \
        rm -rf /var/lib/apt/lists/*;

#pg_repack
RUN set -xe; \
        apt-get update; \
        apt-get install -y --no-install-recommends \
                "postgresql-15-repack" ; \
#                "postgresql-16-repack" ; \
        rm -fr /tmp/* ; \
        rm -fr /var/lib/apt/lists/*;

USER postgres
