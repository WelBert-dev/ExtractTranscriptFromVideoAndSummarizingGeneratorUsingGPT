# Resumo da vídeo aula "220 - Threads pt 01 - Introduction" do canal do YouTube "DevDojo"

Nesta vídeo aula, o canal "DevDojo" apresenta uma introdução ao tópico de Threads em Java, abordando os seguintes pontos:

## O que é uma Thread?
- Uma Thread pode ser tanto um objeto do tipo Thread quanto um processo de execução em um programa.
- As Threads são utilizadas para dividir a carga de tarefas em um determinado processo, permitindo a execução simultânea de diferentes partes do código.
- O número de Threads que podem ser utilizadas paralelamente depende do processador e dos núcleos do sistema.

## Tipos de Threads em Java
- Existem dois tipos de Threads em Java: Threads do tipo User e Threads do tipo Daemon.
- As Threads do tipo User são consideradas prioritárias e o programa só termina quando todas as Threads desse tipo são finalizadas.
- As Threads do tipo Daemon são de menor prioridade e geralmente são utilizadas para tarefas de gerenciamento do sistema, como a limpeza de objetos de memória.
- Quando todas as Threads do tipo User são finalizadas, o programa é encerrado, mesmo que ainda haja Threads do tipo Daemon em execução.

## Criando Threads em Java
- Existem duas formas principais de criar Threads em Java: estendendo a classe Thread ou implementando a interface Runnable.
- Ao estender a classe Thread, é necessário sobrescrever o método `run()`, que contém o código a ser executado pela Thread.
- Ao implementar a interface Runnable, é necessário implementar o método `run()` da interface.
- Recomenda-se utilizar a interface Runnable para criar Threads, pois permite maior flexibilidade no compartilhamento de código entre Threads e classes.

Exemplo de criação de uma Thread estendendo a classe Thread:
```java
public class MyThread extends Thread {
    @Override
    public void run() {
        // Código a ser executado pela Thread
    }
}
```

Exemplo de criação de uma Thread implementando a interface Runnable:
```java
public class MyRunnable implements Runnable {
    @Override
    public void run() {
        // Código a ser executado pela Thread
    }
}
```

## Executando Threads em paralelo
- Para iniciar a execução de uma Thread, é necessário chamar o método `start()` em vez de `run()`.
- O método `start()` inicia uma nova Thread e chama o método `run()` da Thread.
- A JVM é responsável pelo escalonamento e controle da execução das Threads, portanto não há garantia da ordem de execução entre as Threads.
- A execução em paralelo é controlada pela JVM, e o tempo de execução de cada Thread pode variar entre as diferentes execuções do programa.

Exemplo de execução de múltiplas Threads em paralelo:
```java
public class Main {
    public static void main(String[] args) {
        Thread t1 = new Thread(new MyRunnable());
        Thread t2 = new Thread(new MyRunnable());
        Thread t3 = new Thread(new MyRunnable());
        Thread t4 = new Thread(new MyRunnable());

        t1.start();
        t2.start();
        t3.start();
        t4.start();
    }
}
```

Nesse exemplo, as Threads `t1`, `t2`, `t3` e `t4` são iniciadas em paralelo, e a ordem de execução não