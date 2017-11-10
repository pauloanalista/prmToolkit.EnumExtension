# prmToolkit

# EnumExtension
Classe responsável por adicionar novos recursos ao Enum.
A partir da versão 2.0 do pacote Nuget, o projeto foi migrado para .Net Standard 2.0

### Installation - EnumExtension

Para instalar, abra o prompt de comando Package Manager Console do seu Visual Studio e digite o comando abaixo:

Para adicionar somente a referencia da dll
```sh
Install-Package prmToolkit.EnumExtension
```
### Recursos disponíveis
- GetDescription (obtém a descrição do enum)
- ToEnum (Obtém o Enum através do nome passado)
- GetAttribute (Obtém o atributo customizado do enum)
- IsEnumValid(Validar se o valor que está no Enum foi definido corretamente)
- IsEnumValid(Validar se o valor inteiro pertence a um Enum especifico)


### Alguns exemplos
```sh
//Exemplo de Enum
public enum EnumAtuacao
{
    [Description("Responsável por dirigir o veículo")]
    Motorista = 0,
    [Description("Responsável por cobrar a passagem")]
    Cobrador = 1,

    Despachante = 2,

    Fiscal = 3,

    MonitorDePonto = 4
}
    
    
public void Exemplo(){
  //Para obter a descrição que foi definida nas anotações do Enum
  string nomeDoAtributoDaAtuacao = atuacao.GetDescription();
}


public Inserir(EnumAtuacao atuacao, DateTime dataDeContratacao)
{
    //Verifica se o valor que foi passado por parametro no Enum existe dentro das definições do EnumAtuacao
    bool enumValido = atuacao.IsEnumValid();

    //É possível testar se um inteiro contém dentro da definição de um Enum
    int valor = 99;
    bool enumValido = valor.IsEnumValid<EnumAtuacao>();
}
```        
