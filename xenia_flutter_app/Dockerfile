# Use the latest Flutter image with Dart 3.x
FROM ghcr.io/cirruslabs/flutter:latest

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

# Set up a command to run the Flutter app, binding to all network interfaces
CMD ["flutter", "run", "--web-port", "8080", "--web-hostname", "0.0.0.0", "-d", "web-server"]
