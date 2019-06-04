# simple-tasks-on-JAVA.Task-4
Создать класс Годзила. У данного класса должно быть свойство - объем желудка. Написать для данного класса функцию поедания людей. В данную функцию должен передаваться объем съеденного и соответственно уменьшаться место в желудке. Когда Годзила заполнит желудок на 90%, функция должна выводить надпись, что Годзила наелся и больше не может поедать людей.
package Practice;

public class Godzila {

    private static float STOMACH;
    private float value;
    private final float SIZE = 100;
    private float man;

    public Godzila(int man) {
        value = STOMACH + man;
        System.out.println("Желудок заполнен на " + value+" %");
    }


    public void eat(int man) {
        value += man;
        if (value < 0.9*SIZE) {
            System.out.println("Желудок заполнен на " + value+" %");
        } else if (value >= 0.9*SIZE) {
            System.out.println("Желудок заполнен на " + value+" %");
            System.out.println("Годзила наелся и больше не может поедать людей!");
        }
    }
}

package Practice;

public class Main {
    public static void main(String[] args) {
        Godzila g = new Godzila(5);
        g.eat(14);
        g.eat(20);
        g.eat(60);

    }
}
