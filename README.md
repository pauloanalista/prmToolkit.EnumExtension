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
