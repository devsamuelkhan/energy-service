# Step 1: Use an official Node.js image as the base image
FROM node:18

# Step 2: Set the working directory in the container
WORKDIR /app

# Step 3: Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Step 4: Install dependencies
RUN npm install

# Step 5: Copy the rest of the application code to the working directory
COPY . .

# Step 6: Build the React app
RUN npm run build

# # Step 7: Set the environment variable to specify the port
# ENV PORT=3000

# Step 8: Expose the port that the app runs on
EXPOSE 8000

# Step 9: Define the command to run the React app
CMD ["npm", "run", "dev"]
