FROM microsoft/dotnet:1.1.0-sdk-projectjson

RUN mkdir -p /dotnet/app

COPY Controllers Properties Resources appsettings.json Program.cs project.json project.lock.json Startup.cs web.config /dotnet/app/

WORKDIR /dotnet/app

EXPOSE 5001

RUN dotnet restore

ENTRYPOINT ["dotnet", "run"]