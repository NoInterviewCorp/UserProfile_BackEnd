FROM microsoft/dotnet:sdk AS build-env
COPY . /app
WORKDIR /app
# Copy csproj and restore as distinct layers
# COPY *.csproj ./
# Copy everything else and build
# COPY . ./
RUN chmod +x ./wait-for-it.sh
RUN chmod +x ./entrypoint.sh
RUN ["dotnet", "restore"]
RUN ["dotnet", "build"] 
EXPOSE 5004
CMD /bin/bash ./entrypoint.sh
