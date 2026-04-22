instalar o pacote do Swagger:
clique com o botão direito no projeto no Gerenciador de Soluções > Gerenciar Pacotes NuGet. Depois, em Origem do pacote, escolha nuget.org, pesquise por Swashbuckle.AspNetCore, selecione o pacote e clique em Instalar.

exemplo de modelo no Progam.cs para rodar em Swagger:

var builder = WebApplication.CreateBuilder(args);

builder.Services.AddControllers();
builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen();

var app = builder.Build();

app.UseSwagger();
app.UseSwaggerUI();

app.MapControllers();

app.Run();

configurar o LaunchSettings.json para abrir em Swagger:
adicionar ("launchUrl": "swagger",) para abrir em Swagger
