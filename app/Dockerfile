FROM microsoft/dotnet:1.1.0-sdk-projectjson

RUN mkdir -p /dotnet/app

COPY Controllers/* /dotnet/app/Controllers/
COPY Properties/* /dotnet/app/Properties/
COPY Resources/* /dotnet/app/Resources/
COPY appsettings.json Program.cs project.json project.lock.json Startup.cs web.config /dotnet/app/

WORKDIR /dotnet/app

EXPOSE 5001

RUN dotnet restore

ENTRYPOINT ["dotnet", "run"]