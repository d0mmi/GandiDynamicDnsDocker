FROM mcr.microsoft.com/dotnet/runtime:8.0

# Install dependencies
RUN apt-get update && apt-get install -y wget unzip && rm -rf /var/lib/apt/lists/*

# Create the application directory
RUN mkdir -p /app/download
RUN mkdir -p /app/unzip

# Download the release zip file
RUN wget https://github.com/Aldaviva/GandiDynamicDns/releases/latest/download/GandiDynamicDns-linux-arm64.zip -O /app/download/app.zip

# Unzip the downloaded file
RUN unzip /app/download/app.zip -d /app/unzip

RUN mv /app/unzip/gandidynamicdns /app/gandidynamicdns

# Make the executable file executable
RUN chmod 777 /app/gandidynamicdns

# Clean up
RUN rm -rf /app/download
RUN rm -rf /app/unzip

# Set working directory
WORKDIR /app

# Run the application
CMD ["./gandidynamicdns"]