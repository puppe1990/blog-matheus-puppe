## Como usar FactoryBot no Console Rails

Comece usando o ambiente de teste em modo sandbox.

```
rails console -e test --sandbox
```

Então no console chame o FactoryBot

```
require 'factory_bot'
```

Chame as definições de factory

```
FactoryBot.find_definitions
```

Chama os metódos do FactoryBot

```
include FactoryBot::Syntax::Methods

```


Pronto agora você poderá criar as factories direto no console Rails.🤜🏻🤛🏻