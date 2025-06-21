# Use the AWS Lambda Node.js 18 base image
FROM public.ecr.aws/lambda/nodejs:18

# Set working directory inside the container
WORKDIR /var/task

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the application files
COPY . .

# Set the Lambda handler file and export
CMD ["patient-service.handler"]
