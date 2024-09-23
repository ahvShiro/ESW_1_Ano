#ESW 

> [!callout] São restrições do negócio sobre COMO algo vai ser feito
> Ex.: Taxas, descontos, condições

> [!callout] Regra de negócio 🤝 Requisito funcional

- ***Sempre é uma condicional***
	- se, caso, quando, deve, pode, somente, obrigatório, sempre
## 🥥 Vender coco na praia
- Coco somente será entregue aos clientes que realizarem pagamento
- Somente será aceito pagamento em dinheiro
- Clientes que comprarem 4 cocos ganham 1 de graça. Essa promoção não tem término


> [!warning] Cuidados com palavras extremas
> - Todos, extremamente,


## Exercício
- Verificação de disponibilidade
	- Caso um pedido de reserva seja realizado pelo cliente, o sistema verificará a existência de quartos disponíveis no período informado pelo usuário.
- Dados para a reserva
	- Após a verificação de disponibilidade, se houver quartos disponíveis, solicitar nome, endereço e telefone do cliente.
- Cancelamento da reserva
	- Caso o pagamento não seja efetuado pelo cliente em até três dias antes da data prevista de entrada, a reserva é cancelada.
- Impressão de relatório
	- As 00:00 de cada dia, disponibilizar um relatório em PDF de todas as reservas que foram canceladas no dia anterior.
