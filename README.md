public class main {
    public static void main(String[] args) {
        //create a generic enemy and call its functions
        Enemy e1 = new Enemy(100, 25);
        e1.attack();
            
         //create a fire and an ice wizard and call all functions
        Wizard w1 = new Wizard(125, 40, "ice");
        Wizard w2 = new Wizard(150, 50, "fire");
    
        w1.attack();
        w1.damageType();
        w2.attack();
        w2.damageType();
     
        //create a goblin and call its functions
        Goblin g1 = new Goblin(80,15);
        g1.attack();
        }
    }

public class Enemy {
    int health;
    int damage;

    public Enemy(int h, int d){
        health = h;
        damage = d;
    }

    void attack(){
        System.out.println("the enemy attacks");
    }
}
    
public class Wizard extends Enemy{
    String type;
    public Wizard(int h, int d, String t) {
        super(h, d);
        type = t;
    }
    void damageType(){

        if(type.equals("fire")) {
            System.out.println(" This wizard shoots a fireball.");
        } else {
        System.out.println(" This wizard shoots an iceball.");
        }
    }
}

public class Goblin extends Enemy{
    public Goblin(int h, int d) {
        super(h, d);
    }

    @Override
    void attack() {
        System.out.println("The goblin gobbles!");
    }
}
