**Neide**

### 1\. Cliente

* id\_cliente — SERIAL PRIMARY KEY  
* nome — VARCHAR(100)  
* telefone — VARCHAR(11)  
* endereco — VARCHAR(200)

### 2\. Bolo

* id\_bolo — SERIAL PRIMARY KEY  
* sabor — VARCHAR(100)  
* valor — NUMERIC(10,2)  
* descricao — TEXT

### 3\. Encomenda

* id\_encomenda — SERIAL PRIMARY KEY  
* data\_encomenda — DATE  
* observacoes — TEXT  
* situacao\_pagamento — ENUM(pagamento)  
* forma\_pagamento — ENUM(forma')  
* acrescimo — NUMERIC(10,2)  
* valor\_total — NUMERIC(10,2)  
* id\_cliente — INTEGER FOREIGN KEY  
* id\_bolo — INTEGER FOREIGN KEY

## Relacionamentos

* Cliente — Encomenda (1:N): um cliente pode realizar várias encomendas, mas cada encomenda pertence a um único cliente.  
* Bolo — Encomenda (1:N): um tipo de bolo pode estar presente em várias encomendas, mas cada encomenda está associada a um bolo.
  <img width="1201" height="682" alt="image" src="https://github.com/user-attachments/assets/620bd38f-e2e2-4f9d-b15b-159a39cb4313" />
