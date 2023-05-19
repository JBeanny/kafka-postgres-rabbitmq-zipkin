# Authentication for pgadmin 
    postgres:
    container_name: postgres
    image: postgres
    environment:
      POSTGRES_USER: <YOUR-USERNAME>
      POSTGRES_PASSWORD: <YOUR-PASSWORD>
      PGDATA: /data/postgres
    volumes:
      - postgres:/data/postgres
    ports:
      - "5432:5432"
    networks:
      - postgres
    restart: unless-stopped