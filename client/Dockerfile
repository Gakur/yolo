#Define base image
FROM node:alpine


#Define working directory
WORKDIR /app


#Copy package.json and package-lock.json to the working directory
COPY package*.json . /


#Install Dependencies
RUN npm install 


#Copy the rest of the app to the working directory
COPY . .


#Expose the port
EXPOSE 3000


#Define entry point
CMD [ "npm", "start" ]