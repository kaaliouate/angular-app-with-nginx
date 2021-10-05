# Create image from file:
  docker build -t khalidaaliouate/angular-app-image:0.1 .

# Create container from image:
  docker run --name angular-app-container -d -p 8080:80 khalidaaliouate/angular-app:0.1