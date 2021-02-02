# Use official docker image and define the maintainer
FROM  mongo:4.4
LABEL maintainer="darren.gruber@mongodb.com"

# Install some OS package I need
RUN apt update \
 && apt install figlet \
 && apt clean

# Add sample data to our database
ENV  MONGO_INITDB_DATABASE="data"
COPY add_sample_data.js /docker-entrypoint-initdb.d/add_sample_data.js

