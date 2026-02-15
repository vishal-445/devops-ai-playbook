FROM postgres:15-alpine

# Environment variables
ENV POSTGRES_DB=boutique_db
ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=postgres123

# Copy database dump file (will be loaded automatically on first run)
COPY boutique_full.sql /docker-entrypoint-initdb.d/

# Make sure the dump is executable
RUN chmod 644 /docker-entrypoint-initdb.d/boutique_full.sql

# Expose default PostgreSQL port
EXPOSE 5432
