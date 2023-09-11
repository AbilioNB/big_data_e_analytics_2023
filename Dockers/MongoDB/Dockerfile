# Imagem oficial do MongoDB como base
FROM mongo:latest

# Instale o git
RUN apt-get update && apt-get install -y git

# Clone o repositório do GitHub
RUN git clone https://github.com/AbilioNB/big_data_e_analytics_2023.git /data/db

# Defina um diretório de trabalho padrão
WORKDIR /data/db

# Exponha a porta padrão do MongoDB 
EXPOSE 27017

# Inicie o serviço
CMD ["mongod"]
