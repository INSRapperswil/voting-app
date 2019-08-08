# Using official dotnet base image
# FROM microsoft/dotnet:2.0.0-sdk
FROM mcr.microsoft.com/dotnet/core/sdk:2.2

# Set the application directory
RUN mkdir -p /code
WORKDIR /code

# Copy our code from the current src folder to /code/src/Worker inside the container
ADD src/Worker /code/src/Worker

# Install our dotnet dependencies
RUN dotnet restore -v minimal src/Worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 

# Define our default command to be run when launching the container
CMD ["dotnet", "src/Worker/Worker.dll"]