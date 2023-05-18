# Resumo da vídeo aula "221 - Threads pt 02 - Estados das threads"

Nesta vídeo aula, o instrutor aborda os estados das threads em programação Java. Ele utiliza exemplos práticos para ilustrar os conceitos e explica como as threads passam de um estado para outro. A seguir, farei um resumo de cada tópico abordado no vídeo:

## Criação e start de threads

O instrutor menciona que é possível criar threads no Java estendendo a classe `Thread` ou implementando a interface `Runnable`. Ambas as abordagens permitem alcançar o mesmo objetivo de execução paralela de código. Ele mostra como criar as threads e iniciar sua execução com o método `start()`.

## Restrição de múltiplos starts

É ressaltado que é proibido chamar o método `start()` mais de uma vez em uma thread. Se isso for feito, ocorrerá uma exceção do tipo `IllegalThreadStateException`. Portanto, uma vez que uma thread é iniciada, não é possível iniciar novamente.

## Execução concorrente e o papel do scheduler

O instrutor explica que quando uma thread é iniciada, não há garantias de que ela será executada imediatamente. O escalonador (scheduler) do sistema operacional é responsável por decidir quando cada thread terá tempo de execução. Ele compara a thread principal (main) a um corredor que executa as linhas de código sequencialmente, mas pode ceder tempo de execução para outras threads. O scheduler pode intercalar a execução das threads de forma não sequencial.

## Exemplo do método `currentThread()`

Um exemplo de código é apresentado para demonstrar o uso do método `currentThread()`, que retorna a instância da thread em execução no momento. Ao imprimir o resultado desse método, pode-se observar o nome e identificador da thread atual.

## Estados das threads

O instrutor descreve os diferentes estados pelos quais uma thread pode passar:

1. **Novo (New)**: Quando a thread é criada, mas ainda não foi iniciada com o método `start()`.
2. **Executável (Runnable)**: Após a chamada do método `start()`, a thread está pronta para ser executada. No entanto, isso não garante que ela esteja em execução no momento, pois depende do scheduler.
3. **Executando (Running)**: Quando o scheduler seleciona a thread para executar, ela passa para o estado de execução.
4. **Esperando (Waiting)**: Uma thread pode entrar nesse estado quando está aguardando alguma condição específica antes de continuar a execução. Pode ser temporário ou por um período de tempo determinado.
5. **Bloqueado (Blocked)**: Uma thread pode ser bloqueada quando está aguardando o acesso a um recurso compartilhado ou quando outra thread está executando uma região crítica de código.
6. **Morto (Dead)**: Quando uma thread conclui sua execução, seja por ter terminado seu código ou por ter ocorrido uma exceção, ela entra no estado de thread morta e não pode ser reiniciada.

## Transições entre estados

O instrutor explica as possíveis transições entre os estados das threads. Uma thread pode ir do estado de "Runnable" para "Running" e, em seguida, voltar para "Runnable" caso seja interrompida ou o scheduler decida dar