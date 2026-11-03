1. Cliente
id_cliente — SERIAL PRIMARY KEY
nome — VARCHAR(100)
telefone — VARCHAR(11)
endereco — VARCHAR(200)

2. Bolo
id_bolo — SERIAL PRIMARY KEY
sabor — VARCHAR(100)
valor — NUMERIC(10,2)
descricao — TEXT

3. Encomenda
id_encomenda — SERIAL PRIMARY KEY
data_encomenda — DATE
observacoes — TEXT
situacao_pagamento — ENUM(pagamento)
forma_pagamento — ENUM(forma')
acrescimo — NUMERIC(10,2)
valor_total — NUMERIC(10,2)
id_cliente — INTEGER FOREIGN KEY
id_bolo — INTEGER FOREIGN KEY


Relacionamentos
Cliente — Encomenda (1:N): um cliente pode realizar várias encomendas, mas cada encomenda pertence a um único cliente.
Bolo — Encomenda (1:N): um tipo de bolo pode estar presente em várias encomendas, mas cada encomenda está associada a um bolo.

