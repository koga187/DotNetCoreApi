## First project with .netCore.

Initialized with the global.json to set the dotnet version the poroject must use.

### To generate the global.json file use the dotnet CLI bellow:

    $ dotnet new globaljson

Then you can set the version you want to use, be carefull you must have this sdk selected at your PC, you can check if the version is installed with the command bellow:

    $ dotnet --list-sdks

## Como criar a solution ```src/NetCoreApi.sln```

Dentro da pasta ```src``` você vai digitar o comando abaixo sendo que após o parametro de --name é o nome da solution que pode ser o que você desejar.

    $ dotnet new sln --name NetCoreApi

## Como criar uma aplicação de webapi ```src/Api.Application\application.csproj```

Dentro da pasta ```src``` rodar o comando abaixo para criar o projeto de webapi em C#

    $ dotnet new webapi -n application -o Api.Application --no-https

O parametros:

    - -n é para o nome da webapi;
    - -o é a pasta de output dos arquivos de base do projeto;
    - --no-https é para ambientes de testes que não precisam rodar em ssl, o protocolo de segurança HTTP.

## Como referenciar sua aplicação na sua solution

Dentro da pasta src digitar o comando abaixo:

    $ dotnet sln add .\Api.Application\
