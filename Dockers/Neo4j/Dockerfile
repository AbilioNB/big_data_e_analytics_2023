# Use a imagem oficial do Neo4j como base
FROM neo4j:latest

# Instale o utilitário git
RUN apt-get update && apt-get install -y git

# Clone o repositório do GitHub com as bases de dados necessárias
RUN git clone https://github.com/AbilioNB/big_data_e_analytics_2023.git /var/lib/neo4j/import

# Defina um diretório de trabalho padrão
WORKDIR /var/lib/neo4j

# Exponha a porta padrão do Neo4j (7687)
EXPOSE 7687

# Exponha a porta para a interface da web do Neo4j (7474)
EXPOSE 7474

# Defina as variáveis de ambiente para login e senha
ENV NEO4J_AUTH=your_username/your_password

# Inicie o Neo4j
CMD ["neo4j"]
