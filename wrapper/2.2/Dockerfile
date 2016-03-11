FROM cassandra:2.2

# listen to all rpc
RUN sed -ri ' \
              s/^(rpc_address:).*/\1 0.0.0.0/; \
      ' "$CASSANDRA_CONFIG/cassandra.yaml"

# enable PasswordAuthenticator
RUN sed -ri ' \
    s/^(authenticator:).*/\1 PasswordAuthenticator/; \
  ' "$CASSANDRA_CONFIG/cassandra.yaml"

# enable CassandraAuthorizer
RUN sed -ri ' \
    s/^(authorizer:).*/\1 CassandraAuthorizer/; \
  ' "$CASSANDRA_CONFIG/cassandra.yaml"
