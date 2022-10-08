FROM ******************/dotnet/dotnet-sdk-sonar:5.0 AS build

WORKDIR /app


COPY . ./

RUN dotnet restore

RUN dotnet publish -c Release -o out


FROM ************/dotnet/dotnet-aspnet-runtime:5.0

WORKDIR /app
EXPOSE 8080

COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "Home.dll"]