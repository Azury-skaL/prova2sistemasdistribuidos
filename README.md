# Prova-B2---Sistemas-Distribui-dos

Evidencia - 1 - Primeira saída no terminal

PS C:\Users\aluno\Desktop\simulado_distribuidos> python central_pedidos.py
=== CENTRAL DE PEDIDOS ===
Limite simultâneo: 3
Estoque inicial: 10
Pedidos confirmados: [101, 102, 103]
Estoque principal: 7
Réplica antes: 10
Réplica depois: 7
Consulta após falha: REPLICA 7


Evidencia - 2 - Alteração do limite simultaneo para 2

PS C:\Users\aluno\Desktop\simulado_distribuidos> python central_pedidos.py
=== CENTRAL DE PEDIDOS ===
Limite simultâneo: 2
Estoque inicial: 10
Pedidos confirmados: [101, 102, 103]
Estoque principal: 7
Réplica antes: 10
Réplica depois: 7
Consulta após falha: REPLICA 7

Evidencia 3 - Replica após sincronização

PS C:\Users\aluno\Desktop\simulado_distribuidos> python central_pedidos.py
=== CENTRAL DE PEDIDOS ===
Limite simultâneo: 2
Estoque inicial: 10
Pedidos confirmados: [101, 102, 103]
Estoque principal: 7
Réplica antes: 7
Réplica depois: 7
Consulta após falha: REPLICA 7

Evidencia - 4 - 
