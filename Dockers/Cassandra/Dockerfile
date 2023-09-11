# Imagem oficial do Cassandra como base
FROM cassandra:latest

# Instale o git
RUN apt-get update && apt-get install -y git

# Crie um diretório para armazenar as bases de dados
RUN mkdir -p /cassandra_data

# Clone o repositório do GitHub
WORKDIR /cassandra_data
RUN git clone https://github.com/AbilioNB/big_data_e_analytics_2023.git .

# Defina as variáveis de ambiente para login e senha
ENV CASSANDRA_USER=your_username
ENV CASSANDRA_PASSWORD=your_password

# Exponha a porta padrão do Cassandra 
EXPOSE 9042

# Inicie o serviço
CMD ["cassandra", "-f"]
