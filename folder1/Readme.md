1) Multithreading can be used to make the use of all the cores to the fullest
2) Main thread will not send the request
    - Some other thread will send the request
3) Create multiple servers for different imcoming request
4) Thread t1 = new Thread();

<!-- Code Below for how to implement the thread-->

class MyThread extends Thread {
    
    int []values = {1,2,3,4,5};

    public void run(){
        for(int i=0 ; i < values.length ; i++){
            values[i] = values[i]*2;
        }
    }

}

class MyThread implements Runnable{

}

main(){
    Thread t = new MyThread();
    t.start();

    Runnable r = new MyThread();
    r.start();
}


5) Main thread is there by default, all the exccution will be done by the main thread.
6) For parallel processing we can use the thread 

Runnable obj = new Runnable() {
    public void run(){

    }
}
Theread t = new Thread(obj);
t.start();


Runnable run = () -> {

}
Thread t = new Thread(run);