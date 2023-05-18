# Resumo da vídeo aula "221 - Threads pt 02 - Estados das threads"

Nesta vídeo aula do canal "DevDojo" sobre programação e desenvolvimento backend com Java, o instrutor aborda os estados das threads em Java. O objetivo é entender como as threads se comportam e quais são os possíveis estados em que uma thread pode se encontrar durante a execução.

## Estados das threads
Os estados das threads em Java são os seguintes:

1. **Novo (New)**: Quando uma thread é criada, ela entra no estado "novo". Nesse estado, a thread foi instanciada, mas ainda não foi iniciada.

2. **Executável (Runnable)**: Após chamar o método `start()` em uma thread, ela entra no estado "executável" ou "runnable". Nesse estado, a thread está pronta para ser executada, mas não necessariamente está sendo executada. O escalonador do sistema operacional decide quando a thread será executada.

3. **Executando (Running)**: Quando a thread é selecionada pelo escalonador e está sendo executada ativamente, ela está no estado "executando". Nesse estado, o código da thread está sendo processado.

4. **Esperando (Waiting)**: Uma thread pode entrar no estado "esperando" quando aguarda por algum evento externo ou condição para continuar a execução. Ela pode ser temporariamente suspensa e colocada em espera até que a condição seja atendida.

5. **Bloqueado (Blocked)**: Uma thread pode entrar no estado "bloqueado" quando está esperando pelo monitor (ou lock) de um objeto para realizar uma operação. Isso acontece quando a thread tenta adquirir um lock que está sendo mantido por outra thread.

6. **Morto (Dead)**: Quando uma thread completa sua execução ou é encerrada de forma abrupta, ela entra no estado "morto". Uma vez que uma thread está morta, não pode ser reiniciada ou reutilizada. Um novo objeto thread precisa ser criado para iniciar uma nova thread.

É importante notar que uma thread pode transitar entre diferentes estados ao longo de sua execução, dependendo do contexto e das ações realizadas.

## Exemplos de implementação
Na vídeo aula, são apresentados exemplos de criação de threads e a transição entre os estados. Os exemplos demonstram o uso das classes `Thread` e `Runnable` em Java.

```java
// Exemplo de criação de uma thread estendendo a classe Thread
public class MinhaThread extends Thread {
    public void run() {
        // Código da thread
    }
}

// Exemplo de criação de uma thread implementando a interface Runnable
public class MinhaRunnable implements Runnable {
    public void run() {
        // Código da thread
    }
}

public class Main {
    public static void main(String[] args) {
        Thread thread1 = new MinhaThread();
        Thread thread2 = new Thread(new MinhaRunnable());

        thread1.start();
        thread2.start();
    }
}
```

No exemplo acima, são criadas duas threads: uma estendendo a classe `Thread` (classe `MinhaThread`) e outra implementando a interface `Runnable` (classe `MinhaRunnable`). Ambas as classes possuem um método `run()` onde o código da thread é definido. Em seguida, as threads são iniciadas chamando o método `start()`. Isso faz com que as threads