
INSERT INTO CLIENTE (NOME, EMAIL, NUMERO) VALUES
('Saimon', 'saimon@senac', 123213),
('Paula','paula@senac',11924562544),
('Maria','maria@senac',11931446235);

select id_cliente, nome, email, numero from cliente order by nome asc;



INSERT ALL
  INTO PRODUTOS (nome, preco, tipo) VALUES ('Notebook X', 3000, 'Notebook')
  INTO PRODUTOS (nome, preco, tipo) VALUES ('Notebook Y', 3500, 'Notebook')
  INTO PRODUTOS (nome, preco, tipo) VALUES ('Celular Z', 2000, 'Celular')
SELECT 1 FROM dual;

COMMIT;

-
UPDATE PRODUTOS
SET preco = preco * 1.10
WHERE tipo = 'Notebook';

COMMIT;

SELECT * FROM PRODUTOS;


INSERT ALL
  INTO PEDIDOS (cliente_id, produto_id, status) VALUES (1, 1, 'ABERTO')
  INTO PEDIDOS (cliente_id, produto_id, status) VALUES (2, 2, 'CANCELADO')
  INTO PEDIDOS (cliente_id, produto_id, status) VALUES (3, 3, 'FINALIZADO')
  INTO PEDIDOS (cliente_id, produto_id, status) VALUES (1, 2, 'CANCELADO')
SELECT 1 FROM dual;

COMMIT;


DELETE FROM PEDIDOS
WHERE status = 'CANCELADO';

COMMIT;

SELECT * FROM PEDIDOS;




INSERT ALL
  INTO CLIENTES_STG (nome, email) VALUES ('Ana P. Atualizada', 'ana@techplus.com') -- já existe
  INTO CLIENTES_STG (nome, email) VALUES ('Daniela Nova', 'daniela@techplus.com') -- novo
SELECT 1 FROM dual;

COMMIT;
