
# Comandos úteis
Comandos de diferentes tecnologias que são úteis mas que nem sempre estão presentes no dia a dia 😁
## Comandos .Net
Caso seja necessário executar as migrations em um ambiente específico. No exemplo, as migrations estão sendo executadas no ambiente de produção.
```bash
Update-Database -Args '--environment Production'
```
Ao gerar migrations em soluções que possuem vários projetos, é necessário informar ao Entity Framework, qual é o projeto principal da solução e em qual projeto ele deve gerar a migration.
Nesse exemplo, a migration será gerada no projeto de "Infra", sendo que o projeto de inicialização é o "API".
```bash
dotnet ef migrations add NomeDaMigration --project Infra/Infra.csproj --startup-project API/API.csproj
```

## Comandos Angular
Para criar um projeto Angular sem o conceito de "Standalone"
```bash
ng new nome-projeto --no-standalone
```
