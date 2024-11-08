# Use the official Flutter image
FROM cirrusci/flutter:latest

# Set the working directory in the container
WORKDIR /app

# Copy only the necessary files to cache dependencies effectively
COPY pubspec.yaml pubspec.lock ./

# Install Flutter dependencies
RUN flutter pub get

# Copy the rest of the application files
COPY . .

# Expose necessary ports (e.g., for web, debugging, or dev tools)
EXPOSE 8080 9000

# Install additional tools if needed (e.g., bash, vim, etc.)
RUN apt-get update && apt-get install -y nano

# Set up a command to keep the container running if needed
CMD ["flutter", "pub", "get"]
