# Resumo da vídeo aula "221 - Threads pt 02 - Estados das threads"

Nesta vídeo aula do canal do YouTube "DevDojo", o instrutor aborda os estados das threads em programação Java. A aula se baseia em um exemplo anterior, onde foram criadas duas classes, uma estendendo a classe Thread e a outra implementando a interface Runnable. Essas classes são usadas para criar e iniciar threads. 

O instrutor destaca algumas informações importantes sobre os estados das threads:

1. Não é possível chamar o método `start()` duas vezes na mesma thread. Se isso ocorrer, será lançada uma exceção chamada `IllegalThreadStateException`.
2. A thread principal, chamada de `main`, é executada sempre que o programa é iniciado.
3. As threads são como corredores em uma corrida. A thread principal executa seu código sequencialmente e pode iniciar outras threads.
4. O scheduler, que é responsável pelo gerenciamento das threads, pode decidir intercalar a execução entre as threads. Isso significa que a ordem em que as threads são executadas pode não ser necessariamente a ordem em que foram iniciadas.
5. Quando a thread principal morre, ou seja, termina sua execução, as outras threads ainda podem continuar sendo executadas. O programa só é encerrado quando todas as threads de usuário (as threads criadas pelo programa) terminam.
6. Os estados possíveis de uma thread são: novo (new), executável (runnable), em execução (running), esperando (waiting), bloqueada (blocked) e morta (dead).
7. Uma thread é criada no estado novo (new) quando o objeto correspondente é criado.
8. Ao chamar o método `start()` na thread, ela passa para o estado executável (runnable), onde está pronta para ser executada pelo scheduler. Porém, isso não garante que a thread será imediatamente executada.
9. A thread pode voltar do estado de execução (running) para o estado executável (runnable) ou pode ser bloqueada (blocked).
10. Uma thread pode ser bloqueada por motivos como aguardar um recurso ou entrar em um estado de espera por um determinado tempo. No entanto, uma thread bloqueada sempre volta para o estado executável (runnable) quando a condição de bloqueio é liberada.
11. Quando uma thread termina sua execução, ela entra no estado morta (dead). Uma thread morta não pode ser reiniciada ou reutilizada.

É importante destacar que o instrutor menciona que as threads do exemplo não estão sendo bloqueadas, apenas alternam entre os estados executável (runnable) e em execução (running).

## Ressalvas sobre informações inconsistentes:

- Durante o vídeo, o instrutor menciona que uma thread bloqueada sempre volta para o estado executável (runnable) quando a condição de bloqueio é liberada. Entretanto, isso não é totalmente correto. Uma thread bloqueada pode voltar para o estado executável ou esperando (waiting), dependendo do método que foi chamado para bloqueá-la e das condições especificadas.

Este resumo fornece uma visão geral dos tópicos abordados na vídeo aula sobre os estados das threads em Java. É importante assistir ao vídeo completo para obter mais detalhes e exemplos práticos relacionados aos conceitos discutidos.