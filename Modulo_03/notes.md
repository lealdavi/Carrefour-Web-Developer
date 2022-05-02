# Basecamp JS - DIO

## Coleções Chaveadas

Objetivos do Curso:

- Apresentar o objeto map
- Apresentar o objeto set

Estrutura do map:

- É uma coleção de arrays no formato [chave, valor];
- Pode ser iterado por um loop for...of

Os métodos mais comuns são:

Adicionar - myMap.set('apple', 'fruit');

Ler - myMap.get('apple');

Deletar - myMap.delete('apple')

Map vs Objeto

- Maps podem ter chaves de qualquer tipo
- Maps possuem a propriedade length
- Maps são mais fáceis de iterar
- Utilizado quando o valor das chaves é desconhecido
- Os valores tem o mesmo tipo

Estrutura do **set**:

Sets são estruturas que armazenam apenas valores únicos. Sets tem algumas propriedades e métodos bem diferentes de um array.

Set vs Array:

- Possui valores únicos
- Em vez da propriedade length, consulta-se o número de registros pela propriedade size;
- Não possui os métodos map, filter, reduce, etc.