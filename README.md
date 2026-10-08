# Exercicios-Dart



Complete os trechos de código abaixo aplicando conceitos avançados do Dart conforme as instruções nos comentários (`// TODO`).

## 1. Interpolação de Strings com Lógica

Você pode executar lógicas complexas e utilizar operadores ternários diretamente dentro da interpolação `${}`.

```dart
String gerarRelatorio(String nome, double? saldo) {
  // TODO: Retorne a string formatada usando UMA ÚNICA interpolação de string.
  // Regras: 
  // 1. Se saldo for nulo, considere-o como 0.0.
  // 2. A string deve ser: "O cliente [nome] está [positivo/negativo/zerado] com R$ [valor]."
  // Ex: Se saldo for -50.0 -> "O cliente João está negativo com R$ -50.0."
  return ''; 
}
```

## 2. Mergulho Profundo em Null Safety e Null-Aware Operators

Combine o acesso condicional (`?.`), o operador de coalescência nula (`??`) e a atribuição condicional (`??=`) em estruturas aninhadas.

```dart
class Endereco {
  String? cep;
}

class Usuario {
  Endereco? endereco;
  String? apelido;
}

String obterCepSeguro(Usuario? usuario) {
  // TODO: Retorne o CEP do usuário. Se o usuário for nulo, ou o endereço for nulo, ou o CEP for nulo, retorne 'CEP Invalido'. Use apenas uma linha.
  return '';
}

void atualizarApelido(Usuario usuario, String novoApelido) {
  // TODO: Atualize o 'apelido' do usuário para 'novoApelido' APENAS SE o apelido atual for nulo. Use o operador correto.
  
}
```

## 3. Coleções Dinâmicas (Spread, Collection If e Collection For)

O Dart permite montar coleções complexas de forma declarativa e dinâmica no momento da criação.

```dart
List<String> construirMenu(bool isPremium, List<String> promocoesAtivas) {
  List<String> menuBase = ['Início', 'Configurações'];
  
  // TODO: Construa e retorne uma nova Lista combinando os seguintes itens usando a sintaxe de coleções do Dart (NÃO use métodos como add() ou addAll()):
  // 1. Todos os itens de 'menuBase' (Use o operador Spread ...).
  // 2. A string 'Área VIP' (Use Collection If: inclua apenas se isPremium for true).
  // 3. O prefixo 'Promo:' seguido de cada item dentro da lista 'promocoesAtivas' (Use Collection For).
  
  return [];
}
```

## 4. Funções de Alta Ordem e Arrow Syntax (`=>`)

A sintaxe de seta brilha quando usada como funções anônimas (callbacks) em métodos de iteração de coleções.

```dart
List<int> processarNumeros(List<int> numeros) {
  // TODO: Usando os métodos .where() e .map() em cadeia, filtre apenas os números pares da lista e, em seguida, multiplique-os por 3.
  // Converta o resultado final de volta para uma lista com .toList().
  // OBRIGATÓRIO: Use a sintaxe de seta (=>) nos callbacks do where e do map.
  return [];
}
```

## 5. Cascatas Aninhadas (`..` e `?..`)

Operadores de cascata são úteis para configurar objetos, inclusive quando eles podem ser nulos (`?..`).

```dart
class Request {
  String url = '';
  String metodo = 'GET';
  Map<String, String> headers = {};
  
  void adicionarHeader(String chave, String valor) {
    headers[chave] = valor;
  }
}

Request? instanciarRequest(bool criar) {
  if (!criar) return null;
  
  // TODO: Instancie o objeto 'Request' e configure-o usando cascatas (..).
  // 1. Altere a url para 'https://api.exemplo.com'
  // 2. Altere o metodo para 'POST'
  // 3. Chame o método 'adicionarHeader' passando 'Authorization' e 'Bearer Token'.
  // Retorne o objeto na mesma expressão.
  return null;
}
```

## 6. Construtores Avançados: Initializer Lists e Factory

Explore a validação antes da construção do corpo e o controle de instâncias.

```dart
class ConfiguracaoSistema {
  final String ambiente;
  final int timeout;
  
  static final ConfiguracaoSistema _instanciaUnica = ConfiguracaoSistema._interno('PROD', 5000);

  // TODO: Crie um construtor nomeado privado chamado '_interno' usando inicializadores (this.ambiente, this.timeout).
  

  // TODO: Crie um construtor 'factory' padrão que sempre retorne a '_instanciaUnica' em vez de criar uma nova instância (Padrão Singleton).
  
}

class Retangulo {
  final double largura;
  final double altura;
  final double area;

  // TODO: Crie um construtor padrão que receba largura e altura, mas calcule e atribua o valor de 'area' (largura * altura) usando uma Initializer List (:).
  
}
```

Fonte para práticas: https://dart.dev/resources/dart-cheatsheet
