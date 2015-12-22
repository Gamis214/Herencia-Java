# Herencia Java
Ejemplo aplicando Herencia en Java

##Ejemplo
La **Herencia** se utiliza para no repetir parametros en diferentes clases. Un ejemplo de ello es el siguiente ejercicio que 
nos ayudara a entender mejor como es que podemos **HEREDAR** propiedades de otra clase sin necesidad de volverlos a repetir, el siguiente
diagrama nos ayudara a entender mejor el ejemplo:

![Diagrama Herencia](http://oi57.tinypic.com/ou1dow.jpg)

Tenemos nuestra **Clase Padre** llamada:
* Animal

Y 3 **Clases Hijas** llamadas:
* Perro
* Caballo
* Gato

Cada una de las clases hijas tiene diferente raza, pero comparten las mismas propiedades de un **Animal** para ello crearemos nuestra clase
Padre Animal:

##Clase Padre (Animal)
```java
public class Animal {

    private String nombre,tipo_alimentacion;
    private int edad;

    public Animal(String nombre,String tipo_alimentacion,int edad){
        this.nombre = nombre;
        this.tipo_alimentacion = tipo_alimentacion;
        this.edad = edad;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public String getTipo_alimentacion() {
        return tipo_alimentacion;
    }

    public void setTipo_alimentacion(String tipo_alimentacion) {
        this.tipo_alimentacion = tipo_alimentacion;
    }

    public int getEdad() {
        return edad;
    }

    public void setEdad(int edad) {
        this.edad = edad;
    }
}
```
A continuacion creamos nuestras clases hijas.

##Clase Hija (Perro)
```java
public class Perro extends Animal {

    private String raza;

    public Perro(String nombre,String tipo_alimentacion,int edad,String raza){
        super(nombre,tipo_alimentacion,edad);
        this.raza = raza;
    }

    public String getRaza() {
        return raza;
    }

    public void setRaza(String raza) {
        this.raza = raza;
    }

    public void mostrar(){
        System.out.println(getNombre() + "-"+getTipo_alimentacion()+"-"+getEdad()+"-"+getRaza());
    }
}
```

##Clase Hija (Gato)
```java
public class Gato extends Animal {

    String raza;

    public Gato(String nombre, String tipo_alimentacion, int edad, String raza) {
        super(nombre, tipo_alimentacion, edad);
        this.raza = raza;
    }

    public String getRaza() {
        return raza;
    }

    public void setRaza(String raza) {
        this.raza = raza;
    }

    public void mostrar(){
        System.out.println(getNombre() + "-"+getTipo_alimentacion()+"-"+getEdad()+"-"+getRaza());
    }
}
```
##Clase Hija (Caballo)
```java
public class Caballo extends Animal {

    String raza;

    public Caballo(String nombre, String tipo_alimentacion, int edad,String raza) {
        super(nombre, tipo_alimentacion, edad);
        this.raza = raza;
    }

    public String getRaza() {
        return raza;
    }

    public void setRaza(String raza) {
        this.raza = raza;
    }

    public void mostrar(){
        System.out.println(getNombre() + "-"+getTipo_alimentacion()+"-"+getEdad()+"-"+getRaza());
    }
}
```
Una vez realizadas nuestras clases estructuramos el **Main** para crear los **Objetos** de cada uno de nuestras clases hijas y asignarles 
las propiedades necesarias

##Clase Main
```javascript
public class Main {

    public static void main(String[] args) {

        Perro perro = new Perro("Teddy","Croquetas",10,"Chihuahua");
        Gato gato = new Gato("Pelusa","Especial",8,"Siames");
        Caballo caballo = new Caballo("Jhonny","Pasto",21,"Fino");

        //-->Nos muestra los detalles del objeto
        perro.mostrar();
        System.out.println("--------------------------------------------------");
        gato.mostrar();
        System.out.println("--------------------------------------------------");
        caballo.mostrar();

    }
}
```

Al ejecutar el codigo **Main** nos debe arrojar el siguiente resultado:
```
Teddy-Croquetas-10-Chihuahua
--------------------------------------------------
Pelusa-Especial-8-Siames
--------------------------------------------------
Jhonny-Pasto-21-Fino
```


