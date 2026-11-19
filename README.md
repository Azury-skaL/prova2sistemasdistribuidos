# Prova-B2---Sistemas-Distribui-dos

Aluno: Rafael Felipe Zambeli
5º Semestre

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

Evidencia - 4 - Validação do programa

PS C:\Users\aluno\Desktop\simulado_distribuidos> python central_pedidos.py
=== CENTRAL DE PEDIDOS ===
Limite simultâneo: 2
Estoque inicial: 10
Pedidos confirmados: [101, 102, 103]
Estoque principal: 7
Réplica antes: 7
Réplica depois: 7
Consulta após falha: REPLICA 7

Evidencia - 5 - Tolerancia a falhas
PS C:\Users\aluno\Desktop\simulado_distribuidos> python central_pedidos.py
=== CENTRAL DE PEDIDOS ===
Limite simultâneo: 2
Estoque inicial: 10
Pedidos confirmados: [101, 102, 103]
Estoque principal: 7
Réplica antes: 7
Réplica depois: 7
Consulta após falha: REPLICA 7

Questão 1. Qual é a função do semáforo no processamento dos pedidos?
O semáforo (threading.Semaphore) serve para controlar quantas threads podem executar determinada parte do processamento simultaneamente.

Questão 2. Por que é necessário sincronizar os dados entre o servidor principal e a réplica?
Para garantir que os dois servidores tenham as mesmas informações e que a réplica possa continuar funcionando caso o principal falhe.


Questão 3. O que significa tolêrancia a falhas e como ela aparece neste programa?
É a capacidade do sistema de continuar funcionando mesmo quando ocorre uma falha. No programa, isso acontece quando o servidor principal fica offline e a réplica assume as consultas.


Questão 4. Para que server o Lock no programa e como o controle de acesso aos recursos ajuda a prevenir problemas de concorrência?
O Lock serve para permitir que apenas uma thread por vez altere o estoque, evitando que dois pedidos modifiquem o mesmo valor ao mesmo tempo e causem erros.


Questão 5. Considerando a sequência de eventos, a sincronização do estoque deve acontecer antes ou depois do processamento dos pedidos? Explique a relação de causalidade.
A sincronização deve acontecer depois de cada pedido ser processado, pois primeiro o estoque do servidor principal é atualizado e depois esse novo valor é enviado para a réplica.

Conclusão:
Nessa prova eu aprendi a montar e fazer as devidas manutenções em um sistema de comércio eletrônico que utiliza um sistema para controlar o processamento de pedidos, onde um havia um servidor e uma réplica para manter cópias das informações.
