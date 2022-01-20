FROM node:14.17.5
WORKDIR /app
#COPY . .
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]

#>docker image build -t conversao-temperatura .
