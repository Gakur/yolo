#Define base image
FROM node:alpine


#Define working directory
WORKDIR /usr/src/app/client


#Copy package.json and package-lock.json to the working directory
# COPY package*.json . /
COPY . .

#Install Dependencies
# RUN npm install 
RUN npm install

#Copy the rest of the app to the working directory
# COPY . .
FROM node

RUN npm run: build

WORKDIR /app

COPY --from=build /app/build .

#Expose the port
# EXPOSE 5000


#Define entry point
CMD [ "start", "-p", "5000", "-s", "." ]